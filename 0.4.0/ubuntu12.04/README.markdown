# Ubuntu Prebuilt Binaries for Luvit 0.4.0

Binaries come in both `i686` and `x86_64` for Ubuntu 12.04.  Within each there is a both types of builds.

Also these files are mirrored at the luvit.io website prefixed with `/dist` instead of `luvit-releases`.  For example, to wget a luvit binary for the latest luvit release for the latest ubuntu version, use:

```bash
wget http://luvit.io/dist/latest/ubuntu-latest/`uname -m`/luvit-bundled/luvit
```

The `uname -m` will be `i686` or `x86_64` depending on if your machine is 64 or 32 bit.

## Luvit Bundled

The `luvit-bundled` build contains a single binary that can be run as-is.  All the luvit lua modules are embedded in the binary.  

This is useful if you don't want to keep track of a whole tree of files or just want to curl/wget down a binary and start running luvit scripts right away.

This is built using the gyp system by doing `./configure && make -C out`.

## Luvit Standard

The luvit.tar.gz file contains a `luvit` directory with `bin` and `lib/luvit` folders.  The modules are not embedded in the binary and must be at the correct distance relativly from the binary.

The advantage of this version is that you can modify or add built-in module very easily.  Also stack traces for built-in modules have line numbers.
