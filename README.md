# Working with files

This work is devoted to God.

## Finding files in a directory

In a Bash shell:

```bash
find <DIRECTORY_PATH> -regextype posix-extended -iregex '<REGULAR_EXPRESSION>'
```

E.g.

```bash
find packages -regextype posix-extended -iregex '^.+\.(spec|test)\.js$'
```
