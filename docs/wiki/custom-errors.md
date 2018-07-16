# Writing custom Errors and Exceptions
For this, you will need `lobject` as a dependency.  
First of all, create a new class for the exception, or extend an already existing error or exception.
```lua
local SampleException = lobject.class "SampleException" (function () return {} end)
```
That should be enough, however, if you want to include custom information, you can include a builder:
```lua
local SampleException = lobject.class "SampleException" (function (argl)
  return {msg = argl.msg or ""}
end)
--
lerror.raise (SampleException:new {msg = "foo"})
```
