svg_to_ico
==========

[![Travis Build Status](https://www.travis-ci.org/WrinklyNinja/svg_to_ico.svg?branch=master)](https://www.travis-ci.org/WrinklyNinja/svg_to_ico)
[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/WrinklyNinja/svg_to_ico?branch=master&svg=true)](https://ci.appveyor.com/project/WrinklyNinja/svg_to_ico)
[![dependency status](https://deps.rs/repo/github/WrinklyNinja/svg_to_ico/status.svg)](https://deps.rs/repo/github/WrinklyNinja/svg_to_ico)

This is a small cross-platform CLI utility to convert SVG icons into Windows ICO files. SVG images
are parsed and rasterised using
[Nano SVG](https://github.com/memononen/nanosvg), which is restricted to rendering
flat filled shapes.

## Build

To build svg_to_ico, install [Rust](https://www.rust-lang.org) then run

```
cargo build --release
```

to create a release executable at `target/release/svg_to_ico` (`svg_to_ico.exe` on Windows).

## Usage

### CLI

See the output of `./svg_to_ico -h` for a description of the CLI parameters. You can specify the
input SVG path, output ICO path, the DPI to interpret the SVG with, and the image sizes that should
be included in the ICO.

Example:

```
./svg_to_ico -i icon.svg -o icon.ico
```

### Library

You can also use svg_to_ico as a Rust library, just add it to your `Cargo.toml`:

```
[dependencies]
svg_to_ico = "0.1"
```

then use it as shown in the [example](examples/library.rs).
