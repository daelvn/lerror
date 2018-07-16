# `lerror.raise (Exception e)`
# `lerror.raise (Error e)`
Raises an Error or Exception.  
`e` has to be a `lobject` instance. `e.raised (e)` will always be called. In the case of Exceptions, the `All` catch will not catch the Exception. It will error with the following parameters:
```lua
-- For Exceptions
{
  lerror = true,
  mode   = "raise",
  kind   = "exception",
  e      = e
}
-- For Errors
{
  lerror = true,
  error  = true
}
```
