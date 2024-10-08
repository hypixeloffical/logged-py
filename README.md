# Logged.py
A custom logging package with advanced features including color-coded console output, log rotation, and compression.

## Installation
To install the package you can run this command in your command prompt or powershell.

```bash
pip install logged
```

## Usage
### Importing the Package
```python
import logged
```

### Creating a Logger
Create a Logger instance with the desired output type and format.

```python
logger = logger.Logger(output_type='console', format='<bold><gray>/d</gray> <type>/t</type></bold>       /m')
```
**output_type:** Specify "console" for console output or "file" for file output.

**format:** Define the log message format using custom tags (e.g., /d for date, /t for type, /m for message).

**file:** If you chose output type as "file" this is a required parameter which must include the log file path.

### Logging Messages
You can use different methods to log messages at various levels:

```python
logger.trace("This is a trace message.")
logger.debug("This is a debug message.")
logger.info("This is an info message.")
logger.warn("This is a warning message.")
logger.error("This is an error message.")
logger.fatal("This is a fatal message.")
logger.all("This is a message for all levels.")
```
### Features
- **Customizable Formatting:** Use ANSI color codes and custom tags in log messages.
- **Log Rotation with Compression:** Automatically rotates log files and compresses old logs into ZIP archives.
- **Flexible Output Options:** Choose between console and file output.

### API Reference
\<class\>Logger

A class for logging messages.

#### Constructor:

**\<str\>output_type:** "console" or "file". Default is "console".
**\<str\>format:** Log message format. Default is "<bold><gray>/d</gray> <type>/t</type></bold> /m".
**\<str?\>file:** File path for file output.

#### Methods:

**<None>trace(message: str):** Logs a trace message.

**<None>debug(message: str):** Logs a debug message.

**<None>info(message: str):** Logs an info message.

**<None>warn(message: str):** Logs a warning message.

**<None>error(message: str):** Logs an error message.

**<None>fatal(message: str):** Logs a fatal message.

**<None>all(message: str):** Logs a message for all levels.


#### Example:
```python
import logger

# Initialize logger
logger = logger.Logger(output_type='file', format='<bold><gray>/d</gray> <type>/t</type></bold>       /m', file='logfile.txt')

# Log messages
logger.info("This is an info message.")
logger.error("This is an error message.")
```

## License

This package is licensed under the MIT License. See the [LICENSE](https://github.com/hypixeloffical/logged-py/blob/main/LICENSE) file for details.
