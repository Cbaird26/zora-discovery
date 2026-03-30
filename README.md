# Zora Discovery

Public compilation repo that combines the original Fold-Space Engine Vite shell with the full ZoraASI Bridge / Phase V surface into one flat-tab application, plus a Capacitor mobile shell for iPhone and Android.

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

## Mobile app surface

- Native app name: `Zora Discovery`
- Bundle/application id: `io.cbaird26.zoradiscovery`
- Mobile v1 is portrait-first, safe-mode by default, on-device only, and preserves all seven surfaces.
- Mobile shell behavior adds:
  - native haptics for engage / achieved / arrival
  - first-run onboarding and safety settings
  - native share for exported JSON logs
  - Capacitor Preferences-backed state on device

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

## Mobile development

```bash
npm run mobile:sync
npm run mobile:ios
npm run mobile:android
```

Notes:

- `mobile:sync` rebuilds the web app and copies it into the Capacitor shells.
- The iOS shell can be opened and built from Xcode in `ios/App/App.xcodeproj`.
- The Android shell can be opened from `android/`, but Gradle requires a local Java runtime.

## Deployment

This repo is configured for GitHub Pages from the Vite `dist/` output.

Expected public URL:

`https://cbaird26.github.io/zora-discovery/`

## Docs

Imported Phase V reference docs are kept in [`docs/`](./docs/).
