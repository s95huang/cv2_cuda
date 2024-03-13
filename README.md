# cv2_cuda
Build CV2 4.5.5 with CUDA for ros1/2

GPU: 3080,3090 on Ubuntu 20 with CUDA 11.6 with CV2 contrib 


* Note: python libs are attached to the default python3.8

For details, please refer to https://github.com/s95huang/Yolov8TensorrtRos
Only the final build script is added here.

```
cmake -D CMAKE_BUILD_TYPE=RELEASE \
        -D CMAKE_CXX_FLAGS_RELEASE="-O3" \
        -D CMAKE_INSTALL_PREFIX=/usr/local \
        -D OPENCV_EXTRA_MODULES_PATH=$PWD/../../opencv_contrib-4.5.5/modules \
        -D BUILD_TIFF=ON \
        -D WITH_GSTREAMER=ON \
        -D WITH_TBB=ON \
        -D BUILD_TBB=ON \
        -D WITH_EIGEN=ON \
        -D WITH_V4L=ON \
        -D WITH_LIBV4L=ON \
        -D WITH_VTK=OFF \
        -D WITH_OPENGL=ON \
        -D WITH_OPENCL=ON \
        -D WITH_LAPACK=ON \
        -D BUILD_WEBP=OFF \
        -D OpenBLAS_INCLUDE_DIR=/usr/include/openblas \
        -D OpenBLAS_LIB=/usr/lib/x86_64-linux-gnu/libopenblas.so \
        -D Atlas_CLAPACK_INCLUDE_DIR=/usr/include/x86_64-linux-gnu/atlas \
        -D Atlas_INCLUDE_DIR=/usr/include/x86_64-linux-gnu/atlas \
        -D Atlas_LIB_DIR=/usr/lib/x86_64-linux-gnu \
        -D Atlas_CBLAS_LIBRARY=/usr/lib/x86_64-linux-gnu/libcblas.so \
        -D Atlas_BLAS_LIBRARY=/usr/lib/x86_64-linux-gnu/libatlas.so \
        -D OPENCV_ENABLE_NONFREE=ON \
        -D INSTALL_C_EXAMPLES=OFF \
        -D PYTHON3_EXECUTABLE=/usr/bin/python3 \
        -D PYTHON_INCLUDE_DIR=/usr/include/python3.8 \
        -D PYTHON_LIBRARY=/usr/lib/x86_64-linux-gnu/libpython3.8.so \
        -D PYTHON3_NUMPY_INCLUDE_DIRS=/usr/lib/python3/dist-packages/numpy/core/include/ \
        -D BUILD_OPENCV_PYTHON3=ON \
        -D INSTALL_PYTHON_EXAMPLES=ON \
        -D BUILD_NEW_PYTHON_SUPPORT=ON \
        -D OPENCV_GENERATE_PKGCONFIG=ON \
        -D BUILD_TESTS=OFF \
        -D BUILD_EXAMPLES=OFF \
        -D BUILD_PERF_TESTS=OFF \
        -D WITH_CUDA=ON \
        -D ENABLE_FAST_MATH=ON \
        -D CUDA_FAST_MATH=ON \
        -D WITH_CUDNN=ON \
        -D OPENCV_DNN_CUDA=ON \
        -D CUDA_ARCH_BIN=8.6 \
        -D CUDA_ARCH_PTX=8.6 \
        -D WITH_CUBLAS=ON ..

```
