# Svelte-Todo - Svelte Todo App

[![Netlify Status](https://api.netlify.com/api/v1/badges/b0c8ea6a-b6d2-46c8-9c14-7a401c937096/deploy-status)](https://app.netlify.com/sites/sveltesapper-todo/deploys)

## Demo

[Demo](https://sveltesapper-todo.netlify.app/)

Todo Application with Sapper (GraphQL API)
This project was created to explore new frontend libraries.

Note: This project is working in progress.

## ❓ What is this

This is an extension to the [official Sapper Rollup template](https://github.com/sveltejs/sapper-template-rollup) with TypeScript preprocessing and a GraphQL server through TypeGraphQL (Apollo Server).

- [Sapper for Svelte](https://sapper.svelte.dev/)
  - [Official VS Code Plugin](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode)
- [TypeScript](https://www.typescriptlang.org/)
  - [TypeGraphQL](https://typegraphql.ml/)
  - Inside Svelte components, thanks to [`svelte-preprocess`](https://github.com/kaisermann/svelte-preprocess)
- [Progressive Web App (PWA)](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps) best practices set up
  - [`manifest.json`](https://developer.mozilla.org/en-US/docs/Web/Manifest)'s most important fields filled out
  - High [Lighthouse](https://developers.google.com/web/tools/lighthouse) audit score
- [ESLint](https://eslint.org/)
  - [VS Code Plugin](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
  - `eslint:fix` package script

## 📋 Copy

Choose either to clone or fork depending on your preference.

### 🐑 Clone

```sh
git clone https://github.com/codenuru/svelte-todo
```

### ⬇️ Install Dependencies

```sh
cd svelte-todo
yarn  # npm also works
```

## 🛠 Usage

### 🧪 Development

```sh
yarn dev
```

### 🔨 Building for Production

If you do not need to include heavy Babel transforms and polyfills to support old browsers on your site, then remove the `--legacy` flag in the `sapper:build` package script to lighten it up.

```sh
yarn prod
```

### 📦 Exporting a Static Site

Your GraphQL server will not be exported with the rest of the site.

If you do not need to include heavy Babel transforms and polyfills to support old browsers on your site, then remove the `--legacy` flag in the `export` package script to lighten it up.

```sh
npm run export
```

## ⚙ Configuration

### ⚡ Web app

Many of the fields in `static/manifest.json` (`short_name`, `name`, `description`, `categories`, `theme_color`, and `background_color`) are filled with demonstrative values that won't match your site. Similarly, you've got to take new screenshots to replace the included `static/screenshot-1.png` and `static/screenshot-2.png` files. If you want, you can add [app shortcut definitions for "add to home screen" on Android](https://web.dev/app-shortcuts/#define-app-shortcuts-in-the-web-app-manifest). Once you change `theme_color`, update the `meta name="theme-color"` tag in `src/template.html` to match.

The [Apple touch icon](https://developer.apple.com/library/archive/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html), favicon, and `logo-` files (also all in the `static` directory) are created by placing the logo within a "safe area" centered circle that takes up 80% of the canvas's dimension. For instance, the constraining circle in `logo-512.png` is 512 × 0.80 = 409.6 ≈ 410 pixels wide and tall.

### 🗺 Source maps

This project base comes with [source maps](https://blog.teamtreehouse.com/introduction-source-maps) enabled during development and disabled during production for the best compromise between performance and developer experience. You can change this behavior through the `sourcemap` variable in `rollup.config.js`.
