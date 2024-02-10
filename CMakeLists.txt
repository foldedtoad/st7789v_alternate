# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)

# Suppress "simple_bus_reg" on Pico boards as 
# all GPIO ports use the same register.
list(APPEND EXTRA_DTC_FLAGS "-Wno-simple_bus_reg")

set(BOARD_ROOT "${CMAKE_CURRENT_SOURCE_DIR}")

#set(BOARD nrf52840dk_nrf52840)
#set(SHIELD st7789v_alt_nrf52840)

set(BOARD rpi_pico_w)
set(SHIELD st7789v_alt_pico_w)

find_package(Zephyr)
project(st7789v_alt)

FILE(GLOB app_sources src/*.c)

target_sources(app PRIVATE ${app_sources})

# zephyr_compile_options(-save-temps)
