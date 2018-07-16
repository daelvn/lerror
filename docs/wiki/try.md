# `lerror.try`
This function is used to call a list of functions, with several handles for every caught exception.
```lua
lerror.try {
  foo,
  bar,
  baz
} {
  LuaException = function () ... end,
  IOError      = function () ... end
}
```
Optionally, the `All` handle will catch any thrown exceptions, regardless of type (raising them does not have the same effect).
