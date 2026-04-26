## Overview
The project is a C application that renames and converts image files from one format to another. It uses custom libraries for sprite manipulation and image handling.

## Features
- Renaming of image files from `.png` and `.jpg` to `.sprg`.
- Conversion of sprite images to a custom binary format.
- Support for Linux, Windows (using Wine), WebAssembly, and cross-compilation for Windows on Linux.

## Project Structure

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed: `libpng`, `libjpeg`

## Build & Run
To build and run the project:

1. **Build for Linux**
   ```bash
   cd <Project>
   make -f Makefile.linux all
   ```

2. **Run the executable**
   ```bash
   ./build/Main
   ```

3. **Clean and rebuild**
   ```bash
   make -f Makefile.linux clean
   make -f Makefile.linux all
   ```

4. **Build for Windows (using Wine)**
   ```bash
   cd <Project>
   make -f Makefile.wine all
   ```
   
5. **Run the executable in Wine**
   ```bash
   WINEPREFIX=~/wine64 WINEARCH=win64 wine ./build/Main.exe
   ```

6. **Build for WebAssembly**
   ```bash
   cd <Project>
   make -f Makefile.web all
   ```
   
7. **Run the executable with wasmtime**
   ```bash
   wasmtime build/Main.wasm
   ```