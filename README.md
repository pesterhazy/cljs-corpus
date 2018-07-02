# ClojureScript corpus

In linguistics, a text corpus is a set of written texts in a given language, collected to be analyzed to test hypothesis about the language.

Similarly, the aim of cljs-corpus is to provide a searchable archive of ClojureScript code in the wild.

Why would you use this over tools like [Github Code Search](https://github.com/search/advanced)?

- Curation: The projects have been selected to exhibit high standards of quality
- It's All Text: Because the full text is on your machine, you can use text search tools like grep or [ripgrep](https://github.com/BurntSushi/ripgrep) to refine your search.
- Reliability: Compared to Github's fuzzy search, grep is predictable and allows exact string searches as well as regular expression.

cljs-corpus contains popular OSS libraries. But in recognition of the fact that application code is different from library code it also includes real-world applications.

## Usage

Clone this repository and update the submodules:

```
git clone https://github.com/pesterhazy/cljs-corpus.git
cd cljs-corpus
git submodule update --init --recursive
```

Each time `git pull` you will need to update the submodules again:

```
git submodule update --init --recursive
```

The corpus currently weighs in at >300M so give this some time to complete.

## Example queries

For the best search experience, install [ripgrep](https://github.com/BurntSushi/ripgrep). It's fast and reliable.

1. Find creative use of the Google Closure Library

    ```
    rg -w goog
    ```

1. How do people use LocalStorage from ClojureScript?

    ```
    rg -w localstorage
    ```

1. I can't remember the order of arguments for clojure.string/join

    ```
    rg -C3 -g '*.clj[sc]' -w join
    ```
