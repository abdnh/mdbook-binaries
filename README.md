binaries for building/checking mdbook in CI

built with:

```
git clone -b anchors https://github.com/ankitects/mdbook-linkcheck.git
cd mdbook-linkcheck && cargo build --release
cargo install mdbook --version 0.4.10
cp target/release/mdbook-linkcheck ~/.cargo/bin/mdbook ~/out
cd ~
curl -L -o mdbook-toc.tgz https://github.com/badboy/mdbook-toc/releases/download/0.7.0/mdbook-toc-0.7.0-x86_64-unknown-linux-gnu.tar.gz
cd out && tar xzf ../mdbook-toc.tgz
```
