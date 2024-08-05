# Common Lisp development flatpak

- SBCL
- CCL
- qlot (with quicklisp)

## Build and Install Instructions

Note that building requires network access to install quicklisp and qlot.

### Linting

``` shell
flatpak run --command=flatpak-builder-lint org.flatpak.Builder --exceptions manifest org.freedesktop.Sdk.Extension.sbcl.json
```

### Build and Install

``` shell
flatpak run org.flatpak.Builder --user --install --force-clean build-dir org.freedesktop.Sdk.Extension.sbcl.json
```

