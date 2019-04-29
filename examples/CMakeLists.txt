project(examples)

# Create the executable
add_executable(simple-extractor src/simple-extractor.cpp)
add_executable(test src/test.cpp)

# Link the static library from subproject1 using it's alias sub::lib1
# Link the header only library from subproject2 using it's alias sub::lib2
# This will cause the include directories for that target to be added to this project
target_link_libraries(simple-extractor
    gw2dattools
)

target_link_libraries(test
    gw2dattools
)
