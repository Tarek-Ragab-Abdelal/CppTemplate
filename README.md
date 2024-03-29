# C++ Project Template

This repo is just a blank C++ project template, featuring some CMake functionalities that eases the development process.

### Usage

- Clone the repo to you machine

```bash
git clone https://github.com/Tarek-Ragab-Abdelal/CppTemplate
```

- Build command
  - Can be done from the tool bar at VS Code using [CMake Tools](#Recommendations)

```bash
CppTemplate/ $ mkdir build
CppTemplate/ $ cd ./build
CppTemplate/build $ cmake ..
CppTemplate/build $ cmake --build .
```

- Run your app
  - Can be done from the tool bar at VS Code using [CMake Tools](#Recommendations)

```bash
CppTemplate/build $ ./debug/main.exe
```

### Project Structure

```
|- "CMakeLists.txt"
|
|--build (You need to build to see this)
| |- "main.exe"
|
|--include
| |- "config.h"
| |- "defaults.h"
|
|--lib
| |
| |--Boo
| | |--docs
| | |--examples
| | |--src
| | | |- "Boo.cpp"
| | | |- "Boo.h"
| |
| |--Foo
| | |- "Foo.cpp"
| | |- "Foo.h"
| |
|
|--src
| |- "main.cpp"
|
|--test
| |- "unit_test.cpp"
```

### Recommendations

- Use VS code and install this extension
  - [CMake Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools)
    - This will give you access to build and run your application in each of release an debug modes from the bottom bar in VS code.
      <br>![Cmake Tools from ToolBar at VS Code](/assets/cmake_toolbar.png)



      
### Support Me

<p style="display: inline-block; margin-right: 0.25rem;"><a style="padding: 10px;" href="https://www.buymeacoffee.com/tarekragab"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" width="150"/></a>
<a style="padding: 10px;" href="https://www.ko-fi.com/tarekragab"><img src="https://storage.ko-fi.com/cdn/kofi2.png?v=3" width="150"/></a></p>
