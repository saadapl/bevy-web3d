# How to build & run as an app

Use command: `cargo run` in root folder

# How to build & run for web

1. Run command `rustup target add wasm32-unknown-unknown` in terminal.
2. Run command `cargo install -f wasm-bindgen-cli` in terminal.
1. Go to project folder
2. Run command `cargo build --release --target wasm32-unknown-unknown`
3. Run command `wasm-bindgen --out-dir ./out/ --target web ./target/wasm32-unknown-unknown/release/bevy-web3d.wasm`, this will generate a folder named `out` in your project folder
4. Make a new folder named `web`
5. Move the generated folder `out` into the `web` folder
6. Copy your `assets` folder if any into the `web` folder
7. Go to `web` folder and run command `npx serve`