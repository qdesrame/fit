# fit

[![license](http://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/qdesrame/fit/raw/master/LICENSE)
[![GoDoc](https://godoc.org/github.com/qdesrame/fit?status.svg)](https://godoc.org/github.com/qdesrame/fit)
[![Build](https://github.com/qdesrame/fit/workflows/Build/badge.svg)](https://github.com/qdesrame/fit/actions?query=workflow%3ABuild)

<img src="https://raw.githubusercontent.com/hackraft/gophericons/master/png/2.png" width="225" align="right" hspace="25" />

fit is a [Go](http://www.golang.org/) package that implements decoding and
encoding of the [Flexible and Interoperable Data Transfer (FIT)
Protocol](http://www.thisisant.com/resources/fit). Fit is a "compact binary
format designed for storing and sharing data from sport, fitness and health
devices". Fit files are created by newer GPS enabled Garmin sport watches and
cycling computers, such as the Forerunner/Edge/Fenix series.

The two latest versions of Go is supported. The core decoding package has no
external dependencies. The latest release of Go and a few external dependencies
are required for running the full test suite and benchmarks.

**Latest release:** 0.14.0

### Version Support

The current supported FIT SDK version is **21.94**.

Developer data fields are currently only _partially_ supported.
At the moment the decoder parses Developer Data Field Descriptions, Developer Data ID Messages and Field Description Messages.
The decoder currently discards developer data fields found in records. 

The encoder will currently (silently) ignore anything related to Developer data fields,
This also means that encoding will not fail if protocol version 2 is specified for a file header.

Developer data fields support is tracked by
[#21](https://github.com/qdesrame/fit/issues/21)
and
[#64](https://github.com/qdesrame/fit/issues/64).

### Features

* Supports all FIT file types.
* Accessors for scaled fields.
* Accessors for dynamic fields.
* Field components expansion.
* Go code generation for custom FIT product profiles.

### Installation

Using Go modules:

```
$ go get github.com/qdesrame/fit@v0.14.0
```

Using `$GOPATH`:

```
$ go get github.com/qdesrame/fit
```

### About fit

- [Example Usage](https://github.com/qdesrame/fit/wiki/Example-Usage)
- [Data Types](https://github.com/qdesrame/fit/wiki/Data-Types)
- [Main API Reference](https://github.com/qdesrame/fit/wiki/Main-Api-Reference)
- [Custom Product Profiles](https://github.com/qdesrame/fit/wiki/Custom-Product-Profiles)
- [Upcoming Features](https://github.com/qdesrame/fit/wiki/Upcoming-Features)
- [Contributing](https://github.com/qdesrame/fit/blob/master/CONTRIBUTING.md)
- [License](https://github.com/qdesrame/fit/wiki/License)

### Contributors

- [usedbytes](https://github.com/usedbytes)
- [colinrgodsey](https://github.com/colinrgodsey)
- [bpg](https://github.com/bpg)
- [pieterclaerhout](https://github.com/pieterclaerhout)
- [beyoung](https://github.com/beyoung)
