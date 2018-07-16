# Module `lerror.exceptions`
This module depends on `lobject`.  
The module provides a `.pcall` method to replace `lerror.pcall`, an Error `LuaError` and an Exception `LuaException`. Using the `lerror.exceptions.pcall` method, any Lua error will be converted into a `LuaException` and passed to the `try` function. You can throw/raise a `LuaError` or `LuaException` this ways:
```lua
-- Same applies to lerror.raise and LuaException
lerror.throw (LuaError:new {err="message"})
```
