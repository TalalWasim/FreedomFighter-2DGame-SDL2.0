# FreedomFighter
A top down shooting game in C++ using SDL2.0 library. This project was done as part of the "Object-Oriented Programming and Design Methodologies" during the third semester of the undergraduate program at Habib University.

## Project Build Properties
The following build properties need to be set in order to compile the code. Note that the code was originally built in VS2015 and hence some additional properties need to be set to ensure compatibility with VS2017. These properties apply to both configurations (Debug and Release). Any differences in terms of platform specific requirements (Win32 vs x64) are mentioned below.

### Go to Project &rarr Project Properties
1. Select C/C++ &rarr General &rarr set property "additional include directories"
  * Add the following paths:
    * ..\..\SDL2_mixer\include
    * ..\..\SDL2_image\include
    * ..\..\SDL2\include
2. Select C/C++ &rarr Language &rarr set property "Conformance mode" to **No**
3. Select C/C++ &rarr Precompiled Headers &rarr set property "Precompiled Header" to **Not Using Precompiled Headers**
4. Select Linker &rarr General &rarr set property "Additional Library Dependencies"
  * Add the following paths. If using platform Win32:
    * ..\..\SDL2_mixer\lib\x86
    * ..\..\SDL2_image\lib\x86
    * ..\..\SDL2\lib\x86
  * Add the following paths. If using platform x64:
    * ..\..\SDL2_mixer\lib\x64
    * ..\..\SDL2_image\lib\x64
    * ..\..\SDL2\lib\x64
5. Select Linker &rarr Input &rarr set property "Additional Dependencies"
  * Add the following names:
    * SDL2.lib
    * SDL2main.lib
    * SDL2_image.lib
    * SDL2_mixer.lib

## Project Runtime Settings
1. Go to the repository folder "RuntimeLibraries"
  * Inside there are two folders x86 and x64 containing the Win32 and x64 runtime libraries respectively.
  * These need to copied to the "Code_Windows_VisualStudio2017\FreedomFighter\FreedomFighter" directory, depending on which platfrom (Win32 or x64) is being used.
