# FOS

FOS is a small 32-bit x86 educational operating system. It builds a bootable
disk image and runs it in Bochs.

## Build

From the project root, run:

```bash
make -j2
```

If your system does not have `i386-elf-gcc`, build with the host compiler:

```bash
make GCCPREFIX='' -j2
```

## Run

After the build finishes, start Bochs with:

```bash
bochs -q -f .bochsrc
```

## Clean

Remove build files with:

```bash
make clean
```

## Requirements

You need `make`, `gcc`, `binutils`, `perl`, and `bochs`.

On Fedora, install:

```bash
sudo dnf install gcc binutils make perl bochs glibc-devel.i686 libgcc.i686
```

On Ubuntu, install:

```bash
sudo apt install build-essential binutils perl bochs gcc-multilib libc6-dev-i386
```

## Project Layout

- `boot/` bootloader code
- `kern/` kernel code
- `lib/` shared support code
- `user/` user programs and tests
- `inc/` header files

## Notes

- The project is configured for SDL2 Bochs display in `.bochsrc`.
- If Bochs cannot open a window, run it from a local graphical desktop.
