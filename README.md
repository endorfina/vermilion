# vermilion

### What's going on?

Hi. 👻
Vermilion is a bash utility I wrote to keep my tarballs fresh forever (mostly during distro hopping).

### OK. It's simple

```bash
$ git clone <url> <dir>
$ cd <dir>
$ vermilion add git
$ vermilion upgrade
```

vermilion keeps a record of stuff the user has added in `~/.config/vermilion_record`.
The main idea is that should we ever want to wipe the drive clean, we require only to copy this list file and run `vermilion prepare` on the new system in order to fetch all repos at once.

CMake builds automatically receive the `-march=native` flag, among others.

GNU make builds can populate environment variables as of now and this has to be done manually:

```bash
$ vermilion add make cflags CFLAGS cxxflags CXXFLAGS target all
```

This will basically populate CFLAGS and CXXFLAGS with the same flags that cmake receives, then it will call `make all`.

### All wrongs reserved

![GPLv3](https://www.gnu.org/graphics/gplv3-88x31.png)

