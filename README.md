# OpenCV 4.1.1 - MinGW with opencv_contrib-4.1.1-modules

## Dependencies
- MinGW-x86_64-8.1.0-posix-seh-rt_v6-rev0
- Windows-10 64bit
- CMake-3.16.1

## Install
- Install mingw, cmake
- Set PATH for mingw

### cmake-gui
- Where is the source code: `[...]/opencv-4.1.1`, Where to build the binaries: `[...]/opencv_build/`
- Select configure `MinGW Makefiles`, `native Compiler`, `Compiler C: [...]\mingw64\bin\gcc.exe`, `Compiler C ++: [...]\mingw64\bin\g++.exe`

### OpenCV make config
- Check `WITH_OPENGL`
- Check `ENABLE_CXX11`
- Uncheck `WITH_IPP`
- Uncheck `ENABLE_PRECOMPILED_HEADERS`
- Set `OPENCV_EXTRA_MODULES_PATH` to `[...]opencv_contrib-4.1.1/modules`
- Set `VTK_DIR`
- Check `WITH_VTK`

### Build
```
cd opencv_build/
mingw32-make -j 8 
mingw32-make install
```

```
General configuration for OpenCV 4.1.1 =====================================
  Version control:               unknown

  Extra modules:
    Location (extra):            C:/Users/anton/Downloads/opencv_contrib-4.1.1/opencv_contrib-4.1.1/modules
    Version control (extra):     unknown

  Platform:
    Timestamp:                   2019-12-15T09:40:04Z
    Host:                        Windows 10.0.18362 AMD64
    CMake:                       3.16.1
    CMake generator:             MinGW Makefiles
    CMake build tool:            C:/mingw64/bin/mingw32-make.exe
    Configuration:               Release

  CPU/HW features:
    Baseline:                    SSE SSE2 SSE3
      requested:                 SSE3
    Dispatched code generation:  SSE4_1 SSE4_2 FP16 AVX AVX2
      requested:                 SSE4_1 SSE4_2 AVX FP16 AVX2 AVX512_SKX
      SSE4_1 (15 files):         + SSSE3 SSE4_1
      SSE4_2 (2 files):          + SSSE3 SSE4_1 POPCNT SSE4_2
      FP16 (1 files):            + SSSE3 SSE4_1 POPCNT SSE4_2 FP16 AVX
      AVX (5 files):             + SSSE3 SSE4_1 POPCNT SSE4_2 AVX
      AVX2 (29 files):           + SSSE3 SSE4_1 POPCNT SSE4_2 FP16 FMA3 AVX AVX2

  C/C++:
    Built as dynamic libs?:      YES
    C++ Compiler:                C:/mingw64/bin/g++.exe  (ver 4.8.1)
    C++ flags (Release):         -fsigned-char -W -Wall -Werror=return-type -Werror=non-virtual-dtor -Werror=address -Werror=sequence-point -Wformat -Werror=format-security -Wmissing-declarations -Wundef -Winit-self -Wpointer-arith -Wsign-promo -Wuninitialized -Winit-self -Wno-delete-non-virtual-dtor -Wno-comment -Wno-missing-field-initializers -fdiagnostics-show-option -Wno-long-long -fomit-frame-pointer -ffunction-sections -fdata-sections  -msse -msse2 -msse3 -fvisibility=hidden -fvisibility-inlines-hidden -O3 -DNDEBUG  -DNDEBUG
    C++ flags (Debug):           -fsigned-char -W -Wall -Werror=return-type -Werror=non-virtual-dtor -Werror=address -Werror=sequence-point -Wformat -Werror=format-security -Wmissing-declarations -Wundef -Winit-self -Wpointer-arith -Wsign-promo -Wuninitialized -Winit-self -Wno-delete-non-virtual-dtor -Wno-comment -Wno-missing-field-initializers -fdiagnostics-show-option -Wno-long-long -fomit-frame-pointer -ffunction-sections -fdata-sections  -msse -msse2 -msse3 -fvisibility=hidden -fvisibility-inlines-hidden -g  -O0 -DDEBUG -D_DEBUG
    C Compiler:                  C:/mingw64/bin/gcc.exe
    C flags (Release):           -fsigned-char -W -Wall -Werror=return-type -Werror=non-virtual-dtor -Werror=address -Werror=sequence-point -Wformat -Werror=format-security -Wmissing-declarations -Wmissing-prototypes -Wstrict-prototypes -Wundef -Winit-self -Wpointer-arith -Wuninitialized -Winit-self -Wno-comment -Wno-missing-field-initializers -fdiagnostics-show-option -Wno-long-long -fomit-frame-pointer -ffunction-sections -fdata-sections  -msse -msse2 -msse3 -fvisibility=hidden -O3 -DNDEBUG  -DNDEBUG
    C flags (Debug):             -fsigned-char -W -Wall -Werror=return-type -Werror=non-virtual-dtor -Werror=address -Werror=sequence-point -Wformat -Werror=format-security -Wmissing-declarations -Wmissing-prototypes -Wstrict-prototypes -Wundef -Winit-self -Wpointer-arith -Wuninitialized -Winit-self -Wno-comment -Wno-missing-field-initializers -fdiagnostics-show-option -Wno-long-long -fomit-frame-pointer -ffunction-sections -fdata-sections  -msse -msse2 -msse3 -fvisibility=hidden -g  -O0 -DDEBUG -D_DEBUG
    Linker flags (Release):      -Wl,--gc-sections  
    Linker flags (Debug):        -Wl,--gc-sections  
    ccache:                      NO
    Precompiled headers:         NO
    Extra dependencies:          opengl32 glu32
    3rdparty dependencies:

  OpenCV modules:
    To be built:                 aruco bgsegm bioinspired calib3d ccalib core datasets dnn dnn_objdetect dpm face features2d flann fuzzy gapi hfs highgui img_hash imgcodecs imgproc line_descriptor ml objdetect optflow phase_unwrapping photo plot quality reg rgbd saliency shape stereo stitching structured_light superres surface_matching text tracking ts video videoio videostab xfeatures2d ximgproc xobjdetect xphoto
    Disabled:                    world
    Disabled by dependency:      -
    Unavailable:                 cnn_3dobj cudaarithm cudabgsegm cudacodec cudafeatures2d cudafilters cudaimgproc cudalegacy cudaobjdetect cudaoptflow cudastereo cudawarping cudev cvv freetype hdf java js matlab ovis python2 python3 sfm viz
    Applications:                tests perf_tests apps
    Documentation:               NO
    Non-free algorithms:         NO

  Windows RT support:            NO

  GUI: 
    Win32 UI:                    YES
    OpenGL support:              YES (opengl32 glu32)
    VTK support:                 NO

  Media I/O: 
    ZLib:                        build (ver 1.2.11)
    JPEG:                        build-libjpeg-turbo (ver 2.0.2-62)
    WEBP:                        build (ver encoder: 0x020e)
    PNG:                         build (ver 1.6.37)
    TIFF:                        build (ver 42 - 4.0.10)
    JPEG 2000:                   build (ver 1.900.1)
    OpenEXR:                     build (ver 2.3.0)
    HDR:                         YES
    SUNRASTER:                   YES
    PXM:                         YES
    PFM:                         YES

  Video I/O:
    DC1394:                      NO
    FFMPEG:                      YES (prebuilt binaries)
      avcodec:                   YES (58.35.100)
      avformat:                  YES (58.20.100)
      avutil:                    YES (56.22.100)
      swscale:                   YES (5.3.100)
      avresample:                YES (4.0.0)
    GStreamer:                   NO
    DirectShow:                  YES

  Parallel framework:            none

  Trace:                         YES (built-in)

  Other third-party libraries:
    Lapack:                      NO
    Eigen:                       NO
    Custom HAL:                  NO
    Protobuf:                    build (3.5.1)

  OpenCL:                        YES (no extra features)
    Include path:                C:/Users/anton/Downloads/opencv-4.1.1/opencv-4.1.1/3rdparty/include/opencl/1.2
    Link libraries:              Dynamic load

  Python (for build):            NO

  Java:                          
    ant:                         NO
    JNI:                         NO
    Java wrappers:               NO
    Java tests:                  NO

  Install to:                    C:/Users/anton/Downloads/opencv-4.1.1/bb/install
-----------------------------------------------------------------
```

## Common Errors
### MinGW-w64 aviriff.h File comment error

`[...]\mingw64\x86_64-w64-mingw32\include\aviriff.h`

Add `/` to fix the comment.


### M_PI not found
Replace all `M_PI` constants with `CV_PI`

## Credits
Hints from: `https://blog.huihut.com/2018/07/31/CompiledOpenCVWithMinGW64/`
