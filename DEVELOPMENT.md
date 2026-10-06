# Development

## Repository Structure

```
├── Makefile
├── README.md
├── CHANGELOG.md
├── LICENSE
├── packaging/
│   └── arch/
│       ├── local/          PKGBUILD for local development builds
│       ├── ci/             PKGBUILD for GitHub CI builds
│       └── common/         Shared packaging functions (Arch Linux)
├── src/
│   └── usr/share/argvus/svg/
│       ├── ARGVUS-logo.svg       Logotype mark
│       └── ARGVUS-wordmark.svg   Full wordmark
├── tools/
│   └── sh/                 Build and validation scripts
└── docs/
    ├── en/                 English documentation
    └── pt-br/              Brazilian Portuguese documentation
```

## Building

```bash
make build
```

The package is built into `build/dist/`.

## Validation

```bash
make validate
```

Runs PKGBUILD validation and shell script checks.

## Installation

```bash
make install
```

Installs the locally-built package via `pacman -U`.

## Contributing

See CONTRIBUTING.md.
