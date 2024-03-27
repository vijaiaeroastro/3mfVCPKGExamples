3mfExamples (VCPKG Integration)
===============================

To use 3MF with VCPKG, It is quite simple.

First clone the repo with VCPKG integration (this is currently in my repo during the test phase).
If you already have official VCPKG clone, you can clone this to a different name like lib3mf-vcpkg or something like that

```
git clone --recurse-submodules https://github.com/vijaiaeroastro/vcpkg
cd vcpkg
```

If you are on Linux or Mac
```
./bootstrap-vcpkg.sh 
./vcpkg install lib3mf
```

If you are on Windows
```
.\bootstrap-vcpkg.bat 
.\vcpkg.exe install lib3mf
```

Once this process is done, you have lib3mf installed in VCPKG

Now if you are interested in using lib3mf in CMake, it is quite simple.
Create the build directory as usual (mkdir build or mkdir cmake-build-release or however you wish).


Instead of the following

```
cmake ..
```

Use

```
cmake .. -DCMAKE_TOOLCHAIN_FILE=/home/vijai/Code/vcpkg/scripts/buildsystems/vcpkg.cmake
```

In the above line, point to the same vcpkg.cmake from your VCPKG installation, If you are an existing VCPKG user, you should know how to do this
But lib3mf is still not part of the official VCPKG repo yet, so you should point to the toolchain file that you have just cloned as shown above

The rest works exactly as it does.
