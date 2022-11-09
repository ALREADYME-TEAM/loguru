# loguru

[![Build Status](https://secure.travis-ci.org/djyun-dev/loguru.png)](http://travis-ci.org/djyun-dev/loguru)

A Cython-like Python logging library.

This is an almost finished project, but I'd like to release it sooner than everyone else, so you can use it.
We've done our best to minimize XCode guidance on my releases, but if you encounter problems during development, I'm sorry.
Work in progress.


Collect all custom records you want to have in your log.

{}

Record with your own minimal idea of what format your log should be in.

{name} {no} {icon}

Record a string with sprintf (or whatever you want to format your log with). sprintf is an alias for sys.stdout.write(). For example, for log "go here$>" use:

{name} {no} {DEBUG} {*.v5.debug}

Use `strftime` or other supported Python built-in.

{name} {no} {colorized} {color map} {color_map} {5seconds} {all}

Example: Print "all examinations passed": 1, "Some examinations passed": 0, "None passed": 1. (No space within parentheses).

With colorized use:

{name} {no} {colorized} {color map} {20 hours} {all}

Example: Print "all examinations passed": 1, "None passed": 0, "Some examinations passed": 0.

Or other built-in support:

{name} {no} {colorized} {color map} {all}

Example: Print "all examinations passed": 1, "None passed": 0, "Some examinations passed": 0.

If you need the color script running during development, have it near your debugger:

{name} {no} {colorized} {color map}

Example: Print "all examinations passed": 1, "No pass": 0, "Some examinations passed": 0.

If writing red-bloods clueless to this library is your goal, use the one below.

The only reqimtes are proper parentheses and proper location (until the parsing logic clarifies how to handle double closing parentheses, in which case I'll refactor or rewrite).


`print("${ name } ${ no } ${ icon} ${ buildtime : 0.001 } ${ colorized } ${ color_map } 5 "seconds : """

To debug switches, use

`print("${ name } ${ no } ${ colorized } ${ color_map } switch {THE_EXPRS } AND {THE_EXPRS_s`

To inspect selected records, use `print("${ name } ${ no } ${ colorized } ${ color_map } selected")

To inspect all matches of a wildcard, use
`print("${ name } ${ no } ${ colorized } ${ color_map } stop")

`

You'll get better parsing with the solid understanding of how Python's built-in tell all.

You can see the formatter being created here:

```
# <!-- compiled with xdebug -->
<debugger name="PascalConsoleDebugger">
  <classifiers>
    <filter name="compileWithStandardError">
      <condition>
        <pattern>${ dest }</pattern>
        <value>${ dest } ${ color_sub }</value>
      </condition>
    </filter>
  <classifiers>
</debugger>
```
