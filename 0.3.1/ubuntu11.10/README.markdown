# Ubuntu Prebuilt Binaries for Luvit 0.3.1

Binaries come in both `i686` and `x86_64` for Ubuntu 11.10.  Within each there is a both types of builds.

## Luvit Bundled

The `luvit-bundled` build contains a single binary that can be run as-is.  All the luvit lua modules are embedded in the binary.  

This is useful if you don't want to keep track of a whole tree of files or just want to curl/wget down a binary and start running luvit scripts right away.

This is built using the gyp system by doing `./configure && make -C out`.

## Luvit Standard

The luvit.tar.gz file contains a `luvit` directory with `bin` and `lib/luvit` folders.  The modules are not embedded in the binary and must be at the correct distance relativly from the binary.

The advantage of this version is that you can modify or add built-in module very easily.  Also stack traces for built-in modules have line numbers.
