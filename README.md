# chrome-extension-typescript

Spike to create a Google Chrome extension that is developed in TypeScript

## How did I achieve it?

First, I've used [@bricks/pacote-web](https://github.com/dart-pacotes/.bricks/tree/master/pacote_web) to generate a standalone Node.js program with support for hot reload. Then, I've reconfigured `tsconfig.json` to stop bundling in multiple files (remove `bundle` entry), as [browsers don't support `CommonJS` scripts](https://bobbyhadz.com/blog/typescript-uncaught-referenceerror-exports-is-not-defined). I've also remove generation of source-maps and `.d.ts` files, as I feel they are not needed for the context of Chrome Extensions.

Start scripts were also reconfigured to remove support for `swc` compilation, as the tool does not provide proper support for bundling files. As a final note, I've added the `clean-manifest.js` post build script, which removes the `$schema` entry from `manifest.json`, as Google Chrome reports a warning if it's present.

2023-06-09 13-28-00.mp4

## Scripts

- `npm run build` to transpile and bundle files in `.cjs`, `.js`, `.d.ts` and respective source-maps
- `npm run start` to run the project with hot-reload
- `npm run test` to run the unit tests
- `npm run lint` to analyze and lint the project
- `npm run format` to format the project based on lint feedback
- `npm run docs` to generate docs site
- `npm run docs:publish` to generate docs site and publish it to GitHub Pages

## Hooks

This repository is configured with client-side Git hooks that automatically format + lint the codebase before each push. You can install it by running the following command:

```bash
./hooks/INSTALL
```

---

### Contact

This template was prepared by:

- João Freitas, @freitzzz
- Rute Santos, @rutesantos4

Contact us for freelancing work!
