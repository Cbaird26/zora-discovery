# Zora Discovery

Public compilation repo that combines the original Fold-Space Engine Vite shell with the full ZoraASI Bridge / Phase V surface into one flat-tab application.

This repo is the combined runtime. It does not modify either source repo:

- Part I source: `~/fold-space-engine`
- Part II source: `~/fold-space-engine-phase-v`

## Top-level tabs

- `Probability Sculptor`
- `Fold-Space Engine`
- `Timeline Selector`
- `Decision`
- `Intent`
- `Navigation`
- `Research`

Default opening tab: `Probability Sculptor`

## Composition model

- The first three tabs preserve the original Part I shell behavior.
- The last four tabs run inside the imported `ZoraASI Bridge` wrapper.
- `ZoraASI Bridge` is shared shell behavior, not a separate tab.
- The imported discovery state uses its own localStorage namespace: `zora-discovery-product-state`.

## Local development

```bash
npm install
npm run dev
```

## Test and build

```bash
npm test
npm run build
```

## Deployment

This repo is configured for GitHub Pages from the Vite `dist/` output.

Expected public URL:

`https://cbaird26.github.io/zora-discovery/`

## Docs

Imported Phase V reference docs are kept in [`docs/`](./docs/).
