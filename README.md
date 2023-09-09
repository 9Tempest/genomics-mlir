# genomics-mlir
The Genomics-MLIR project aims to provide a MLIR Dialect of genomics ops and a set of transformations, supporting scalable code-generation to heterogenous accelerators

## Building against a pre-built LLVM
If you have built llvm-project separately in the directory `$LLVM_INSTALL_DIR``, you can configure the project out-of-tree using the following command as template:
```bash
cmake -GNinja -Bbuild \
  -DCMAKE_BUILD_TYPE=Release \
  -DMLIR_DIR="$LLVM_INSTALL_DIR/lib/cmake/mlir/" \
   -DLLVM_ENABLE_ASSERTIONS=On \
  -DLLVM_TARGETS_TO_BUILD=host \
  .
```
Then run build commands to build the project
```bash
cmake --build build
```

## Testing
Under Development