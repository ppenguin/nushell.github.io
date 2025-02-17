---
title: dfr col
categories: |
  expression
version: 0.87.0
expression: |
  Creates a named column expression.
usage: |
  Creates a named column expression.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for expression

<div class='command-title'>{{ $frontmatter.expression }}</div>

## Signature

```> dfr col {flags} (column name)```

## Parameters

 -  `column name`: Name of column to be used


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Creates a named column expression and converts it to a nu object
```nu
> dfr col a | dfr into-nu
╭───────┬────────╮
│ expr  │ column │
│ value │ a      │
╰───────┴────────╯
```


**Tips:** Dataframe commands were not shipped in the official binaries by default, you have to build it with `--features=dataframe` flag