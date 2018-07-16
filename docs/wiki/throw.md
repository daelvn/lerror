# `lerror.throw (Exception e)`
# `lerror.throw (Error e)`
Throws an Error or an Exception.  
`e`. Has to be an Exception or Error `lobject` instance. It will call `e.thrown (e)` in the case of an Exception, but not an Error. Every thrown Exception can be caught with the `All` catch. This function will call error with the following parameters:
```lua
-- For Exceptions
{
  lerror = true,
  mode   = "throw",
  kind   = "exception",
  e      = e
}
-- For Errors
{
  lerror = true,
  error  = true
}
```
