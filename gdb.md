## Breakpoints
* break ... - set breakpoint
  * foo.c:42 - break at line in file
  * foo.c:bar - break at function in file
* tbreak (tb) ... - set one-time breakpoint
* rbreak (rb) foo - break at *foo* (can supply arbitrary grep style regex)
* clear ... / del $BP_NUM - remove breakpoint
* disable / enable (once) $BP_NUM
* info break - list breakpoints
* condition (cond) $BP_NUM x==42 - only break if condition is fullfilled;
  call without last argument to remove condition
* break ... if x==42 - short form of above
* command $BP_NUM
  silent
  ...
  (continue)
  end

## Moving around
* next / step (n) - move / step n times
* continue (n) - continue and ignore next n breakpoints
* finish (fin) - resume until just after end of current stack frame
* until - run until a source line greater than the current one (break out of loop)
* until ... - run until line, function etc.

## Watchpoints
* watch x - break when x changes value
* watch (x > 10) - break when condition is satisfied
* vanish when variable goes out of scope

## Catchpoints
* break at exceptions, signals, forks, library loading etc.

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

## Expressions
* can use all operators and own/library functions! e.g. len(x) > 0;
  if there are no debug symbols for linked function, int return values are assumed;
    can circumvent with "set $f = (double (*) (double)) cos; p $f(...)"
* compiling with -g3 lets us use preprocessor macros in expressions

## Misc
* help $CMD - get help on command
* run - can restart program too!
  * even after recompiling, no need to restart gdb
* list $FILE - changes focus too
* define - create macro, use $arg0 etc. to refer to arguments
  * show user - show all macros
