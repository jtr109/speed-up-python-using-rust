# Speed up your Python using Rust - Red Hat Developer

## Tips

* Don't forget to set `~/.cargo/config` as below if you use macOS.
* The `*.dylib` settle in `target/debug` if you calling `cargo build` without `--release`

## Config Example

```config
[target.x86_64-apple-darwin]
# compilation in macOS
# reference: https://crates.io/crates/cpython
rustflags = [
  "-C", "link-arg=-undefined",
  "-C", "link-arg=dynamic_lookup",
]
```

## Reference

https://developers.redhat.com/blog/2017/11/16/speed-python-using-rust/
