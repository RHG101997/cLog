# cLog

A Python library for adding colors to text in terminal and command prompt using ANSI escape sequences.

## Installation

```bash
pip install cLog
```

## Usage

### Basic Setup

```python
from cLog import BeginClog

# Create an instance
logger = BeginClog()
```

### Colored Text Logging

#### Simple colored text
```python
# Basic colored text (strong accent by default)
logger.log("red", "This is red text")
logger.log("green", "This is green text")
logger.log("blue", "This is blue text")

# With normal accent
logger.log("yellow", "This is yellow text with normal accent", "normal")
```

#### Text with colored backgrounds
```python
# Text with background color
logger.bgLog("red", "white", "White text on red background")
logger.bgLog("blue", "yellow", "Yellow text on blue background")

# With strong background accent
logger.bgLog("cyan", "black", "Black text on cyan background", "strong")
```

#### Quick warning and error messages
```python
logger.warning("This is a warning message")  # Yellow text
logger.error("This is an error message")      # Red text
```

### Block Coloring

For coloring multiple lines of text:

```python
# Start colored block
logger.beginBlock("cyan")
print("All this text will be cyan")
print("This line too!")
print("And this one as well")

# Reset to normal color
logger.reset()
print("Back to normal color")
```

### Available Colors

- black
- red
- green
- yellow
- blue
- magenta
- cyan
- white

### Text Accents

- `"normal"` - Standard color intensity
- `"strong"` - Bright/bold color (default)

### Background Accents

- `"normal"` - Standard background
- `"strong"` - Bright background

## Examples

Run the built-in test functions to see examples:

```python
from cLog.clog import testLogs, testBlock

# Test various log functions
testLogs()

# Test block coloring
testBlock()
```

