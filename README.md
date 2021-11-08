binaries for building/checking mdbook in CI

built with:

```
git clone -b anchors https://github.com/ankitects/mdbook-linkcheck.git
cd mdbook-linkcheck && cargo build --release
cp target/release/mdbook-linkcheck ~/out
cd ..
git clone https://github.com/abdnh/mdbook
cd mdBook
git checkout arabic-search
cargo build --release
cp target/release/mdbook ~/out
cd ~
curl -L -o mdbook-toc.tgz https://github.com/badboy/mdbook-toc/releases/download/0.7.0/mdbook-toc-0.7.0-x86_64-unknown-linux-gnu.tar.gz
cd out && tar xzf ../mdbook-toc.tgz
```

The mdBook binary is built from https://github.com/abdnh/mdbook/tree/arabic-search to support Arabic search.
