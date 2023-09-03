# .gitignore Tool

Bash script for maintaining and standardizing .gitignore files using the
program-specific files available at
[github/gitignore](https://github.com/github/gitignore).

Functions:

1. `add` - remove a particular section (or list of sections) if found.
2. `create` - parse all the files in the Git repo (use `gitpython` library for
   this), create a list of all MIME types found, and append the correspondinm
   `github/gitignore` files to the `.gitignore` file.
3. `list` - list the sections in a `.gitignore` file.
4. `remove` - remove a particular section (or list of sections) if found.
5. `update` - parse existing file and updating the sections present in the file.
