# Source and build information

DshOffice 26.8.2.2 is built from the LibreOffice 26.8.2.2 source release:

- https://download.documentfoundation.org/libreoffice/src/26.8.2.2/
- https://git.libreoffice.org/core

## Build environment

- Windows x64
- Cygwin 64
- Visual Studio 2022 Build Tools (MSVC 14.44)
- LLVM 19.1.7 clang-cl (required by Skia)
- CMake 4.x, Ninja, NASM 2.16

Configure options (see `patches/autogen.input`):

```
--with-product-name=DshOffice
--with-branding=<branding directory>
--with-lang=zh-CN
--enable-release-build
--disable-skia=no          # Skia enabled (required on Windows)
--disable-pdfium
--without-java
--disable-gpgmepp
--disable-firebird-sdbc
```

## Modified source files

The full modified files are in `patches/`:

- `autogen.input`
- `ExternalProject_openssl.mk` (`/O2` → `/O1` to avoid an MSVC ICE)
- `ExternalProject_curl.mk` (disable docs/examples build)
- `jconfigint.h` (define `HIDDEN` for MSVC)
- `configure.ac` (use a standalone CMake)
- `branding/` (DshOffice logo / splash assets)

## Post-build changes

Applied to the installed tree after `make`:

- UI strings: `LibreOffice` → `DshOffice` in `.ui` files
- `ShowDonation = false` (profile + `main.xcd` default)
- update URLs cleared (`program/version.ini`)
- `InfoURL` / `VolunteerURL` → https://github.com/Link-h1j
- custom icons under `icons/`
- readme rewritten

## License

MPL 2.0 — see `LICENSE`. MPL headers and LICENSE/CREDITS files inside the
binary distribution are retained as required by the license.
