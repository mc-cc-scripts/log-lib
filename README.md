# log-lib

A Library to ease logging of data

```lua
local log = require('./libs/log')
local filePath = './Output.lua'
local content = {
    key1 = 'value1',
    key2 = 'value2'
}
-- write into file:
log.write(content, filePath, "w+")

-- write into default error File, incl. traceback:
log.ErrorHandler(content, nil)
```

### write
Default dataAccess is `"w+"`
```lua
log.write(content: <table|string>, filePath: <string>, dataAccess: <string>)
DataAccess:
"w" | "w+" | "a" | "a+"
```

### ErrorHandler

```lua
log.ErrorHandler(content: <table|string>, filePath: <string|nil>, traceback: <boolean|nil>)
```
