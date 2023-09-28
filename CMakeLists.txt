cmake_minimum_required(VERSION 3.0)

project(gstrtspserver)

add_definitions(-DHAVE_CONFIG_H)

set(CMAKE_C_COMPILER "/opt/openwrt_toolchain/arm-openwrt-icatchtek-glibc/bin/arm-openwrt-linux-gcc") 

set(BSP4_DIR "/home/wang.zhou/project/v57/gds/ES2/bsp4_glibc") 

set(STAGING_DIR "/home/wang.zhou/project/v57/gds/ES2/bsp4_glibc/staging_dir")

include_directories(./)

include_directories(${BSP4_DIR}/build_dir/target-arm-linux_glibc/gstreamer-1.12.4/)

include_directories(${STAGING_DIR}/target-arm-linux_glibc/usr/include/gstreamer-1.0)

include_directories(${STAGING_DIR}/target-arm-linux_glibc/usr/include/glib-2.0)

###
link_directories(${STAGING_DIR}/target-arm-linux_glibc/usr/lib)

link_directories(${STAGING_DIR}/target-arm-linux_glibc/usr/lib/libgstreamer-1.0)

link_directories(${STAGING_DIR}/target-arm-linux_glibc/root-icatchtek/usr/lib/gstreamer-1.0/)

link_directories(${STAGING_DIR}/target-arm-linux_glibc/usr/libglib-2.0)

link_libraries(
         glib-2.0
         gmodule-2.0
         gobject-2.0
         gstbase-1.0
         gstreamer-1.0
         gstrtsp-1.0
)

add_subdirectory(gst)
add_subdirectory(examples)
