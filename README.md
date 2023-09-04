# .gitignore Tool

Bash script for maintaining and standardizing .gitignore files using the
program-specific files available at
[github/gitignore](https://github.com/github/gitignore).

## Usage:

```sh
ignoretool <mode> <list> -w -f <file>
```

### Arguments:

#### `<mode>` (required):

1. `add` - add a new section to an existing .gitignore file.
2. `create` - initialize a new .gitignore file from a list of preset or selected
   sections.
3. `list` - list the sections found in a `.gitignore` file.
4. `remove` - remove a particular section (or list of sections).
5. `update` - parse existing file and updating the sections present in the file.

#### `<list>` (optional):

The list is a comma- or space-delimited list of gitignore configurations. To see
what the names of each are, look at the `data` file for reference.

If no list options are given, the script will open a `fzf` prompt for you to
specify which ignore files to use.

#### `-w` or `--write` (optional)

The script will print to `stdout` by default. To write to the gitignore file
itself, pass the `-w` flag to the script.

#### `-f <file>` (optional)

Use the `-f` flag to specify the path to the .gitignore file.

If no file is specified, the script will use Git to find the base of the
repository and search f the .gitignore file there.
