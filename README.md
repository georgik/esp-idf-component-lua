# Lua - ESP-IDF Component

ESP-IDF componet which wrap Lua from upstream repository - https://www.lua.org/

Version of Lua submodule: 5.4.7

Check our version tag for specific version of Lua.

This is not Lua REPL. This component is suitable for embedding Lua code inside another ESP-IDF application. 
If you're seeking for interactive REPL, please check out the project: https://github.com/whitecatboard/Lua-RTOS-ESP32

## Example projects

- https://github.com/georgik/esp32-c3-lua-test
- https://github.com/georgik/esp32-sdl3-example

## Changes to upstream

This components overrides luaconf.h. 

Changing value of LUA\_32BITS from 0 to 1

```c
#define LUA_32BITS      1
```

