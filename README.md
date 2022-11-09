# loguru

Loguru is a generator for easy-to-generate log files.
It is based on the [Loguru](https://github.com/excel-creators/loguru) library.

## Usage

Modular Loguru is modular and contains modules to generate log files from a file of origin.
There are two types of modules:
**

- `loguru.get_frame` - called when loguru started and returns a helper for disabling Tornado's CSS unnecessary styling for the `$1` style
- `loguru.get_room` - called when loguru catches an unexpected an error happened

In addition to these modules, there're some useful functions:
**

  * loguru.get_file
  * loguru.get_room
  * loguru.copy
  * loguru.get_frame
  * loguru.get_url

  Those two module can generate log files from terminal and Firefox.

The log files can be saved to files or provided as sockets using `loguru.test_commands`. Loguru also generates a log file with the trace of its execution trace.
  Note: loguru.test_commands supports a number of commands.

    **
    loguru.test_command('interpreter', 'dav')(tion, cookie, name, start) -  do some thing with `loguru`.log and `loguru.dat`

    loguru.test_command('interpreter', 'dav')(tation, cookie, rd, nonLn, txt, ext, filename) -  do some thing with `loguru`.log and `loguru.dat`

    loguru.test_command('interpreter', 'html-html')(tation, cookie, verb, tag) -  do some thing with `loguru`.log and `loguru.dat`

    loguru.test_command('interpreter', 'html-html')(tation, cookie, cpu_time) -  do some thing with `loguru`.log and `loguru.dat`

    loguru.test_command('interpreter', 'html-html')(tation, cookie, js_time) -  do some thing with `loguru`.log and `loguru.dat`

    loguru.test_command('interpreter', 'html-html')(tation, cookie, data_time) -  do some thing with `loguru`.log and `loguru.dat`

    loguru.test_command('interpreter', 'html-html')(tation, cookie, js_time) -  do some thing with `loguru`.log and `loguru.kdf`

    loguru.test_command('interpreter', 'html-json')(tation, cookie, js_time) -  do some thing with `loguru`.log and `loguru.dat`

    loguru.test_command('interpreter', 'html-text')(tation, cookie, utf8_character, html_exclusive) -  do some thing with `loguru`.log and `loguru.dat`

    loguru.test_command('interpreter', 'html-text')(tation, cookie, utf8_character, html_exclusive) -  do some thing with `loguru`.log and `loguru.dat`

    loguru.test_command('interpreter', 'html-text')(tation, cookie