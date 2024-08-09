# Logged.py
A custom logging package with advanced features including color-coded console output, log rotation, and compression.

## Installation
To install the package, you need to create a distribution and upload it to PyPI. If you want to install it locally for testing, follow these steps:

Prepare the Package: Create the source distribution and wheel files:

```bash
python setup.py sdist bdist_wheel
```
Install Locally:

```bash
pip install dist/your_logging_package-0.1.0-py3-none-any.whl
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
**output_type:** Specify "console" for console output or "file" for file output.\n
**format:** Define the log message format using custom tags (e.g., /d for date, /t for type, /m for message).\n
**file:** If you chose output type as "file" this is a required parameter which must include the log file path.\n

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
<class>Logger
A class for logging messages.

Constructor:

**<str>output_type:** "console" or "file". Default is "console".
**<str>format:** Log message format. Default is "<bold><gray>/d</gray> <type>/t</type></bold> /m".
**<str?>file:** File path for file output.

Methods:

**trace(message: str):** Logs a trace message.
**debug(message: str):** Logs a debug message.
**info(message: str):** Logs an info message.
**warn(message: str):** Logs a warning message.
**error(message: str):** Logs an error message.
**fatal(message: str):** Logs a fatal message.
**all(message: str):** Logs a message for all levels.

Example:
```python
import logger

# Initialize logger
logger = logger.Logger(output_type='file', format='<bold><gray>/d</gray> <type>/t</type></bold>       /m', file='logfile.txt')

# Log messages
logger.info("This is an info message.")
logger.error("This is an error message.")
```

## License

This package is licensed under the MIT License. See the LICENSE file for details.
