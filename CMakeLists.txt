cmake_minimum_required(VERSION 3.12) # Cmake must be on version 3.12 or above to proceed.
project(libpacreader VERSION 0.0.16) # Start the project.

set(CMAKE_C_STANDARD 99) # C99 is required.
set(CMAKE_C_STANDARD_REQUIRED ON)

FILE(GLOB SOURCES src/*.c) # Get all the files from the src directory.

add_executable(libpacreader ${SOURCES}) # Create the library.

install(TARGETS libpacreader DESTINATION /usr/local/bin) # Put the library in the bin folder.

target_include_directories(libpacreader PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/headers) # Get the files in the header directory as well.
