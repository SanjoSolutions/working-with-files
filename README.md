# Working with files

This work is devoted to God.

## Table of contents

* [Finding files in a directory (with POSIX extended regular expression support)](#finding-files-in-a-directory-with-posix-extended-regular-expression-support)
* [Finding files in a directory (with PERL regular expression support)](#finding-files-in-a-directory-with-perl-regular-expression-support)

## Finding files in a directory (with POSIX extended regular expression support)

In a Bash shell:

```bash
find <DIRECTORY_PATH> -regextype posix-extended -iregex '<REGULAR_EXPRESSION>'
```

E.g.

```bash
find packages -regextype posix-extended -iregex '^.+\.(spec|test)\.js$'
```

## Finding files in a directory (with PERL regular expression support)

PERL regular expressions also support negativ lookahead patterns.

In a Bash shell:

```bash
find <DIRECTORY_PATH> | grep -P '<REGULAR_EXPRESSION>'
```

E.g.

```bash
find packages | grep -P '^packages\/[^\/]+\/(?!src\/).+\.(?:spec|test)\.js$'
```
