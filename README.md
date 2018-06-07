# Manifest Language Syntax

The Manifest language is very simply a list of lines.  Each line is ether whitespace (ignored), a comment (starts with #), or defines an item.

## Details

### First line

To automatically change the scope make the first line of the manifest the following:

```manifest
# :-- manifest --:
# This is a manifest file now
```

### Comment

Any line starting with "#" is a comment


```manifest
# This is a comment

  # This is a also a comment
```

#### Header

Any comment with a with "--" is a header comment.

```manifest
#-- This is a header
```

### Item

Any non-empty line is a item line.  Each line has 4 or more parts that are space separated:
1. The name of the item
2. The version of the item
3. Reference to the item's version (usually a git hash)
4. Other space separated metadata

```manifest
#-- Example of a line
# name  version  ref      metadata
foo     1.2.3    afdc125  release-1.2.3 release-1.2 develop master
bar     2.3.4    abc123   release-2.3.4 release-2.3 develop master
```

## Install

Clone this repo into the `~/.atom/packages` item and reload atom.

```bash
$ cd ~/.atom/packages
$ git clone git@github.com:jkamenik/language-manifest.git
```