# lua-msvc

## Sample Makefile for NMake

This repository contains a Makefile to use with _Microsoft Visual Studio_ (or Command Line Tools) for building dynamically linked Lua on Windows. The Makefile must be used from a __preconfigured Command Prompt__ (like one installed with the Command Line Tools for Visual C++).

## Example of basic usage (for Lua 5.3.5):

Extract lua-5.3.5.tar.gz to lua-5.3.5 and change to that directory. Next, you have two options. The simplest, if you have Git installed, is to execute `git clone https://github.com/vtudorache/lua-msvc.git msvc` at the command prompt. The other is to create a subdirectory named, let's say, `msvc` (it can have any name). 
The created (or cloned) directory has two subdirectories, `static` and `dynamic`, according to the link type. From each subdirectory you can execute:

`nmake install`

at the command prompt. This will install Lua to `C:\Lua53` as defined in the Makefile.

## Advanced usage:

You can make an independent build directory and copy there the Makefile from the `static` or `dynamic` subdirectory. Then from the build directory, execute:

`nmake install INSTALL_ROOT=%PATH_TO_INSTALL_ROOT% SOURCE_ROOT=%PATH_TO_SOURCE_ROOT%`

where the variable `%PATH_TO_SOURCE_ROOT%` must contain the path to a valid Lua source tree (containing a `src` directory) and `%PATH_TO_INSTALL_ROOT%` is the desired path for the installed programs.


