# Level 1 -> Level 2

## Goal

The password for the next level is stored in a file named `-` in the home directory.

## Concepts

Most commands treat a lone `-` as "read from standard input" instead of as a file name. That means `cat -` doesn't open a file called `-`. It just waits for me to type input.

Putting `./` in front of the name fixes this. `./` means "the current directory," so `./-` is a path to the file instead of a bare `-` the command can misread.

## What I did

I ran `ls` and saw one file named `-`. Running `cat -` just hung, because `cat` was waiting for input from my keyboard, so I stopped it with `Ctrl+C`. Then I ran:

`cat ./-`

This printed the password for the next level.

## What I learned

A file name can be misread by a command if it looks like an option or a special symbol. Adding the path (`./`) makes it clear that I mean a file. In later levels, I expect to read manual pages (`man`) to figure out how commands handle special cases like this.

## Real-World Application

File names starting with `-` can be mistaken for command options, which is a known security issue. For example, if an attacker creates a file named `-rf` in a folder, a careless `rm *` can interpret it as an option instead of a file name. Defenders avoid this by using `./*` instead of `*`, or by using `--` to mark the end of options.
