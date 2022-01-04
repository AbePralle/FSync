![FSync](Media/Logo/FSync-Black.png)

# FSync

Summary   | Current Release
----------|-----------------------
Version   | 1.2
Date      | December 26, 2021
Platforms | macOS, Linux (Ubuntu+), Windows
License   | [MIT](LICENSE)
Author    | Abe Pralle

# About
Console utility to sync one folder with another. New and modified source files are copied to the destination and any destination files that do not exist in the source are deleted.

# Installation

## New Installation

1. Install [morlock.sh](https://morlock.sh)
2. `morlock install abepralle/shellview`

## Updating Existing Installation
`morlock update shellview`

# Example

    fsync ~/Libraries/MyLibrary ~/Projects/MyProject/Libraries/MyLibrary

# Usage

    fsync [options] source-filepath destination-filepath

## Options

Option                        | Description
------------------------------|-------------------------------------
--dry-run<br>--dry<br>-d      | Print file copy messages without actually copying them.<br>Should not be used with --quiet.
--exclude=&lt;pattern&gt;<br>-x &lt;pattern&gt; | Exclude any files matching the given pattern from being copied or deleted. Multiple `--exclude` patterns can be given. Example: `--exclude="**/Web/*"`.
--help<br>-h<br>-?            | Show this help text.
--keep-unused<br>--keep<br>-k | Do not delete files that are in destination but no longer in source.
--missing<br>-m               | Only copy missing files.
--quiet<br>-q                 | Do not print file copy actions.

# Notes
- Hidden files are automatically excluded from being synced.

