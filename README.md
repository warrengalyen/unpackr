# unpackr

A work in progress command line utility to unpack various types of archives quickly.

```
unpackr /path/to/my/archive.zip
```

## Supported Formats

- unix ar archives
- microsoft cabinet
- portable executable containing microsoft cabinet
- zip archives
- uncompressed tarballs
- gzip-compressed tarballs
- xz-compressed tarballs
- bzip2-compressed tarballs
- gzip-compressed files
- xz-compressed files
- bzip2-compressed files

Note on cabinet files: this uses the [cab](https://crates.io/crates/cab) Rust library which
currently only supports deflate cabs.  This means it's unable to extract cabs which use
the LZX or Quantum compression formats.