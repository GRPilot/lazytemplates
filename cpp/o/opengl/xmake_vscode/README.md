# OpenGL template for Visual Studio Code with xmake build system

## Project's structure:
The project has the following structure:

```
root
│ .gitignore
│ xmake.lua              | build script
│
├─vscode/
│  compile_commands.json | for intellisense
│  c_cpp_properties.json | for intellisense
│  launch.json           | debugging by F5
│  settings.json
│  tasks.json            | tasks for build & install
│
├─bin/
│ │ opengl-xmake.exe     | executable
│ └─res/                 | resources
│   └─textures/
│      marble.jpg
│      texture_error.jpg
│
└─src/
  │ deps.h
  │ main.cpp
  ├─mash/
  │  mash.cpp
  │  mash.h
  │  vertex.cpp
  │  vertex.h
  ├─model/
  │  model.cpp
  │  model.h
  ├─renderer/
  │  renderer.cpp
  │  renderer.h
  │  render_context.cpp
  │  render_context.h
  │  render_object.h
  ├─shader/
  │  shader.cpp
  │  shader.h
  ├─texture/
  │  stb_image.cpp
  │  texture.cpp
  │  texture.h
  └─window/
     window.cpp
     window.h
```
If you have some troubles with intellisense, just run this command in the project's root:
```bash
> xmake project -k compile_commands
```
and move the *compile_commands.json* file into *.vscode*

## Build, Run and Debugging:
For building you have to run a consonant task in vscode or run the following command in the project's root directory:
```bash
> xmake build
```

For installing executable into *bin* directory for debugging or running, you also can use vscode task or command:
```bash
> xmake install
```

If you want to build, install and run debugger, you can press F5. Don't forget to put the breakpoints
