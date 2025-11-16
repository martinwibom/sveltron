# Sveltron Template

A template for building cross-platform desktop applications using [SvelteKit](https://kit.svelte.dev/) and [Electron](https://www.electronjs.org/), powered by Vite.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or newer recommended)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

### Installation

```bash
npm install
# or
yarn install
```

### Development

To start the app in development mode with hot reload:

```bash
npm run start
```

This will launch both the Electron main process and the SvelteKit renderer with live reload.

### Create distributable installer

```bash
npm run make
```

This will create a distributable installer for your app. You can configure this in the makers section in forge.config.ts. Reference the makers documentation for more information.

### Packaging

This will build the app and you can find the output in the out directory. You can run the production app by opening the .app file in the out directory. This will not create your app's installer for distribution though.

```bash
npm run package
```

## Project Structure

```
/ (root)
├── electron/         # Electron main & preload scripts
│   ├── main.ts
│   └── preload.ts
├── src/              # SvelteKit app source
│   ├── app.html
│   ├── app.css
│   └── lib/
│   └── routes/
├── static/           # Static assets
├── package.json      # Project metadata & scripts
├── vite.config.ts    # Vite config for renderer
├── vite.main.config.ts # Vite config for Electron main
├── vite.preload.config.ts # Vite config for preload
├── forge.config.ts   # Electron Forge config
└── tsconfig.json     # TypeScript config
```

## Customization

- Update the `src/` directory to add your SvelteKit pages and components.
- Modify Electron behavior in `electron/main.ts` and `electron/preload.ts`.
- Adjust Vite and Forge configs as needed for your use case.

## License

This template is provided as-is, without warranty. Use it as a starting point for your own projects.
