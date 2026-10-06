# Security Policy

## Supported Versions

Only the latest tagged release is actively supported.

| Version | Supported |
| ------- | --------- |
| latest tag | Yes |
| older releases | No |

## Reporting a Vulnerability

Please **do not** open a public issue for security vulnerabilities. Report
them privately through [GitHub Security Advisories](https://github.com/argvus/argvus-wallpapers/security/advisories/new),
or contact the maintainers directly.

Please include the affected version/tag, package name, reproduction steps,
impact, and a suggested fix if available.

## Verifying published packages

Releases published in `argvus/packages` are GPG-signed. To verify a package:

```sh
gpg --verify argvus-wallpapers-<VERSION>-1-any.pkg.tar.zst.sig argvus-wallpapers-<VERSION>-1-any.pkg.tar.zst
```

## Scope

This project produces an Arch Linux package containing wallpaper assets. The
package checksum, release signature, and source archive URL are the relevant
packaging security controls.
