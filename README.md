# ClojureScript corpus

In linguistics, a text corpus is a set of texts written in a language. Its purpose is to be analyzed to test hypotheses about the actual usage of the language.

Similarly the aim of cljs-corpus is to provide a searchable local archive of ClojureScript as it is used in the wild.

Why would you use a local archive over tools like [Github Code Search](https://github.com/search/advanced)?

- Curation: The projects have been selected to exhibit high standards of quality
- It's All Text: Because the full text is present on your machine, you can use text search tools like grep or ripgrep to refine your search.
- Reliability: Compared to Github's fuzzy search, grep is predictable and allows exact string maches as well as regular expression queries.

The corpus contains popular OSS libraries. But recognizing the differences between application code and library code the archive also puts a focus on real-world applications written in ClojureScript.

## Usage

Clone this repository and update its submodules:

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

For the best search experience, install [ripgrep](https://github.com/BurntSushi/ripgrep), a fast and reliable replacement for grep.

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

## Related work

- [CrossClj](https://crossclj.info/)
- [Coal mine](https://github.com/mfikes/coal-mine)
