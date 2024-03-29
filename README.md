# C++ Project Template

This repo is just a blank C++ project template, featuring some CMake functionalities that eases the development process.

### Project Structure

```
|- CMakeLists.txt
|
|--build (You need to build to see this)
| |-main.exe
|
|--include
| |- config.h
| |- defaults.h
|
|--lib
| |
| |--Boo
| | |--docs
| | |--examples
| | |--src
| | | |- Boo.cpp
| | | |- Boo.h
| |
| |--Foo
| | |- Foo.cpp
| | |- Foo.h
| |
|
|--src
| | |- main.cpp
|
|--test
| | |- unit_test.cpp
```

### Recommendations

- Use VS code and install this extension {#CMAKE_TOOLS}
  - [CMake Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools)
    - This will give you access to build and run your application in each of release an debug modes from the bottom bar in VS code.
      ![Cmake Tools from ToolBar at VS Code](/assets/cmake_toolbar.png)

### Usage

- Clone the repo to you machine

```
git clone https://github.com/Tarek-Ragab-Abdelal/CppTemplate
```

- run build command (Can be done from the tool bar at VS Code using [CMake Tools](./#CMAKE_TOOLS))

```
CppTemplate/ $ mkdir build
CppTemplate/ $ cd ./build
CppTemplate/build $ cmake ..
CppTemplate/build $ cmake --build .
```

- run your app
  (Can be done from the tool bar at VS Code using [CMake Tools](./#CMAKE_TOOLS))

```
CppTemplate/build $ ./debug/main.exe
```
