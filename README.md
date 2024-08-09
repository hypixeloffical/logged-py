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
logger = your_logging_package.Logger(output_type='console', format='<bold><gray>/d</gray> <type>/t</type></bold>       /m')
```
output_type: Specify "console" for console output or "file" for file output.
format: Define the log message format using custom tags (e.g., /d for date, /t for type, /m for message).
Logging Messages
You can use different methods to log messages at various levels:

python
Copy code
logger.trace("This is a trace message.")
logger.debug("This is a debug message.")
logger.info("This is an info message.")
logger.warn("This is a warning message.")
logger.error("This is an error message.")
logger.fatal("This is a fatal message.")
logger.all("This is a message for all levels.")
Features
Customizable Formatting: Use ANSI color codes and custom tags in log messages.
Log Rotation with Compression: Automatically rotates log files and compresses old logs into ZIP archives.
Flexible Output Options: Choose between console and file output.
API Reference
create_file_if_not_exists(file_path)
Creates an empty file if it does not exist.

Parameters:
file_path: Path to the file to create.
zip_and_delete_file(file_path)
Compresses a file into a ZIP archive and deletes the original file.

Parameters:
file_path: Path to the file to compress.
Logger
A class for logging messages.

Constructor:

output_type (str): "console" or "file". Default is "console".
format (str): Log message format. Default is "<bold><gray>/d</gray> <type>/t</type></bold> /m".
file (Optional[str]): File path for file output.
Methods:

trace(message: str): Logs a trace message.
debug(message: str): Logs a debug message.
info(message: str): Logs an info message.
warn(message: str): Logs a warning message.
error(message: str): Logs an error message.
fatal(message: str): Logs a fatal message.
all(message: str): Logs a message for all levels.
Example
Here’s a complete example demonstrating how to use the Logger class:

python
Copy code
import your_logging_package

# Initialize logger
logger = your_logging_package.Logger(output_type='file', format='<bold><gray>/d</gray> <type>/t</type></bold>       /m', file='logfile.txt')

# Log messages
logger.info("This is an info message.")
logger.error("This is an error message.")
License
Specify the license under which your package is distributed. For example:

This package is licensed under the MIT License. See the LICENSE file for details.
