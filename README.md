# Cherry

A C++ based interpreter for the Cherry scripting language.

---

__What you need:__

* Visual Studio 2017 or Visual Studio 2019
* GCC (or Clang) 9.2 or earlier
  * We recommend using Pacman on [MSYS2](https://www.msys2.org/) to get GCC 9.2 or earlier then set it on your path to use from Git bash or Cmder or whatever terminal emulator you like the most.
  * We use some C++20 features (or are upgrading to) for better readability and performance as well as better const semantics. Of which `aggregate initializer names` are one of those features. We also plan to use the `3-way comparison operator` to speed up production. If possible we will also use concepts, but in all likelihood we'll wait for the release of C++20 before using them.
  * If you're going to use GCC (or Clang) you set `unix` as your second argument.
* CMAKE 3.9 or earlier

__To build Cherry:__

* Clone the repository through HTTPS or SSH protocol.
* Run the build script with any combination of the following flags:
  * 'd' Specifies a debug build.
  * 'r' Specifies a release build.
  * 'o' Specifies a optimized debug build.
  * 'p' Specifies for the library to enable profiling. This is more of a debugging feature, so we recommend only enabling it in a debugging build.
  * 'b' Enables benchmark testing.
  * 't' Enables source testing.
  * 'q' Is used to ignore commonly annoying compiler warnings, usually ones that show up a lot.

For example a debug build with testing, profiling, and quiet compiling would have the flag sequence: `-dtpq` or potentially `-pqdt`. The order of the flags do not matter, just that they are followed initially by the `-` and that they are valid flags. The build script will not do anything with flags it doesn't know, it will simply continue to process all flags.
