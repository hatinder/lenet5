mxnet ubuntu 18.04 build commands (testing completed. R-package built sucessfully from the master) \
cd incubator-mxnet \
mkdir build \
mkdir build/Release \
cmake -DUSE_CUDA=0 -DUSE_OPENCV=1 -DUSE_BLAS=open -DUSE_LAPACK=1 ../../ \
make -j$(nproc) \
cd ../../docs/install/ \
./install_mxnet_ubuntu_python.sh
./install_mxnet_ubuntu_r.sh
It failed on the master at first run with following error. \
* cp: cannot overwrite non-directory 'R-package/inst/include/dmlc' with directory '3rdparty/dmlc-core/include/dmlc' \
Makefile:583: recipe for target 'rpkg' failed

 But after I applied the changes in the fix #13590
it worked here is the last line.
* DONE (mxnet) \
Done! MXNet for R installation is complete. Go ahead and explore MXNet with R :-)


