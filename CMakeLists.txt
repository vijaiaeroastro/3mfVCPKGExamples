cmake_minimum_required(VERSION 3.27)
project(3mfExamples)

set(CMAKE_CXX_STANDARD 11)

# Find the package
find_package(lib3mf REQUIRED COMPONENTS Cpp)

# Include necessary definitions to add a texture path
add_definitions(-DTEXTURESPATH="${CMAKE_CURRENT_SOURCE_DIR}/Files/Textures/")

# Build all the examples
add_executable(Example_ColorCube Source/ColorCube.cpp)
target_link_libraries(Example_ColorCube lib3mf::lib3mf)
copy_lib3mf_libraries(Example_ColorCube)

add_executable(Example_Components Source/Components.cpp)
target_link_libraries(Example_Components lib3mf::lib3mf)
copy_lib3mf_libraries(Example_Components)

add_executable(Example_Converter Source/Converter.cpp)
target_link_libraries(Example_Converter lib3mf::lib3mf)
copy_lib3mf_libraries(Example_Converter)

add_executable(Example_Cube Source/Cube.cpp)
target_link_libraries(Example_Cube lib3mf::lib3mf)
copy_lib3mf_libraries(Example_Cube)

add_executable(Example_SecureCube Source/SecureCube.cpp)
target_link_libraries(Example_SecureCube lib3mf::lib3mf)
copy_lib3mf_libraries(Example_SecureCube)

add_executable(Example_ExtractInfo Source/ExtractInfo.cpp)
target_link_libraries(Example_ExtractInfo lib3mf::lib3mf)
copy_lib3mf_libraries(Example_ExtractInfo)

add_executable(Example_TextureCube Source/TextureCube.cpp)
target_link_libraries(Example_TextureCube lib3mf::lib3mf)
copy_lib3mf_libraries(Example_TextureCube)

add_executable(Example_Slice Source/Slice.cpp)
target_link_libraries(Example_Slice lib3mf::lib3mf)
copy_lib3mf_libraries(Example_Slice)

add_executable(Example_BeamLattice Source/BeamLattice.cpp)
target_link_libraries(Example_BeamLattice lib3mf::lib3mf)
copy_lib3mf_libraries(Example_BeamLattice)