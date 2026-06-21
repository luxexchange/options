# @luxfi/options

Options-chain UI components for Lux Exchange.

A set of headless-leaning, monochrome React components for building an
options/derivatives trading surface — the chain grid, order ticket,
multi-leg strategy builder, positions table, expiration selector and
symbol search. Styling is driven by Tailwind utility classes and a small
set of CSS variables, so consumers supply their own brand layer.

## Install

```bash
pnpm add @luxfi/options
```

Peer dependencies: `react` and `react-dom` (19+).

## Components

| Export | Description |
|--------|-------------|
| `SymbolSearch` | Underlying/symbol picker with inline search. |
| `ExpirationBar` | Horizontal expiration-date selector. |
| `OptionsChain` | Strike-by-strike calls/puts chain grid. |
| `OptionsOrderForm` | Single-leg order ticket (limit/market, buy/sell). |
| `StrategyPanel` | Multi-leg strategy builder with templates. |
| `PositionsTable` | Open-positions table with close actions. |

UI primitives (`Button`, `Card`, `Input`, `TokenIcon`, `cn`) are also
re-exported for consumers that want to compose with the same building blocks.

## Types

The package ships a broad set of instrument types covering options,
margin, futures, FX, fixed income and a unified `Instrument` shape, plus
default `STRATEGY_TEMPLATES` and `OPTIONS_APPROVAL_LEVELS` that consumers
can extend or override.

```ts
import {
  OptionsChain,
  OptionsOrderForm,
  StrategyPanel,
  type OptionStrike,
  type StrategyOrder,
} from "@luxfi/options"
```

## License

BSD-3-Clause © 2020-2026 Lux Industries, Inc. See [LICENSE](./LICENSE).

Extracted from the Lux Exchange monorepo as a standalone, non-GPL package.
