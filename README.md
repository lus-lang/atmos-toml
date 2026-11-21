# toml

Reads and writes TOML 1.0, with dates and times as values of the standard library time module.

```lus nocheck
local toml = require("https://atmosp.here/2.0/toml.lus")

local config = toml.decode("[server]\nport = 8080\nstarted = 2026-07-02T09:15:00Z\n")
print(config.server.port)                    --> 8080
print(config.server.started:iso())           --> 2026-07-02T09:15:00Z
print(toml.encode({ name = "lus", tags = { "a", "b" } }))
```

The package requires Lus 2.0. It declares no permissions. It calls no `pledge` of its own, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `toml.lus`. Run `lus doc toml.lus` to print it.
