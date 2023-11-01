# gcc, g++ & gdb on _Windows_

Steps for downloading and installing the _MinGW-w64_ *(Minimalist GNU for Windows)* toolset, which includes _gcc_, _g++_, and _gdb_. This toolset is essential for developing _C_ and _C++_ programs on *Windows 10* or *Windows 11* computers. The installation will be carried out using the _msys2_ Software Distribution and Building Platform.

## Download _MSYS2_
* [MSYS2](https://www.msys2.org/)
* Once you have downloaded and installed `MSYS2` launch it.

## Update _MSYS2 UCRT64_ Packages
* Update the package db and base packages using pacman: `pacman -Syu`

## Update _MSYS2 MSYS_
* Update the package db and base packages using pacman: `pacman -Su`

## Install _gcc_ using _MSYS2 MinGW 64-bit_
* Open MinGW 64-bit from the Windows menu. You can search for packages with name _gcc_ using: `pacman -Ss gcc`
* This will display all the packages for _gcc_. The one you are looking for (64-bit system) is: `pacman -S mingw-w64-x86_64-gcc` 

### Check to see if _gcc_ is successfully installed
```Shell
$ gcc --version
gcc.exe (Rev2, Built by MSYS2 project) 13.2.0
Copyright (C) 2023 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```
### Check to see if _g++_ is successfully installed
```
$ g++ --version
g++.exe (Rev2, Built by MSYS2 project) 13.2.0
Copyright (C) 2023 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```
## Install _gdb_ Debugger
* You can search for packages with name _gdb_ using: `pacman -Ss gdb`
* This will display all the packages for `gdb`. The one you are looking for (64-bit system) is:

`pacman -S mingw-w64-x86_64-gdb`

### Check to see _gdb_ version
```Shell
gdb --version
GNU gdb (GDB) 13.2
Copyright (C) 2023 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
```

## Set the Path environment variable once installation is complete
* You won't be able to run any of your _C_ and _C++_ programs from anywhere in your file system if you don't set the path environment variable.
* Naviage to the location we installed _MSYS2_ and _gcc_.
* It should be in the `C:\msys64\mingw64\bin`

* From the Windows menu, search for _Environment Variable_ and you should see "Edit the system environment variables" option.
* Open that option and click the Environment Variables button and select the _Path_ option in System variables;
* Then click edit and select new and add the path `C:\msys64\mingw64\bin` and click OK.


