# Get the lines around each match with ripgrep

You can include the lines that come before or after each match with ripgrep to better understand the context of each match.

This can done with the `--context {number}` parameter or shortened to `-C {number}` to include {number} lines before and after each match.

```
$ rg -C 1 "pattern" .
```

The `--before-context` parameter or shortened to `-B` will only include the lines before each match.

The `--after-context` parameter or shortened to `-A` will only include the lines after each match.
