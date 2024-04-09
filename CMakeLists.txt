cmake_minimum_required(VERSION 3.10)
project(GameAndWatchRetroGo)

set(CMAKE_CXX_STANDARD 11)

add_executable(my_app Core/Src/bilinear.c)
add_executable(my_app Core/Src/gw_buttons.c)
add_executable(my_app Core/Src/gw_flash.c)
add_executable(my_app Core/Src/gw_lcd.c)
add_executable(my_app Core/Src/main.c)
add_executable(my_app Core/Src/sha256.c)
add_executable(my_app Core/Src/flashapp.c)
add_executable(my_app Core/Src/bq24072.c)
add_executable(my_app Core/Src/porting/lib/lz4_depack.c)
add_executable(my_app Core/Src/porting/lib/lzma/LzmaDec.c)
add_executable(my_app Core/Src/porting/lib/lzma/lzma.c )
add_executable(my_app Core/Src/porting/common.c)
add_executable(my_app Core/Src/porting/odroid_audio.c)
add_executable(my_app Core/Src/porting/odroid_display.c)
add_executable(my_app Core/Src/porting/odroid_input.c)
add_executable(my_app Core/Src/porting/odroid_netplay.c)
add_executable(my_app Core/Src/porting/odroid_overlay.c)
add_executable(my_app Core/Src/porting/odroid_sdcard.c)
add_executable(my_app Core/Src/porting/odroid_system.c)
add_executable(my_app Core/Src/porting/crc32.c)
add_executable(my_app Core/Src/stm32h7xx_hal_msp.c)
add_executable(my_app Core/Src/stm32h7xx_it.c)
add_executable(my_app Core/Src/system_stm32h7xx.c)

# Specify the compiler (GCC in this case)
set(CMAKE_CXX_COMPILER g++)
# Add any necessary flags (optional)
# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra")

# Run 'make' after building the project
add_custom_target(run
    COMMAND make
    WORKING_DIRECTORY ${CMAKE_BINARY_DIR}
    COMMENT "Running make"
)
