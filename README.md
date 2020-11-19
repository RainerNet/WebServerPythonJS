# Machine Decompiler

This is a work-in-progress cross-platform decompiler designed to work using
machine learning, rather than algorithmically, allowing users to train the
decompiler together to produce an always-updating product.

## Building from source

```bash
mkdir -p build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ../
cmake --build .
```

The client binary should be located in `build/client/md-client(.exe)`. The
server binary should be located in `build/server/md-server(.exe)`.

## Running the client

The default, community integration server credentials are as follows

```
communit