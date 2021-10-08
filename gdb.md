## Breakpoints
* break ... - set breakpoint
* tbreak (tb) ... - set one-time breakpoint
* clear ... / del $BP_NUM - remove breakpoint
* info break - list breakpoints
* condition (cond) $BP_NUM x==42 - only break if condition is fullfilled
* break ... if x==42 - short form of above

## Watchpoints
* watch x - break when x changes value
* watch (x > 10) - break when condition is satisfied
* vanish when variable goes out of scope

## Call stack
* frame 0/1/...
* up/down - navigate call stack
* backtrace (bt) - show entire stack

## TUI
* gdb ... -tui
* toggle with CTRL-X-A

## Startup files
* .gdbinit in home directory and project directory
* gdb -command=... - specify startup file

## Misc
* help $CMD - get help on command
* run - can restart program too!
