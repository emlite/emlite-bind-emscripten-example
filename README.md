# emlite-bind-example

This is an example repo showing the usage of emlite-bind in a node project targeting the browser. It uses webpack to bundle the necessary dependencies (emlite and @bjorn3/browser_wasi_shim).

If you don't have the wasm32-wasip1 target, you can run `rustup target add wasm32-wasip1`.

To build:
```bash
# after cloning and cd'ing into the repo
npm i
npm run cargo # runs cargo build --target=wasm32-wasip1
npm run pack # runs webpack
npm run serve # runs http-server on the dist directory
```

To target wasm32-uknown-unknown, remove the @bjorn3/browser_wasi_shim from you package.json, and any references to it in the src/index.js file.