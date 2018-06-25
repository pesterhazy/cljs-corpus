# ClojureScript corpus

A collection of high-quality ClojureScript code with high greppability.

The OSS projects referenced in this reposiory have been selected because they solve a variety of problems and contain high-quality code.

- Usage examples: find how libraries and Browser APIs are used in real code
- Inspiration: find out how others approach problems
- Remember: remind yourself of the use of ClojureScripts standard library

## Usage

Clone this repository

Check out the submodules:

```
git submodule update --init --recursive
```

The corpus currently weighs in at >300M so give this some time to complete.

## Example queries

Install [ripgrep](https://github.com/BurntSushi/ripgrep). It's fast and reliable.

Find usage of the Google Closure Library

```
rg -w goog
```

How do I use LocalStorage from ClojureScript?

```
rg -w localstorage
```

How does do I join a collection into a string again?

```
rg -w join
```
