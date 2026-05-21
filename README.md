# Prism Python Library

[![fern shield](https://img.shields.io/badge/%F0%9F%8C%BF-Built%20with%20Fern-brightgreen)](https://buildwithfern.com?utm_source=github&utm_medium=github&utm_campaign=readme&utm_source=https%3A%2F%2Fgithub.com%2Fprism-api%2Fsdk-py)
[![pypi](https://img.shields.io/pypi/v/prism-py-sdk)](https://pypi.python.org/pypi/prism-py-sdk)

The Prism API SDK provides convenient access to the Prism APIs from your favorite programming language.

## Table of Contents

- [Documentation](#documentation)
- [Installation](#installation)
- [Reference](#reference)
- [Usage](#usage)
- [Environments](#environments)
- [Async Client](#async-client)
- [Exception Handling](#exception-handling)
- [Websockets](#websockets)
- [Advanced](#advanced)
  - [Access Raw Response Data](#access-raw-response-data)
  - [Retries](#retries)
  - [Timeouts](#timeouts)
  - [Custom Client](#custom-client)
- [Contributing](#contributing)

## Documentation

API reference documentation is available [here](https://docs.prismapi.io/api-reference).

## Installation

```sh
pip install prism-py-sdk
```

## Reference

A full reference for this library is available [here](https://github.com/prism-api/sdk-py/blob/HEAD/./reference.md).

## Usage

Instantiate and use the client with the following:

```python
from prism import Client
from prism.api import SolanaDexWalletProfilePayloadOptions

client = Client(
    api_key="<value>",
)

client.api.solana.dex.get_wallet_profile(
    wallet="suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
    options=SolanaDexWalletProfilePayloadOptions(
        include_metadata=True,
        include_labels=True,
        include_metrics=[
            "7d"
        ],
    ),
)
```

## Environments

This SDK allows you to configure different environments for API requests.

```python
from prism import Client
from prism.environment import ClientEnvironment

client = Client(
    environment=ClientEnvironment.PRODUCTION,
)
```

## Async Client

The SDK also exports an `async` client so that you can make non-blocking calls to our API. Note that if you are constructing an Async httpx client class to pass into this client, use `httpx.AsyncClient()` instead of `httpx.Client()` (e.g. for the `httpx_client` parameter of this client).

```python
import asyncio
from prism.api import SolanaDexWalletProfilePayloadOptions

from prism import AsyncClient

client = AsyncClient(
    api_key="<value>",
)


async def main() -> None:
    await client.api.solana.dex.get_wallet_profile(
        wallet="suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
        options=SolanaDexWalletProfilePayloadOptions(
            include_metadata=True,
            include_labels=True,
            include_metrics=[
                "7d"
            ],
        ),
    )


asyncio.run(main())
```

## Exception Handling

When the API returns a non-success status code (4xx or 5xx response), a subclass of the following error
will be thrown.

```python
from prism.core.api_error import ApiError

try:
    client.api.solana.dex.get_wallet_profile(...)
except ApiError as e:
    print(e.status_code)
    print(e.body)
```

## Websockets

The SDK supports both sync and async websocket connections for real-time, low-latency communication. Sockets can be created using the `connect` method, which returns a context manager. 
You can either iterate through the returned `SocketClient` to process messages as they arrive, or attach handlers to respond to specific events.

```python
from prism import Client

client = Client(...)

# Connect to the websocket (Sync)
with client.subscription.connect(...) as socket:
    # Iterate over the messages as they arrive
    for message in socket:
        print(message)

    # Or, attach handlers to specific events
    socket.on(EventType.MESSAGE, lambda message: print("received message", message))

import asyncio
from prism import AsyncClient

client = AsyncClient(...)

# Connect to the websocket (Async)
async with client.subscription.connect(...) as socket:
    async for message in socket:
        print(message)
```

## Advanced

### Access Raw Response Data

The SDK provides access to raw response data, including headers, through the `.with_raw_response` property.
The `.with_raw_response` property returns a "raw" client that can be used to access the `.headers` and `.data` attributes.

```python
from prism import Client

client = Client(...)
response = client.api.solana.dex.with_raw_response.get_wallet_profile(...)
print(response.headers)  # access the response headers
print(response.status_code)  # access the response status code
print(response.data)  # access the underlying object
```

### Retries

The SDK is instrumented with automatic retries with exponential backoff. A request will be retried as long
as the request is deemed retryable and the number of retry attempts has not grown larger than the configured
retry limit (default: 2).

Which status codes are retried depends on the `retryStatusCodes` generator configuration:

**`legacy`** (current default): retries on
- [408](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/408) (Timeout)
- [409](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/409) (Conflict)
- [429](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/429) (Too Many Requests)
- [5XX](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status#server_error_responses) (All server errors, including 500)

**`recommended`**: retries on
- [408](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/408) (Timeout)
- [409](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/409) (Conflict)
- [429](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/429) (Too Many Requests)
- [502](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/502) (Bad Gateway)
- [503](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/503) (Service Unavailable)
- [504](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/504) (Gateway Timeout)

Use the `max_retries` request option to configure this behavior.

```python
client.api.solana.dex.get_wallet_profile(..., request_options={
    "max_retries": 1
})
```

### Timeouts

The SDK defaults to a 60 second timeout. You can configure this with a timeout option at the client or request level.

```python
from prism import Client

client = Client(..., timeout=20.0)

# Override timeout for a specific method
client.api.solana.dex.get_wallet_profile(..., request_options={
    "timeout_in_seconds": 1
})
```

### Custom Client

You can override the `httpx` client to customize it for your use-case. Some common use-cases include support for proxies
and transports.

```python
import httpx
from prism import Client

client = Client(
    ...,
    httpx_client=httpx.Client(
        proxy="http://my.test.proxy.example.com",
        transport=httpx.HTTPTransport(local_address="0.0.0.0"),
    ),
)
```

## Contributing

While we value open-source contributions to this SDK, this library is generated programmatically.
Additions made directly to this library would have to be moved over to our generation code,
otherwise they would be overwritten upon the next generated release. Feel free to open a PR as
a proof of concept, but know that we will not be able to merge it as-is. We suggest opening
an issue first to discuss with us!

On the other hand, contributions to the README are always very welcome!
