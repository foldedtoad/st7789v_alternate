# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)

set(BOARD_ROOT "${CMAKE_CURRENT_SOURCE_DIR}")
set(BOARD nrf52840dk_nrf52840)
set(SHIELD st7789v_alternate)

find_package(Zephyr)
project(st7789v_alternate)

FILE(GLOB app_sources src/*.c)

target_sources(app PRIVATE ${app_sources})

# zephyr_compile_options(-save-temps)
