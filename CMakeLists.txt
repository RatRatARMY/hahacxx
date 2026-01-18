cmake_minimum_required(VERSION 4.1)
project(hahacxx)

set(CMAKE_CXX_STANDARD 26)
add_subdirectory(vendor/SDL EXCLUDE_FROM_ALL)
add_subdirectory(vendor/SDL_image EXCLUDE_FROM_ALL)
add_subdirectory(vendor/SDL_ttf EXCLUDE_FROM_ALL)
add_executable(hahacxx main.cpp)
target_link_libraries(hahacxx PRIVATE
        SDL3::SDL3
        SDL3_image::SDL3_image
        SDL3_ttf::SDL3_ttf
)
