# Zora Discovery

Public web compilation surface for the Fold-Space / Zora Discovery app family.
This repo combines the original Fold-Space Engine Vite shell with the full ZoraASI Bridge / Phase V surface into one flat-tab application.

Live site:

- https://cbaird26.github.io/zora-discovery/

Related public repos:

- Part I public foundation: [`fold-space-engine`](https://github.com/Cbaird26/fold-space-engine)
- Part II artifact/reference: [`fold-space-engine-phase-v`](https://github.com/Cbaird26/fold-space-engine-phase-v)
- Mobile shell: [`zora-discovery-mobile`](https://github.com/Cbaird26/zora-discovery-mobile)
- Desktop shell: [`zora-discovery-desktop`](https://github.com/Cbaird26/zora-discovery-desktop)

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
- App shell settings use a separate namespace: `zora-discovery-shell-state`.

## Freeze boundary

This repo is the canonical public web compilation surface.

That means:

- it stays web-only
- Phase V remains the artifact/reference repo
- mobile changes happen only in `zora-discovery-mobile`
- desktop changes happen only in `zora-discovery-desktop`

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
