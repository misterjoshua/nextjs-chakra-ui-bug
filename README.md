# Bug Reproducer Project

To test the bug with this repo, type the following:

```
yarn install
yarn build
```

## Reproduce the underlying bug from scratch

```
yarn create next-app my-chakra-app
cd my-chakra-app
yarn set version berry
yarn config set nodeLinker pnp
yarn add @chakra-ui/react @emotion/react@^11 @emotion/styled@^11 framer-motion@^4
yarn install
```

Copy/paste the example from https://chakra-ui.com/docs/getting-started#nextjs into `pages/_app.tsx`

```
yarn build
```

Get this error:

```
info  - Checking validity of types
info  - Creating an optimized production build
Failed to compile.

ModuleNotFoundError: Module not found: Error: Can't resolve '@chakra-ui/react' in 'E:\p\my-chakra-app\pages'


> Build error occurred
Error: > Build failed because of webpack errors
    at E:\p\my-chakra-app\.yarn\__virtual__\next-virtual-884fbe2c0d\0\cache\next-npm-11.1.0-ba26540f3a-b74dfd738b.zip\node_modules\next\dist\build\index.js:390:19
    at async Span.traceAsyncFn (E:\p\my-chakra-app\.yarn\__virtual__\next-virtual-884fbe2c0d\0\cache\next-npm-11.1.0-ba26540f3a-b74dfd738b.zip\node_modules\next\dist\telemetry\trace\trace.js:60:20)
```
