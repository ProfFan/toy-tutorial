# An out-of-tree MLIR dialect

This is an example of an out-of-tree [MLIR](https://mlir.llvm.org/) project, using the Ch1 of the MLIR tutorial.

## Building

This setup assumes that you have built LLVM and MLIR in `$LLVM_BUILD_DIR` and installed them to `$LLVM_INSTALL_PREFIX`. To build, run
```sh
mkdir build && cd build
cmake -G Ninja .. -DMLIR_DIR=$LLVM_INSTALL_PREFIX/lib/cmake/mlir -DLLVM_EXTERNAL_LIT=$LLVM_BUILD_DIR/bin/llvm-lit
cmake --build .
```

**Note**: Make sure to pass `-DLLVM_INSTALL_UTILS=ON` when building LLVM with CMake in order to install `FileCheck` to the chosen installation prefix.

