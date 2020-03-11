# lua-msvc

## Sample Makefile for NMake

This repository contains a Makefile to use with _Microsoft Visual Studio_ (or Command Line Tools) for statically building Lua on Windows. The Makefile must be used from a __preconfigured Command Prompt__ (like one installed with the Command Line Tools for Visual C++).

## Example of basic usage (for Lua 5.3.5):

Extract lua-5.3.5.tar.gz to lua-5.3.5 and change to that directory. Next, you have two options. The simplest, if you have Git installed, is to execute `git clone https://github.com/vtudorache/lua-msvc.git msvc` at the command prompt. The other is to create a subdirectory named, let's say, `msvc` (it can have any name), then change to the created directory (`msvc` in this example) and then copy Makefile here. Then execute:

`nmake install`

at the command prompt. This will install Lua to `C:\Lua53` as defined in the Makefile.

## Advanced usage:

You can make an independent build directory and copy there the Makefile. Then from that directory, execute:

`nmake install INSTALL_ROOT=%PATH_TO_INSTALL_ROOT% SOURCE_ROOT=%PATH_TO_SOURCE_ROOT%`

where the variable `%PATH_TO_SOURCE_ROOT%` must contain the path to a valid Lua source tree (containing a `src` directory) and `%PATH_TO_INSTALL_ROOT%` is the desired path for the installed programs.

Options to build Lua library as DLL will be added in the future.

