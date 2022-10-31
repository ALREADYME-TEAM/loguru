# Loguru

Loguru is a Django page logger built using [Wiki](http://wiki.loguru.org) with easy-to-digest code.


Contributions:

  See [wiki.loguru.org](http://wiki.loguru.org/sites/default/wiki)

# Installation

### Requirements

  A Python 3.4+ development environment and a version of Django before 1.6.0 are required.

  See [`pip`](https://docs.python-breeding.org/en/latest/user-guide/) for installation instructions.


### Install

  `pip install loguru`


# Configuration

  The configuration of Loguru is written into `loguru.ini` file, located in the `yourproject/` directory.
  Your project's.gitignore may also contain the `loguru.ini` subdirectory, in which case the `loguru.ini` file may be ignored.


## Configuration examples

  Lets say that Auth manager typically records posting with a `user` and a associated `account_id` on the first line of the log. We may insert a class name, a python module and the logging-related parameters for the Auth manager, e.g. `logger` or `logger`:

    from loguru import logger

    _logger = logger()    # default logger object
    _logger.debug("Debug")  # adds debug level
    _logger.info("Info")  # adds info level
    _logger.warning("Warning") # adds warning level
    _logger.error("Error") # adds error level

    _logger.info("Appropriate module name for logging")
    if "auth.manager" in Loguru's module names:
        _logger.info("Attaching auth.manager module name to logger's module names")
    _logger.info("Will start logger in the default thread context")


Each Loguru logger should specify all logging parameters as well as a pre-trigger api-key:

    __logging__ = [
        ['auth.manager', 'frontend-login', True],
     ]


You may also specify specific modules (via the SHORT_MODULE constant) as well. For default module:

  ```python
  loguru.default_module = logging
```

The `loguru.ini` file will also provide all these logging key values, as may changed with the `update_loguru_ini` task.

  ```python
  default_module = logging
  __logging__ = [
    [ "auth.manager", "frontend-login", True ]
  ]
  __short_module = auth.manager
```

  You may overwrite default module and short_module settings by manual entry in `loguru.ini`-object.

  For example, the following Loguru settings correspond to `loguru.ini` file:

    hit_list = []
    #flag to capture addresses
    log_db = False

And you may insert something like the log resources (see above):

    hit_list = [

        # inventory items
        RegisterItem(),
        DUPLIST
     ]

# Setting the log url to the web address (for example):
     log_url = 'https://www.example.com/'

When using the multi-threading mode, use `threading.current_thread.name` to get the current thread's name. Default value is `main`:

    default_url = 'http://loguru.example.com'

# Internet and HTTPS checking for security reasons:
    if is