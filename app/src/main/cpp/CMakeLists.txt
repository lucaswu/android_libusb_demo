
cmake_minimum_required(VERSION 3.22.1)


project("libusbdemo")

include_directories(libUSB/include)

add_library(${CMAKE_PROJECT_NAME} SHARED
        native-lib.cpp)


target_link_libraries(${CMAKE_PROJECT_NAME}
        # List libraries link to the target library
        android
        log
        ${CMAKE_SOURCE_DIR}/libs/${ANDROID_ABI}/libusb1.0.so )