Double Glow Duel Color
=========
## A filter that does two things.

This filter requires your layer to have an alpha channel and to prevent color loss you are strongly recommended to apply this GEGL filter on a duplicate layer while fusing it with Gimp blend modes. GEGL's blending operations will work at the cost of color loss. Gimp's blend modes do not have this problem.

![image preview](glow.png)

## Duel Color

![image preview](duelcolor.png)

## Double Glow
![image preview](doubleglow.png)


## Compiling and Installing

### Linux

To compile and install you will need the GEGL header files (`libgegl-dev` on
Debian based distributions or `gegl` on Arch Linux) and meson (`meson` on
most distributions).

```bash
meson setup --buildtype=release build
ninja -C build
```

If you have an older version of gegl you may need to copy to `~/.local/share/gegl-0.3/plug-ins`
instead (on Ubuntu 18.04 for example).



### Windows

The easiest way to compile this project on Windows is by using msys2.  Download
and install it from here: https://www.msys2.org/

Open a msys2 terminal with `C:\msys64\mingw64.exe`.  Run the following to
install required build dependencies:

```bash
pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl
```

Then build the same way you would on Linux:

```bash
meson setup --buildtype=release build
ninja -C build
```



