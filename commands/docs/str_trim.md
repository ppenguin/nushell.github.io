---
title: str trim
categories: |
  strings
version: 0.87.0
strings: |
  Trim whitespace or specific character.
usage: |
  Trim whitespace or specific character.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for strings

<div class='command-title'>{{ $frontmatter.strings }}</div>

## Signature

```> str trim {flags} ...rest```

## Flags

 -  `--char, -c {string}`: character to trim (default: whitespace)
 -  `--left, -l`: trims characters only from the beginning of the string
 -  `--right, -r`: trims characters only from the end of the string

## Parameters

 -  `...rest`: For a data structure input, trim strings at the given cell paths


## Input/output types:

| input        | output       |
| ------------ | ------------ |
| list\<string\> | list\<string\> |
| record       | record       |
| string       | string       |
| table        | table        |
## Examples

Trim whitespace
```nu
> 'Nu shell ' | str trim
Nu shell
```

Trim a specific character
```nu
> '=== Nu shell ===' | str trim --char '=' | str trim
Nu shell
```

Trim whitespace from the beginning of string
```nu
> ' Nu shell ' | str trim --left
Nu shell
```

Trim a specific character
```nu
> '=== Nu shell ===' | str trim --char '='
 Nu shell
```

Trim whitespace from the end of string
```nu
> ' Nu shell ' | str trim --right
 Nu shell
```

Trim a specific character
```nu
> '=== Nu shell ===' | str trim --right --char '='
=== Nu shell
```
