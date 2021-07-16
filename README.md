[Build raylib using make](https://github.com/raysan5/raylib/wiki/Working-on-GNU-Linux#build-raylib-using-make):
```shell
$ git clone https://github.com/raysan5/raylib.git
$ cd raylib/src/
$ make PLATFORM=PLATFORM_DESKTOP RAYLIB_LIBTYPE=SHARED
$ sudo make install RAYLIB_LIBTYPE=SHARED
```

Build examples
```shell
$ cd ../examples/
$ git clone https://github.com/corelight/cwrap
$ sed -Ei 's|^CC = gcc|CC = ./cwrap/cwrap.pl|' Makefile
$ sed -Ei "s|find . -type f|find . -type f ! -path './cwrap/*'|" Makefile
$ make BUILD_MODE=DEBUG
```
