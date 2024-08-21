# NAME

Script Generator - A simple script generator based on file extensions

# VERSION

1.0.1 (2024.08.21.)

# SYNOPSIS

script.pl \[options\] \[file ...\]

    Options:
      -i, --interpreter  specify the interpreter to use (e.g., bash, zsh, perl, ruby etc.)
      -o, --options      specify code options to be appended below the shebang (e.g., pl-strict, py-pwn etc.)
      -v, --version      display the script version
      -h, --help         brief help message
      -m, --man          full documentation

# OPTIONS

- **-i, --interpreter**

    Specify the interpreter to use for the script. The default is 'bash'. If the script extension is recognized (e.g., \`.pl\` for Perl), the appropriate interpreter will be used automatically unless overridden.

- **-o, --options**

    Specify the code options to be appended below the shebang. If no options are provided, files containing only the shebang will be created. 

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

Options are defined with a hyphen, placing the interpreter on the left and the distinguishing name of the options on the right. You can include multiple options. However, if more than one option of the same interpreter is provided, only one will be applied.

## OPTIONS AVAILABLE

- pl-strict : (perl)

            use warnings;
            use strict;

- py-pwn : (python, python3)

            from pwn import *
            if __name__ == '__main__':

- py-main : (python, python3) 

            if __name__ == '__main__':

# LICENSE

This project is licensed under the GNU General Public License v3.0
