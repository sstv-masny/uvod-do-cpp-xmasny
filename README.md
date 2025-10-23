# Getting started (per-folder)

This repository contains multiple independent C++ exercises/projects organized into separate folders. Each folder is an independent small project and can be built and run on its own. This README explains how to start and run code separately by folder.

## How the repo is organized

- Each top-level folder contains one independent C++ task or example.
- Look inside a folder to find source files (e.g. `main.cpp`), a `CMakeLists.txt`, or a `Makefile`.
- If a folder already contains its own README, follow the instructions inside that folder.

## Common ways to build & run a single folder

Replace `folder_name` below with the actual folder you want to run.

1) Quick compile with g++ (single file or small projects)

```bash
cd folder_name
# single source file
g++ -std=c++17 -O2 -Wall -Wextra main.cpp -o main
./main

# or compile all .cpp files in that folder
g++ -std=c++17 -O2 -Wall -Wextra *.cpp -o app
./app
```

2) CMake-based projects (recommended if `CMakeLists.txt` exists)

```bash
cd folder_name
mkdir -p build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
cmake --build . --config Release
# run the produced binary (name depends on CMake target)
./my_executable
```

On Windows with Visual Studio: open the generated .sln or use "Open Folder" -> configure CMake in VS.

3) Makefile-based projects

```bash
cd folder_name
make
./app   # or whichever binary the Makefile builds
```

4) Visual Studio Code

- Open the folder in VS Code (File → Open Folder).
- Install the C/C++ extension (ms-vscode.cpptools).
- Use the VS Code Run/Debug pane or create a tasks.json/launch.json to build and run.

## Troubleshooting

- No `main.cpp` / entry point: open the folder and find which source file contains `int main()`.
- Missing dependencies or headers: check the folder README or any provided instructions; install any required libraries.
- Compile errors: enable more verbose output (remove -O2 / add -g) and fix warnings/errors reported by the compiler.

## Tips for maintainers

- Consider adding a README inside each folder with exact build/run commands for that task.
- Add simple Makefiles or CMakeLists.txt where possible so users can build consistently.
