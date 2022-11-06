## loguru

Basic Loguru Logging Framework


~loguru~ is a Loguru logger, a pre-instanced logger, built on top of **almost** as fast yet type-safe (i.e. slower) threading API as **almost**. It provides a
*only* no-arg Loguru logger, providing the decorums and helpers to easily manage your logging:

### Example
```python

from loguru import logger

print(logger.info("I'm a logandum."))
```

### Interface
### examples
```python
import loguru

loguru = logger.Logger()
loguru.info('Hello there!')
```
### Error handling
*Returns*: None
*Raised*: None

### Example:
```python
import loguru

loguru.info("stuff", msg, default=default_error)
```

```python
import loguru

def default_error(msg):
    print('My error message')


loguru.info('My error message', default=default_error)
```

### Context management
*On a higher level, the logger's context manager is used to manage the logger instances. This way, the current logger will
fall back to the default for the vast majority of cases in a most helpful way.*
*It is also possible to define a colorizer function, which is called when you want to print an error message based on its level (or
other criteria).
```python
from loguru import logger

loguru.info("stuff")

default_error = logger.ERROR

# Get a colorizer function. For example, if you want to use a #JAVA error text in your log.

  default_colorizer = logger.Colorizer(level=default_error.level)

  loguru.info('My name is %s' % default_colorizer.colorize('My error message'))


```

### Time-int and timetracker logging
*The TIME_INT_API uses a timer to implement the time-int representation of the events.*
*The TIME_TIMETRACE_API uses a timing reactor to implement the time-tracking system.*

### Format formatting
```python
import loguru

loguru.info("%s %s" % (stuff, format))
```

### Globals
On the primary level, use of `loguru` in a single function or script makes no sense. You should instead use a **basically* the same** *engine*
-- the ``logger.Logger`` Object.

```python
from loguru import Logger as _Logger

def print(msg):
    _Logger.print(msg)
```

:simple: print("hello world!")

### Marathon and parallel logging with `loguru.logsection_fn`
*class:`loguru.logsection_fn` uses thread-safeness to make it *usually* better in terms of performance and memory usage.*

```python
import loguru

loguru.append_logsection_fn(x, y)
```

=====
`loguru` is intended to be a logging functionality implemented by the
**almost** API, which is generally faster than **almost**. However, please be aware that

**almost** is relatively *strong-willed**. It will handle issues with signaling