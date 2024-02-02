cmake_minimum_required(VERSION 3.21)

include(pico_sdk_import.cmake)

project(beep_beep_rev)

pico_sdk_init()

add_executable(beep_beep_rev beep_beep_rev.c)

target_link_libraries(beep_beep_rev pico_multicore pico_stdlib hardware_spi hardware_sync pico_bootsel_via_double_reset)

pico_add_extra_outputs(beep_beep_rev)