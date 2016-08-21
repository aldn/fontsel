cmake_minimum_required(VERSION 2.8.11)

set(APP fontsel)

project(${APP})

# generate Clang's CompilationDatabase system
set(CMAKE_EXPORT_COMPILE_COMMANDS 1)

# find includes in corresponding build directories
set(CMAKE_INCLUDE_CURRENT_DIR ON)

# run moc automatically when needed.
set(CMAKE_AUTOMOC ON)

find_package(Qt5Widgets)

add_executable(${APP}
   fontsel.cpp
)

target_link_libraries(${APP}
    Qt5::Widgets
)

