# FOS

<h1 align="center">
<img src="https://i.postimg.cc/BnZmZZ0h/banar-OS.png" alt="Description of image" style="border-radius: 5px;">
</h1>

FOS is an educational operating system. It is a refactored version of [MIT Operating Systems Lab 6.828.](https://ocw.mit.edu/courses/6-828-operating-system-engineering-fall-2012/), adapted to help students learn operating system concepts through hands-on work.

# What is this project?

This project involves creating a fully functional operating system in C.

The project aims to develop a system that manages memory, schedules processes, and ensures protection for shared resources.

## Build

From the project root, run:

```bash
make -j2
```

If your system does not have `i386-elf-gcc`, use the host compiler instead:

```bash
make GCCPREFIX='' -j2
```

## Run

After the build finishes, run the system in Bochs:

```bash
bochs -q -f .bochsrc
```

## Clean

Remove all generated files with:

```bash
make clean
```
