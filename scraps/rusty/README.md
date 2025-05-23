```
[2c7acb4] [19:56:17] koom@t14 /home/koom/repos/koo5/yellow-scraps/0/yellow-scraps/scraps/rusty (master) 
 cargo run
   Compiling rusty_runtime_demo v0.1.0 (/home/koom/repos/koo5/yellow-scraps/0/yellow-scraps/scraps/rusty)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 16.65s
     Running `target/debug/rusty_runtime_demo`
Creating 3 separate JavaScript runtimes with isolated global state...

Runtime Runtime-A initialized
Runtime Runtime-B initialized
Runtime Runtime-C initialized

--- Demonstrating separate global state ---

Setting different counter values:
Runtime Runtime-A: counter set to 100
Runtime Runtime-B: counter set to 200
Runtime Runtime-C: counter set to 300

Incrementing Runtime-A 3 times:
Runtime Runtime-A: counter = 101
Runtime Runtime-A: counter = 102
Runtime Runtime-A: counter = 103

Incrementing Runtime-B 5 times:
Runtime Runtime-B: counter = 201
Runtime Runtime-B: counter = 202
Runtime Runtime-B: counter = 203
Runtime Runtime-B: counter = 204
Runtime Runtime-B: counter = 205

Incrementing Runtime-C 2 times:
Runtime Runtime-C: counter = 301
Runtime Runtime-C: counter = 302

--- Final State of Each Runtime ---
Runtime 1 state: {"name":"Runtime-A","counter":103}
Runtime 2 state: {"name":"Runtime-B","counter":205}
Runtime 3 state: {"name":"Runtime-C","counter":302}

Incrementing Runtime-A 3 times:
Runtime Runtime-A: counter = 104
Runtime Runtime-A: counter = 105
Runtime Runtime-A: counter = 106

Incrementing Runtime-B 5 times:
Runtime Runtime-B: counter = 206
Runtime Runtime-B: counter = 207
Runtime Runtime-B: counter = 208
Runtime Runtime-B: counter = 209
Runtime Runtime-B: counter = 210

Incrementing Runtime-C 2 times:
Runtime Runtime-C: counter = 303
Runtime Runtime-C: counter = 304

--- Final State of Each Runtime ---
Runtime 1 state: {"name":"Runtime-A","counter":106}
Runtime 2 state: {"name":"Runtime-B","counter":210}
Runtime 3 state: {"name":"Runtime-C","counter":304}

--- Demonstrating Independence ---
Incrementing only Runtime-A:
Runtime Runtime-A: counter = 107
After incrementing only Runtime-A:
Runtime 1 final: {"name":"Runtime-A","counter":107}
Runtime 2 final: {"name":"Runtime-B","counter":210}
Runtime 3 final: {"name":"Runtime-C","counter":304}

Demo complete! Each runtime maintained separate global state.
```