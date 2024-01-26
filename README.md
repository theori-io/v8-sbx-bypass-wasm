# V8 Sandbox Escape using WasmIndirectFunctionTable::targets

## Setup

```
$ Fetch v8 source code and depot_tools
$ git checkout f7a3499f6d7e50b227a17d2bbd96e4b59a261d3c
$ gclient sync
$ gn args out/x64.release
$ Edit 'args.gn'
$ autoninja -C out/x64.release
```

## args.gn

```
is_component_build = false
is_debug = false
target_cpu = "x64"
v8_enable_sandbox = true
use_goma = false
v8_enable_backtrace = true
v8_enable_disassembler = true
v8_enable_object_print = true
v8_enable_verify_heap = true
dcheck_always_on = false
v8_expose_memory_corruption_api = true
```