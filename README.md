# Java Shell Implementation

A lightweight shell implementation in Java that supports basic Unix-like commands. This shell provides a minimal command-line interface with support for common shell operations.

## Features

- Basic command prompt interface (`$`)
- Built-in commands:
  - `pwd` - Print working directory
  - `cd` - Change directory (supports absolute paths and `~` for home directory)
  - `echo` - Print text to console (supports both quoted and unquoted strings)
  - `type` - Display information about command type
  - `exit` - Exit the shell

- External command execution through PATH lookup
- Path normalization and validation
- Home directory resolution (`~`)

## Requirements

- Java 11 or higher
- `java.nio.file` support
- Operating system with PATH environment variable

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/java-shell.git
```

2. Compile the Java file:
```bash
javac Main.java
```

3. Run the shell:
```bash
java Main
```

## Usage

The shell provides a command prompt (`$`) where you can enter commands:

```bash
$ pwd
/current/working/directory
$ echo "Hello World"
Hello World
$ cd ~
$ type echo
echo is a shell builtin
```

### Supported Commands

1. `pwd`
   - Displays the current working directory

2. `cd [directory]`
   - Changes the current working directory
   - Supports absolute paths and `~` for home directory
   - Example: `cd ~/Documents` or `cd /usr/local`

3. `echo [text]`
   - Prints text to the console
   - Supports both quoted and unquoted strings
   - Example: `echo Hello World` or `echo "Hello World"`

4. `type [command]`
   - Displays whether a command is a shell builtin or its location in PATH
   - Example: `type pwd` or `type java`

5. `exit 0`
   - Exits the shell

## Implementation Details

- Uses Java NIO for file operations
- Implements PATH lookup for external commands
- Handles both built-in commands and external executables
- Supports basic string parsing for command arguments
- Implements working directory management

## Limitations

- Basic command parsing (no advanced shell features)
- Limited support for command arguments and flags
- No pipeline support
- No environment variable expansion
- No wildcard support
- No command history

## Contributing

Feel free to submit issues and enhancement requests!
