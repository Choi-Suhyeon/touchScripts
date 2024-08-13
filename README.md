# NAME

Script Generator - A simple script generator based on file extensions

# VERSION

0.0.0 (2024.08.13.)

# SYNOPSIS

script.pl \[options\] \[file ...\]

    Options:
      -i, --interpreter  specify the interpreter to use (e.g., bash, zsh, perl, ruby etc.)
      -v, --version      display the script version
      -h, --help         brief help message
      -m, --man          full documentation

# OPTIONS

- **-i, --interpreter**

    Specify the interpreter to use for the script. The default is 'bash'. If the script extension is recognized (e.g., \`.pl\` for Perl), the appropriate interpreter will be used automatically unless overridden.

- **-v, --version**

    Displays the version of the script.

- **-h, --help**

    Prints a brief help message.

- **-m, --man**

    Displays the complete manual page for the script.

# DESCRIPTION

This script generates a new script file with the correct shebang line based on the file extension or the specified interpreter. It can also add basic boilerplate code and set the execute permissions for the file.

The supported interpreters include bash, zsh, sh, csh, ksh, tcsh, perl, ruby, python, and python3. 

If no specific extension is provided, the script will use the interpreter given as an option or the default interpreter.

If an extension is provided and it is unsupported, the script will raise an error. This happens if no interpreter is provided as an option, rather than using the default interpreter.
