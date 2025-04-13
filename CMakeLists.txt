cmake_minimum_required(VERSION 3.14)
project(MyWxApp)

set(CMAKE_CXX_STANDARD 17)

# Automatically find wxWidgets using wx-config
find_package(wxWidgets REQUIRED COMPONENTS core base)

# Include wxWidgets settings
include(${wxWidgets_USE_FILE})

# Add your executable
add_executable(MyWxApp main.cpp)  # Add more source files here as needed

# Link wxWidgets libraries
target_link_libraries(MyWxApp ${wxWidgets_LIBRARIES})
