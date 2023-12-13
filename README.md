## C - Simple Shell ##

A simple UNIX command interpreter written as part of the low-level programming and algorithm track at ALX.

## Description

**simple_shell** is a simple UNIX command language interpreter that reads commands from either a file or standard input and executes them.

## Invocation

Usage: **simple_shell** [filename]

To invoke **shell** , compile all '.c' files in the repository and run the resulting executable:

```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
/.hsh

```

**Shell** can be invoked both interactively and non-interactively. If **shell** is invoked with standard input not connected to a terminal, it reads and executes received commands in order.

Example:

```
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$

```
If **shell** is invoked with standard input connected to a terminal (determined by [isatty](https://linux.die.net/man/3/isatty)(3)), an *interactive* shell is opened. When executing interactively, **shell** displays the prompt `$ ` when it is ready to read a command.

Example:

```
$./hsh
$

```
Alternatively, if commands  line arguments are supplied invocation, **shell** treats a first argument as a file from which to read commands. The supplied file should contains one command per line. **Shell** runs each of the commands contained in the file in order before exiting.

Example:

```
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$

```
