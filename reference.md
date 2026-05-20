# Reference
## Solana Dex
<details><summary><code>client.solana.dex.<a href="src/prism/solana/dex/client.py">get_wallet_profile</a>(...) -> SolanaDexWalletProfile</code></summary>
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
from prism import ApiClient, SolanaDexWalletProfilePayloadOptions
from prism.environment import ApiClientEnvironment

client = ApiClient(
    api_key="<value>",
    environment=ApiClientEnvironment.DEFAULT,
)

client.solana.dex.get_wallet_profile(
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

<details><summary><code>client.solana.dex.<a href="src/prism/solana/dex/client.py">search_wallet_profiles</a>(...) -> SearchWalletProfilesDexResponse</code></summary>
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
from prism import ApiClient, SolanaDexWalletProfileSearchPayloadQuery, SolanaDexProfileSearchPayloadSort, SolanaDexProfileSearchPayloadFilter, SolanaDexWalletProfilePayloadOptions
from prism.environment import ApiClientEnvironment

client = ApiClient(
    api_key="<value>",
    environment=ApiClientEnvironment.DEFAULT,
)

client.solana.dex.search_wallet_profiles(
    limit=10,
    query=SolanaDexWalletProfileSearchPayloadQuery(
        text="cupsey",
        fields=[
            "wallet_address"
        ],
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

<details><summary><code>client.solana.dex.<a href="src/prism/solana/dex/client.py">get_token_profile</a>(...) -> SolanaDexTokenProfile</code></summary>
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
from prism import ApiClient, SolanaDexTokenProfilePayloadOptions
from prism.environment import ApiClientEnvironment

client = ApiClient(
    api_key="<value>",
    environment=ApiClientEnvironment.DEFAULT,
)

client.solana.dex.get_token_profile(
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

<details><summary><code>client.solana.dex.<a href="src/prism/solana/dex/client.py">search_token_profiles</a>(...) -> SearchTokenProfilesDexResponse</code></summary>
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
from prism import ApiClient, SolanaDexTokenProfileSearchPayloadQueryField, SolanaDexProfileSearchPayloadSort, SolanaDexProfileSearchPayloadFilter, SolanaDexTokenProfilePayloadOptions
from prism.environment import ApiClientEnvironment

client = ApiClient(
    api_key="<value>",
    environment=ApiClientEnvironment.DEFAULT,
)

client.solana.dex.search_token_profiles(
    limit=10,
    query=SolanaDexTokenProfileSearchPayloadQueryField(
        text="bonk",
        fields=[
            "metadata.name"
        ],
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

<details><summary><code>client.solana.dex.<a href="src/prism/solana/dex/client.py">get_trades</a>(...) -> GetTradesDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns trades for a wallet, token or both.
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
from prism import ApiClient
from prism.environment import ApiClientEnvironment

client = ApiClient(
    api_key="<value>",
    environment=ApiClientEnvironment.DEFAULT,
)

client.solana.dex.get_trades(
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

**wallet:** `typing.Optional[str]` — Wallet address to filter trades by. When combined with `token`, returns only trades for that wallet on that token.
    
</dd>
</dl>

<dl>
<dd>

**token:** `typing.Optional[str]` — Token address to filter trades by. When combined with `wallet`, returns only trades for that wallet on that token.
    
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

<details><summary><code>client.solana.dex.<a href="src/prism/solana/dex/client.py">get_swaps</a>(...) -> GetSwapsDexResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns swaps for a wallet, token or both.
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
from prism import ApiClient
from prism.environment import ApiClientEnvironment

client = ApiClient(
    api_key="<value>",
    environment=ApiClientEnvironment.DEFAULT,
)

client.solana.dex.get_swaps(
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

**wallet:** `typing.Optional[str]` — Wallet address to filter swaps by. When combined with `token`, returns only swaps for that wallet on that token.
    
</dd>
</dl>

<dl>
<dd>

**token:** `typing.Optional[str]` — Token address to filter swaps by. When combined with `wallet`, returns only swaps for that wallet on that token.
    
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

<details><summary><code>client.solana.dex.<a href="src/prism/solana/dex/client.py">get_price</a>(...) -> typing.List[SolanaDexPrice]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns prices for one or more tokens.
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
from prism import ApiClient
from prism.environment import ApiClientEnvironment

client = ApiClient(
    api_key="<value>",
    environment=ApiClientEnvironment.DEFAULT,
)

client.solana.dex.get_price(
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

**tokens:** `typing.List[str]` — Token addresses to retrieve the latest prices for. Accepts between 1 and 1000 tokens per request.
    
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

<details><summary><code>client.solana.dex.<a href="src/prism/solana/dex/client.py">get_price_stats</a>(...) -> typing.List[SolanaDexPriceStats]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price stats for one or more tokens.
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
from prism import ApiClient
from prism.environment import ApiClientEnvironment

client = ApiClient(
    api_key="<value>",
    environment=ApiClientEnvironment.DEFAULT,
)

client.solana.dex.get_price_stats(
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

**tokens:** `typing.List[str]` — Token addresses to retrieve price statistics for. Accepts between 1 and 1000 tokens per request.
    
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

<details><summary><code>client.solana.dex.<a href="src/prism/solana/dex/client.py">get_price_candles</a>(...) -> typing.List[SolanaDexPriceCandle]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price candles for a specific token.
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
from prism import ApiClient
from prism.environment import ApiClientEnvironment
import datetime

client = ApiClient(
    api_key="<value>",
    environment=ApiClientEnvironment.DEFAULT,
)

client.solana.dex.get_price_candles(
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

**token:** `str` — Token address to retrieve price candles for.
    
</dd>
</dl>

<dl>
<dd>

**interval:** `int` — Sampling interval between data points, in seconds.
    
</dd>
</dl>

<dl>
<dd>

**from:** `typing.Optional[datetime.datetime]` 

Start of the candle range, as a date-time RFC3339 string.
Must be combined with `to` to define a bounded range.
    
</dd>
</dl>

<dl>
<dd>

**to:** `typing.Optional[datetime.datetime]` 

End of the candle range, as a date-time RFC3339 string. Defaults to the current time.
Must be combined with either `from` (to define a bounded range) or `count` (to return the N most recent candles ending at `to`).
    
</dd>
</dl>

<dl>
<dd>

**count:** `typing.Optional[int]` 

Number of candles to return, ending at `to`.
Must be combined with `to`.
    
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

<details><summary><code>client.solana.dex.<a href="src/prism/solana/dex/client.py">get_price_history</a>(...) -> typing.List[SolanaDexPriceHistory]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns price history for one or more tokens.
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
from prism import ApiClient
from prism.environment import ApiClientEnvironment
import datetime

client = ApiClient(
    api_key="<value>",
    environment=ApiClientEnvironment.DEFAULT,
)

client.solana.dex.get_price_history(
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

**tokens:** `typing.List[str]` — Token addresses to retrieve price history for. Accepts between 1 and 100 tokens per request.
    
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

**to:** `typing.Optional[datetime.datetime]` — End of the history range, as a date-time RFC3339 string. Defaults to the current time.
    
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

