file(GLOB CtsApplicationSources RELATIVE ${CMAKE_CURRENT_SOURCE_DIR}
    src/*.cpp
    src/gui/*.cpp
)

file(GLOB CtsApplicationHeaders RELATIVE ${CMAKE_CURRENT_SOURCE_DIR}
    src/*.h
    src/gui/*.h
)


# Define an executable
add_executable(CityTrafficSimulator++ ${CtsApplicationHeaders} ${CtsApplicationSources})
include_directories(src)
include_directories(${CtsGlobalIncludeDirs})

# Define the libraries this project depends upon
target_link_libraries(CityTrafficSimulator++ cts-core Qt5::Widgets)