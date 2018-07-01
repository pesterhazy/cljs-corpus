# ClojureScript corpus

In linguistics, a text corpus is a set of written texts in a given language, collected to be analyzed to test hypothesis about the language.

Similarly, the aim of cljs-corpus is to provide a searchable archive of ClojureScript code in the wild.

What does this give you over tools like Github Code Search?

- Curation: The projects have been selected to exhibit high standards of quality
- It's All Text: Because the archive is on your machine, you can use text search tools like grep or ripgrep to narrow down searches.
- Reliability: Compared to Github's fuzzy search, grep is predictable and allows exact string searches as well as regular expression.

cljs-corpus contains popular OSS libraries. But in recognition of the fact that application code is different from library code it also includes real-world applications.

## Usage

Clone this repository and update the submodules:

```
git clone https://github.com/pesterhazy/cljs-corpus.git
cd cljs-corpus
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
