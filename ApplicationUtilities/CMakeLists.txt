cmake_minimum_required(VERSION 3.1)
project(ApplicationUtilities LANGUAGES CXX)

include(${AVS_CMAKE_BUILD}/BuildDefaults.cmake)
cd /Users/username/my_project/build/
cmake/Users/username/my_project/source/avs-device-sdk \
-DGSTREAMER_MEDIA_PLAYER=ON \
-DCURL_LIBRARY=/usr/local/opt/curl-openssl/lib/libcurl.dylib \
-DCURL_INCLUDE_DIR=/usr/local/opt/curl-openssl/include \
-DPORTAUDIO=ON \
-DPORTAUDIO_LIB_PATH=/Users/me/pj/3p/portaudio/lib/.libs/libportaudio.a \
-DPORTAUDIO_INCLUDE_DIR=/Users/me/pj/3p/portaudio/include \
-DCMAKE_BUILD_TYPE=DEBUG

add_subdirectory("DefaultClient")
add_subdirectory("Resources")
add_subdirectory("SystemSoundPlayer")
add_subdirectory("SDKComponent")

if (ANDROID)
    add_subdirectory("AndroidUtilities")

endif()
