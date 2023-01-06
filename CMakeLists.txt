cmake_minimum_required(VERSION 3.12)

#incluimos el ambiente de desarrollo
include(pico_sdk_import.cmake)
#especificamos proyecto y compiladores C ,C++ y ASM (Solo usaremos C, pero se puede dejar asi)
project(matera C CXX ASM)
#inicializamos el entorno
pico_sdk_init()

#ESpecificamos cual v a ser el archivo ejecutable
add_executable(matera main.c)
pico_add_extra_outputs(matera)
#Agregamos librerias propias de raspberry pi pico
target_link_libraries(matera pico_stdlib pico_multicore)