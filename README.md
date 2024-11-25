# Lua - ESP-IDF Component

ESP-IDF componet which wrap Lua from upstream repository - https://www.lua.org/

This is version was built from Lua master branch which is under development!

Consider using 5.3 or 5.4 for stable versions.

This is not Lua REPL. This component is suitable for embedding Lua code inside another ESP-IDF application. 
If you're seeking for interactive REPL, please check out the project: https://github.com/whitecatboard/Lua-RTOS-ESP32

## Configuration option

- `LUA_MAXSTACK` - default value: 1000000 - Limits the size of the Lua stack.

Modify values:

```shell
idf.py menuconfig
```

## Example projects

- https://github.com/georgik/esp32-c3-lua-test
- https://github.com/georgik/esp32-sdl3-example

## Changes to upstream

This components overrides luaconf.h. 

Changing value of LUA\_32BITS from 0 to 1

```c
#define LUA_32BITS      1
```

