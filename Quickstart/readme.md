# Example:
## conanfile.txt
https://docs.conan.io/2/tutorial/consuming_packages/build_simple_cmake_project.html

## Initial setup commands:
run after first install.
```
conan profile detect --force
```

## Project commands:
run in source code directory for a project.
```
conan install . --output-folder=build --build=missing
cd build
cmake .. -DCMAKE_TOOLCHAIN_FILE=conan_toolchain.cmake -DCMAKE_BUILD_TYPE=Release
cmake --build .

# Run app
./appname
```
