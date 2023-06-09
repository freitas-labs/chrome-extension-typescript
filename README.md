# chrome-extension-typescript

Spike to create a Google Chrome extension that is developed in TypeScript

- pacote web to generate
- remove module es6
- target still es6
- remove d.ts and map gen
- 

## Scripts

- `npm run build` to transpile and bundle files in `.cjs`, `.js`, `.d.ts` and respective source-maps
- `npm run start` to run the project with `swc` compilation

- `npm run start:hot` to run the project with hot-reload enabled

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
