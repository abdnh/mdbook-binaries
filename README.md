binaries for building/checking mdbook in CI

built with:

```
git clone -b anchors https://github.com/ankitects/mdbook-linkcheck.git
cd mdbook-linkcheck && cargo build --release
cargo install mdbook --version 0.4.10
cp target/release/mdbook-linkcheck ~/.cargo/bin/mdbook ~/out
```
