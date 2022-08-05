# platter2

This is a fork of [platter](https://github.com/ryanisaacg/platter) with some upgrades and fixes.

Thanks, @ryanisaacg, for your hard work. 

--

A simple utility to serve you files on a `platter`

`platter2` works on both desktop and web, and returns a byte buffer of the file's contents.
On desktop, `load_file` is backed by native file system APIs. On web, it is backed by an
HTTP 'GET' request.

```rust
let file_contents = load_file("path_to_my_file").await?;
```

## Web Support

To use `platter2` on the web, enable either the `web-sys` feature (for `wasm-pack` and `wasm-bindgen` workflows) or the `stdweb` feature (for `stdweb` and `cargo-web` workflows).
