if(CMAKE_HOST_WIN32)
    set(libname "libconfig")
else()
    set(libname "config")
endif()

add_executable(c++_example1	example1.cpp )
add_executable(c++_example2	example2.cpp )
add_executable(c++_example3	example3.cpp )
add_executable(c++_example4	example4.cpp )

target_include_directories(c++_example1 PRIVATE ${CMAKE_SOURCE_DIR}/lib)
target_include_directories(c++_example2 PRIVATE ${CMAKE_SOURCE_DIR}/lib)
target_include_directories(c++_example3 PRIVATE ${CMAKE_SOURCE_DIR}/lib)
target_include_directories(c++_example4 PRIVATE ${CMAKE_SOURCE_DIR}/lib)

target_link_libraries(c++_example1 ${libname}++ )
target_link_libraries(c++_example2 ${libname}++ )
target_link_libraries(c++_example3 ${libname}++ )
target_link_libraries(c++_example4 ${libname}++ )
