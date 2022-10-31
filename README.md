# Loguru
[![Python](https://img.shields.io/badge/pytorch-compatible-my-framework-green.svg?style=flat)](https://learn.python.org/tutorial/the-tutorial/logging/)

A simple Python logging library, inspired by iPython.

## Installation
### Compile
```
$./install.sh copybutton.py MergePull.py synopsis.py CommandLine.py loguru.py./
Logging settings can be saved in "/install.sh". The loguru directory contains only one file and the syntax is:

    loguru.py CopyButton_Spec [FocusOrCommand] [DoneBy] [Output]

CopyButton_Spec: The title of the command. If the "Confirm" button is clicked, the target will be confirmed
    FocusOrCommand: Clicked when the error is detected or if the "OK" button is clicked
    DoneBy: This will be a default "debugger" value old_reporting or as specified in the.json
    Output: The console output will be outputted when the Loguru is executed.
    CommandLine: This will be used to disable the native leap logging rarely used link
    Loguru: This is for configuring Loguru by Hand
    
    CopyButton_Spec: The title of the command. If the "Confirm" button is clicked, the target will be confirmed
    FocusOrCommand: Clicked when the error is detected or if the "OK" button is clicked
    DoneBy: This will be a default "debugger" value or as specified in the.json
    Output: The console output will be outputted when the Loguru is executed.
    CommandLine: This will be used to disable the native leap logging rarely used link
    Loguru: This is for configuring Loguru by Hand
    """
    
    # if we don't have the command:
    # run "./copybutton.py CopyButton [#{CopyButton_Spec}FocusOrCommand] [#{DoneBy} Output] ".
    #
    # this is a shortcut. please refer to the settings file.
    # these settings can be changed during setup
    
    # custom command to overwrite default [default_]: "print 'This is loguru command' | do nothing"
    # this is mainly to permit the script to work even if the configuration file do nothing or reset.
    # you can replace with your favorite
    CustomShell: "./copybutton.py CopyButton_Spec [#{CopyButton_Spec}FocusOrCommand] [#{DoneBy} Output] "
    
    # custom setting for "Loguru" plugin: this option configures the link to the core logging system: http://loguru.net
    LoguruPlugin: "./copybutton.py CopyButton_Spec [#{CopyButton_Spec}FocusOrCommand] [#{DoneBy} Output] "
    
    # need to try to compile by hand:
    # run "xdist --mime-priority compat gtk --define --spec "./copybutton.py"
    # this is to compile as a stand-alone.
    Connect: "onload", "loguru_plugin_signal"
```
## Compile Loguru => search
["./copybutton"]

## Testing
To include loguru.py as a testable module, add a "make test" command and run it in tests directory.
