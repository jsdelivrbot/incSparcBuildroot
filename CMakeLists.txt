cmake_minimum_required(VERSION 3.5.1)

set (TOOLCHAIN_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../incSparcToolchain/bld/output")
get_filename_component(TOOLCHAIN_PATH ${TOOLCHAIN_PATH} ABSOLUTE)

set (KERNEL_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../incSparcKernel")
get_filename_component(KERNEL_PATH ${KERNEL_PATH} ABSOLUTE)

set (KERNEL_DEFCONFIG_PATH "${CMAKE_CURRENT_SOURCE_DIR}/configs/pearl6u_sparc_leon3_kernel_defconfig")

configure_file(${CMAKE_CURRENT_SOURCE_DIR}/configs/pearl6u_sparc_leon3_defconfig
               ${CMAKE_CURRENT_BINARY_DIR}/pearl6u_sparc_leon3_defconfig @ONLY)
