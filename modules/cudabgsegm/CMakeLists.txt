if(ANDROID OR IOS)
  ocv_module_disable(cudabgsegm)
endif()

set(the_description "CUDA-accelerated Background Segmentation")

ocv_warnings_disable(CMAKE_CXX_FLAGS /wd4127 /wd4324 /wd4512 -Wundef -Wmissing-declarations)

ocv_define_module(cudabgsegm opencv_video OPTIONAL opencv_legacy opencv_imgproc opencv_cudaarithm opencv_cudafilters opencv_cudaimgproc)
