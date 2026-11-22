# toml

`toml` reads and writes TOML 1.0, with offset date times as values of the standard library `time` module.

The following example reads a server configuration, then writes the settings of a blog.

```lus nocheck
local toml = require("https://atmosp.here/2.0/toml.lus")

local config = toml.decode("[server]\nport = 8080\nstarted = 2026-07-02T09:15:00Z\n")
print(config.server.port)                    --> 8080
print(config.server.started:iso())           --> 2026-07-02T09:15:00Z
print(toml.encode({ title = "Field notes", tags = { "travel", "food" } }))
```

The package requires Lus 2.0 and declares no permissions. It never calls `pledge`, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `toml.lus`, which `lus doc toml.lus` prints.
