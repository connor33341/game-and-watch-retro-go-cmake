cmake_minimum_required(VERSION 3.10)
project(GameAndWatchRetroGo)

set(CMAKE_CXX_STANDARD 11)

add_executable(bilinear Core/Src/bilinear.c)
add_executable(gw_buttons Core/Src/gw_buttons.c)
add_executable(gw_flash Core/Src/gw_flash.c)
add_executable(gw_lcd Core/Src/gw_lcd.c)
add_executable(main Core/Src/main.c)
add_executable(sha256 Core/Src/sha256.c)
add_executable(flashapp Core/Src/flashapp.c)
add_executable(bq24072 Core/Src/bq24072.c)
add_executable(lz4_depack Core/Src/porting/lib/lz4_depack.c)
add_executable(LzmaDec Core/Src/porting/lib/lzma/LzmaDec.c)
add_executable(lzma Core/Src/porting/lib/lzma/lzma.c )
add_executable(common Core/Src/porting/common.c)
add_executable(odroid_audio Core/Src/porting/odroid_audio.c)
add_executable(odroid_display Core/Src/porting/odroid_display.c)
add_executable(odroid_input Core/Src/porting/odroid_input.c)
add_executable(odroid_netplay Core/Src/porting/odroid_netplay.c)
add_executable(odroid_overlay Core/Src/porting/odroid_overlay.c)
add_executable(odroid_sdcard Core/Src/porting/odroid_sdcard.c)
add_executable(odroid_system Core/Src/porting/odroid_system.c)
add_executable(crc32 Core/Src/porting/crc32.c)
add_executable(stm32h7xx_hal_msp Core/Src/stm32h7xx_hal_msp.c)
add_executable(stm32h7xx_it Core/Src/stm32h7xx_it.c)
add_executable(system_stm32h7xx Core/Src/system_stm32h7xx.c)
# Specify the compiler (GCC in this case)
set(CMAKE_CXX_COMPILER g++)
#add_subdirectory(./)
# Add any necessary flags (optional)
# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra")

# Run 'make' after building the project
add_custom_target(run
    COMMAND make
    WORKING_DIRECTORY ${CMAKE_BINARY_DIR}
    COMMENT "Running make"
)
