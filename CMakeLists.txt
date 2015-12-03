cmake_minimum_required(VERSION 2.8.4)
project(stm32-template)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}")

# Change the stm-template_SOURCE_DIR variable after changing the project name on line 2
add_custom_target(stm32-build COMMAND make -C ${stm32-template_SOURCE_DIR}
        CLION_EXE_DIR=${PROJECT_BINARY_DIR})

# Change the stm-template_SOURCE_DIR variable after changing the project name on line 2
add_custom_target(stm32-upload COMMAND make -C ${stm32-template_SOURCE_DIR}
        CLION_EXE_DIR=${PROJECT_BINARY_DIR} program)
