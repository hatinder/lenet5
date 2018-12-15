mxnet ubuntu 18.04 build commands (testing in progress) \
cd src/apache-mxnet-src-1.3.1-incubating \
mkdir build \
mkdir build/Release \
cmake -DUSE_CUDA=0 -DUSE_OPENCV=1 -DUSE_BLAS=open -DUSE_LAPACK=1 ../../ \
make -j$(nproc) \
cd ../../docs/install/ \
./install

