# FSync
Console utility to sync one folder with another. New and modified source files are copied to the destination and any destination files that do not exist in the source are deleted.

## Version
- v1.0.1 - November 5, 2020
- macOS, Linux, Windows
- [MIT License](LICENSE)
- By Abe Pralle

## Installation
1. Install the [Rogue](https://github.com/AbePralle/Rogue) language.
2. Run `rogo` in this folder to compile **FSync**.
    - On macOS and Linux a launcher will be created here: `/usr/local/bin/fsync`.
    - On Windows the build process will print the necessary folder to add to the system PATH environment variable.

### Example

    fsync ~/Libraries/MyLibrary ~/Projects/MyProject/Libraries/MyLibrary

### Usage

    fsync [options] source-filepath [destination-filepath]

### Options

Option                        | Description
------------------------------|-------------------------------------
--dry-run<br>--dry<br>-d      | Print file copy messages without actually copying them.<br>Should not be used with --quiet.
--help<br>-h<br>-?            | Show this help text.
--keep-unused<br>--keep<br>-k | Do not delete files that are in destination but no longer in source.
--quiet<br>-q                 | Do not print file copy actions.

### Notes
- If no destination filepath is given, the current folder is used as the fsync destination.

