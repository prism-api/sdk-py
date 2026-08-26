# Reference
## Api Evm Dex
<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">get_wallet_profile</a>(...) -> EvmDexWalletProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a wallet profile for a specific wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import EvmDexWalletProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.get_wallet_profile(
    chain_id=1,
    wallet="0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045",
    options=EvmDexWalletProfilePayloadOptions(
        include_metadata=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**wallet:** `str` — Wallet address to retrieve the profile for.
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[EvmDexWalletProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">search_wallet_profiles</a>(...) -> SearchWalletProfilesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter, query, and sort wallet profiles based on specified metrics and conditions.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import EvmDexWalletProfileSearchPayloadQuery, EvmDexProfileSearchPayloadSort, EvmDexWalletProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.search_wallet_profiles(
    limit=10,
    chain_id=1,
    query=EvmDexWalletProfileSearchPayloadQuery(
        fields=[
            "wallet_address"
        ],
        text="0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045",
    ),
    sort=EvmDexProfileSearchPayloadSort(
        field="metrics.7d.cumulative_pnl",
        direction="desc",
    ),
    options=EvmDexWalletProfilePayloadOptions(
        include_metadata=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return in a single page.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque cursor returned by a previous response. Pass it to fetch the next page of results.
    
</dd>
</dl>

<dl>
<dd>

**query:** `typing.Optional[EvmDexWalletProfileSearchPayloadQuery]` 
    
</dd>
</dl>

<dl>
<dd>

**filter:** `typing.Optional[EvmDexProfileSearchPayloadFilter]` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[EvmDexProfileSearchPayloadSort]` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[EvmDexWalletProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">get_token_profile</a>(...) -> EvmDexTokenProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the profile for a specific token.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import EvmDexTokenProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.get_token_profile(
    chain_id=1,
    token="0x6982508145454Ce325dDbE47a25d4ec3d2311933",
    options=EvmDexTokenProfilePayloadOptions(
        include_metadata=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**token:** `str` — Token address to retrieve the profile for.
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[EvmDexTokenProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">search_token_profiles</a>(...) -> SearchTokenProfilesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter, query, and sort token profiles based on specified metrics and conditions.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import EvmDexTokenProfileSearchPayloadQueryField, EvmDexProfileSearchPayloadSort, EvmDexTokenProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.search_token_profiles(
    limit=10,
    chain_id=1,
    query=EvmDexTokenProfileSearchPayloadQueryField(
        fields=[
            "token_address"
        ],
        text="0x6982508145454Ce325dDbE47a25d4ec3d2311933",
    ),
    sort=EvmDexProfileSearchPayloadSort(
        field="metrics.1d.usd_volume",
        direction="desc",
    ),
    options=EvmDexTokenProfilePayloadOptions(
        include_metadata=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return in a single page.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque cursor returned by a previous response. Pass it to fetch the next page of results.
    
</dd>
</dl>

<dl>
<dd>

**query:** `typing.Optional[EvmDexTokenProfileSearchPayloadQueryField]` 
    
</dd>
</dl>

<dl>
<dd>

**filter:** `typing.Optional[EvmDexProfileSearchPayloadFilter]` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[EvmDexProfileSearchPayloadSort]` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[EvmDexTokenProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">get_position_profile</a>(...) -> EvmDexPositionProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a position profile for a specific wallet-token pair.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import EvmDexPositionProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.get_position_profile(
    chain_id=1,
    wallet="0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045",
    token="0x6982508145454Ce325dDbE47a25d4ec3d2311933",
    options=EvmDexPositionProfilePayloadOptions(
        include_metadata=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**wallet:** `str` — Wallet address of the position to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**token:** `str` — Token address of the position to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[EvmDexPositionProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">search_position_profiles</a>(...) -> SearchPositionProfilesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter, query, and sort position profiles based on specified metrics and conditions.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import EvmDexProfileSearchPayloadSort, EvmDexPositionProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.search_position_profiles(
    limit=10,
    chain_id=1,
    sort=EvmDexProfileSearchPayloadSort(
        field="metrics.7d.pnl",
        direction="desc",
    ),
    options=EvmDexPositionProfilePayloadOptions(
        include_metadata=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return in a single page.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque cursor returned by a previous response. Pass it to fetch the next page of results.
    
</dd>
</dl>

<dl>
<dd>

**filter:** `typing.Optional[EvmDexProfileSearchPayloadFilter]` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[EvmDexProfileSearchPayloadSort]` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[EvmDexPositionProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">get_trades</a>(...) -> GetTradesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns trades for a wallet and/or token on a single chain.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.get_trades(
    limit=20,
    chain_id=1,
    wallet="0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return in a single page.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque cursor returned by a previous response. Pass it to fetch the next page of results.
    
</dd>
</dl>

<dl>
<dd>

**wallet:** `typing.Optional[str]` — Wallet address to filter trades by.
    
</dd>
</dl>

<dl>
<dd>

**token:** `typing.Optional[str]` — Token address to filter trades by.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">get_swaps</a>(...) -> GetSwapsDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns swaps for a combination of wallet, token and/or pool.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.get_swaps(
    limit=20,
    chain_id=1,
    wallet="0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return in a single page.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque cursor returned by a previous response. Pass it to fetch the next page of results.
    
</dd>
</dl>

<dl>
<dd>

**wallet:** `typing.Optional[str]` — Wallet address to filter swaps by.
    
</dd>
</dl>

<dl>
<dd>

**token:** `typing.Optional[str]` — Token address to filter swaps by.
    
</dd>
</dl>

<dl>
<dd>

**pool:** `typing.Optional[str]` — Pool address to filter swaps by.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">get_price</a>(...) -> typing.List[EvmDexPrice]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns prices for one or more tokens or pools.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.get_price(
    chain_id=1,
    tokens=[
        "0x6982508145454Ce325dDbE47a25d4ec3d2311933"
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**tokens:** `typing.Optional[typing.List[str]]` — Token addresses to retrieve the latest prices for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `typing.Optional[typing.List[str]]` — Pool addresses to retrieve the latest prices for.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">get_price_stats</a>(...) -> typing.List[EvmDexPriceStats]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price stats for one or more tokens or pools.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.get_price_stats(
    chain_id=1,
    tokens=[
        "0x6982508145454Ce325dDbE47a25d4ec3d2311933"
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**tokens:** `typing.Optional[typing.List[str]]` — Token addresses to retrieve price statistics for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `typing.Optional[typing.List[str]]` — Pool addresses to retrieve price statistics for.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">get_price_candles</a>(...) -> typing.List[EvmDexPriceCandle]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price candles for a specific token and/or pool.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
import datetime

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.get_price_candles(
    chain_id=1,
    token="0x6982508145454Ce325dDbE47a25d4ec3d2311933",
    from_=datetime.datetime.fromisoformat("2026-04-27T00:00:00+00:00"),
    to=datetime.datetime.fromisoformat("2026-04-27T01:00:00+00:00"),
    interval=60,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**interval:** `int` — Sampling interval between data points, in seconds.
    
</dd>
</dl>

<dl>
<dd>

**token:** `typing.Optional[str]` — Token address to filter by.
    
</dd>
</dl>

<dl>
<dd>

**pool:** `typing.Optional[str]` — Pool address to filter by.
    
</dd>
</dl>

<dl>
<dd>

**from:** `typing.Optional[datetime.datetime]` 

Start of the candle range, as a date-time RFC3339 string.
Can be combined with `to` to define a bounded range.
    
</dd>
</dl>

<dl>
<dd>

**to:** `typing.Optional[datetime.datetime]` 

End of the candle range, as a date-time RFC3339 string. 
Defaults to the current time.
    
</dd>
</dl>

<dl>
<dd>

**count:** `typing.Optional[int]` 

Number of candles to return.
Must be combined with `from` or `to`.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.evm.dex.<a href="src/prism/api/evm/dex/client.py">get_price_history</a>(...) -> typing.List[EvmDexPriceHistory]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price history for one or more tokens or pools.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
import datetime

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.evm.dex.get_price_history(
    chain_id=1,
    tokens=[
        "0x6982508145454Ce325dDbE47a25d4ec3d2311933"
    ],
    from_=datetime.datetime.fromisoformat("2026-04-27T00:00:00+00:00"),
    to=datetime.datetime.fromisoformat("2026-04-27T01:00:00+00:00"),
    interval=3600,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**chain_id:** `int` — Numeric EVM chain ID to query. See [Supported Chains](/documentation/evm/overview#supported-chains).
    
</dd>
</dl>

<dl>
<dd>

**from:** `datetime.datetime` — Start of the history range, as a date-time RFC3339 string.
    
</dd>
</dl>

<dl>
<dd>

**interval:** `int` — Sampling interval between data points, in seconds.
    
</dd>
</dl>

<dl>
<dd>

**tokens:** `typing.Optional[typing.List[str]]` — Token addresses to retrieve price history for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `typing.Optional[typing.List[str]]` — Pool addresses to retrieve price history for.
    
</dd>
</dl>

<dl>
<dd>

**to:** `typing.Optional[datetime.datetime]` 

End of the history range, as a date-time RFC3339 string. 
Defaults to the current time.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Api Solana Dex
<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">get_wallet_profile</a>(...) -> SolanaDexWalletProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a wallet profile for a specific wallet.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import SolanaDexWalletProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
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
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**wallet:** `str` — Wallet address to retrieve the profile for.
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[SolanaDexWalletProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">search_wallet_profiles</a>(...) -> SearchWalletProfilesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter, query, and sort wallet profiles based on specified metrics and conditions.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import SolanaDexWalletProfileSearchPayloadQuery, SolanaDexProfileSearchPayloadSort, SolanaDexProfileSearchPayloadFilter, SolanaDexWalletProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.search_wallet_profiles(
    limit=10,
    query=SolanaDexWalletProfileSearchPayloadQuery(
        fields=[
            "identity.name"
        ],
        text="cupsey",
    ),
    sort=SolanaDexProfileSearchPayloadSort(
        field="metrics.7d.cumulative_pnl",
        direction="desc",
    ),
    dynamic_labels={
        "smart": SolanaDexProfileSearchPayloadFilter()
    },
    options=SolanaDexWalletProfilePayloadOptions(
        include_metadata=True,
        include_labels=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return in a single page.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque cursor returned by a previous response. Pass it to fetch the next page of results.
    
</dd>
</dl>

<dl>
<dd>

**query:** `typing.Optional[SolanaDexWalletProfileSearchPayloadQuery]` 
    
</dd>
</dl>

<dl>
<dd>

**filter:** `typing.Optional[SolanaDexProfileSearchPayloadFilter]` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[SolanaDexProfileSearchPayloadSort]` 
    
</dd>
</dl>

<dl>
<dd>

**dynamic_labels:** `typing.Optional[SolanaDexProfileSearchPayloadDynamicLabels]` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[SolanaDexWalletProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">get_token_profile</a>(...) -> SolanaDexTokenProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the profile for a specific token.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import SolanaDexTokenProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.get_token_profile(
    token="Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk",
    options=SolanaDexTokenProfilePayloadOptions(
        include_metadata=True,
        include_market=True,
        include_labels=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**token:** `str` — Token address to retrieve the profile for.
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[SolanaDexTokenProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">search_token_profiles</a>(...) -> SearchTokenProfilesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter, query, and sort token profiles based on specified metrics and conditions.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import SolanaDexTokenProfileSearchPayloadQueryField, SolanaDexProfileSearchPayloadSort, SolanaDexProfileSearchPayloadFilter, SolanaDexTokenProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.search_token_profiles(
    limit=10,
    query=SolanaDexTokenProfileSearchPayloadQueryField(
        fields=[
            "metadata.name"
        ],
        text="bonk",
    ),
    sort=SolanaDexProfileSearchPayloadSort(
        field="market.liquidity",
        direction="desc",
    ),
    dynamic_labels={
        "trending": SolanaDexProfileSearchPayloadFilter()
    },
    options=SolanaDexTokenProfilePayloadOptions(
        include_metadata=True,
        include_market=True,
        include_labels=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return in a single page.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque cursor returned by a previous response. Pass it to fetch the next page of results.
    
</dd>
</dl>

<dl>
<dd>

**query:** `typing.Optional[SolanaDexTokenProfileSearchPayloadQueryField]` 
    
</dd>
</dl>

<dl>
<dd>

**filter:** `typing.Optional[SolanaDexProfileSearchPayloadFilter]` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[SolanaDexProfileSearchPayloadSort]` 
    
</dd>
</dl>

<dl>
<dd>

**dynamic_labels:** `typing.Optional[SolanaDexProfileSearchPayloadDynamicLabels]` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[SolanaDexTokenProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">get_position_profile</a>(...) -> SolanaDexPositionProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a position profile for a specific wallet-token pair.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import SolanaDexPositionProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.get_position_profile(
    wallet="suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
    token="Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk",
    options=SolanaDexPositionProfilePayloadOptions(
        include_metadata=True,
        include_labels=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**wallet:** `str` — Wallet address of the position to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**token:** `str` — Token address of the position to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[SolanaDexPositionProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">search_position_profiles</a>(...) -> SearchPositionProfilesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Filter, query, and sort position profiles based on specified metrics and conditions.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
from prism.api import SolanaDexProfileSearchPayloadSort, SolanaDexProfileSearchPayloadFilter, SolanaDexPositionProfilePayloadOptions

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.search_position_profiles(
    limit=10,
    sort=SolanaDexProfileSearchPayloadSort(
        field="metrics.7d.pnl",
        direction="desc",
    ),
    dynamic_labels={
        "winner": SolanaDexProfileSearchPayloadFilter()
    },
    options=SolanaDexPositionProfilePayloadOptions(
        include_metadata=True,
        include_labels=True,
        include_metrics=[
            "7d"
        ],
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return in a single page.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque cursor returned by a previous response. Pass it to fetch the next page of results.
    
</dd>
</dl>

<dl>
<dd>

**filter:** `typing.Optional[SolanaDexProfileSearchPayloadFilter]` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[SolanaDexProfileSearchPayloadSort]` 
    
</dd>
</dl>

<dl>
<dd>

**dynamic_labels:** `typing.Optional[SolanaDexProfileSearchPayloadDynamicLabels]` 
    
</dd>
</dl>

<dl>
<dd>

**options:** `typing.Optional[SolanaDexPositionProfilePayloadOptions]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">get_trades</a>(...) -> GetTradesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns trades for a combination of wallet, token and/or pool.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.get_trades(
    limit=20,
    wallet="suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return in a single page.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque cursor returned by a previous response. Pass it to fetch the next page of results.
    
</dd>
</dl>

<dl>
<dd>

**wallet:** `typing.Optional[str]` — Wallet address to filter trades by.
    
</dd>
</dl>

<dl>
<dd>

**token:** `typing.Optional[str]` — Token address to filter trades by.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">get_swaps</a>(...) -> GetSwapsDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns swaps for a combination of wallet, token and/or pool.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.get_swaps(
    limit=20,
    wallet="suqh5sHtr8HyJ7q8scBimULPkPpA557prMG47xCHQfK",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return in a single page.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque cursor returned by a previous response. Pass it to fetch the next page of results.
    
</dd>
</dl>

<dl>
<dd>

**wallet:** `typing.Optional[str]` — Wallet address to filter swaps by.
    
</dd>
</dl>

<dl>
<dd>

**token:** `typing.Optional[str]` — Token address to filter swaps by.
    
</dd>
</dl>

<dl>
<dd>

**pool:** `typing.Optional[str]` — Pool address to filter swaps by.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">get_price</a>(...) -> typing.List[SolanaDexPrice]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns prices for one or more tokens or pools.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.get_price(
    tokens=[
        "Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk"
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tokens:** `typing.Optional[typing.List[str]]` — Token addresses to retrieve the latest prices for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `typing.Optional[typing.List[str]]` — Pool addresses to retrieve the latest prices for.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">get_price_stats</a>(...) -> typing.List[SolanaDexPriceStats]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price stats for one or more tokens or pools.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.get_price_stats(
    tokens=[
        "Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk"
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tokens:** `typing.Optional[typing.List[str]]` — Token addresses to retrieve price statistics for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `typing.Optional[typing.List[str]]` — Pool addresses to retrieve price statistics for.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">get_price_candles</a>(...) -> typing.List[SolanaDexPriceCandle]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price candles for a specific token and/or pool.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
import datetime

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.get_price_candles(
    token="Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk",
    from_=datetime.datetime.fromisoformat("2026-04-27T00:00:00+00:00"),
    to=datetime.datetime.fromisoformat("2026-04-27T01:00:00+00:00"),
    interval=60,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**interval:** `int` — Sampling interval between data points, in seconds.
    
</dd>
</dl>

<dl>
<dd>

**token:** `typing.Optional[str]` — Token address to filter by.
    
</dd>
</dl>

<dl>
<dd>

**pool:** `typing.Optional[str]` — Pool address to filter by.
    
</dd>
</dl>

<dl>
<dd>

**from:** `typing.Optional[datetime.datetime]` 

Start of the candle range, as a date-time RFC3339 string.
Can be combined with `to` to define a bounded range.
    
</dd>
</dl>

<dl>
<dd>

**to:** `typing.Optional[datetime.datetime]` 

End of the candle range, as a date-time RFC3339 string. 
Defaults to the current time.
    
</dd>
</dl>

<dl>
<dd>

**count:** `typing.Optional[int]` 

Number of candles to return.
Must be combined with `from` or `to`.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api.solana.dex.<a href="src/prism/api/solana/dex/client.py">get_price_history</a>(...) -> typing.List[SolanaDexPriceHistory]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price history for one or more tokens or pools.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from prism import Client
from prism.environment import ClientEnvironment
import datetime

client = Client(
    api_key="<value>",
    environment=ClientEnvironment.PRODUCTION,
)

client.api.solana.dex.get_price_history(
    tokens=[
        "Z4d9YXR4pSkdKcu9UBcwxHp7i32buzdDtAR1b1Gbonk"
    ],
    from_=datetime.datetime.fromisoformat("2026-04-27T00:00:00+00:00"),
    to=datetime.datetime.fromisoformat("2026-04-27T01:00:00+00:00"),
    interval=3600,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**from:** `datetime.datetime` — Start of the history range, as a date-time RFC3339 string.
    
</dd>
</dl>

<dl>
<dd>

**interval:** `int` — Sampling interval between data points, in seconds.
    
</dd>
</dl>

<dl>
<dd>

**tokens:** `typing.Optional[typing.List[str]]` — Token addresses to retrieve price history for.
    
</dd>
</dl>

<dl>
<dd>

**pools:** `typing.Optional[typing.List[str]]` — Pool addresses to retrieve price history for.
    
</dd>
</dl>

<dl>
<dd>

**to:** `typing.Optional[datetime.datetime]` 

End of the history range, as a date-time RFC3339 string. 
Defaults to the current time.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

