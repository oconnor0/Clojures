# Clojures

This is, or will be, a Sublime Text package that handles support for Clojure and ClojureScript. Some of this is because ST's default Clojure package didn't differentiate between Clojure and ClojureScript which broke how linting and Zeal wanted to interact with scopes.

Additionally, I've been changing some of the syntax definition so that various pieces are highlighted more consistently and so that Expand Selection to Scope works more consistently.

For example, given the following:

```clojurescript
(def name :keyword symbol)
```

With the default syntax, if the cursor is in `symbol`, Expand Selection to Scope will fill everything inside the parens, but if the cursor is on any other form in, Expand Selection to Scope will expand to just that word. Adding a `variable.other.symbol.clojure` scope allows ST to know to not expand beyond.

## Future?

I am uncertain if this package is worth publishing.

The tests have not been updated to handle the syntax changes.

EDN should probably be its own syntax?

`def` are treated as functions rather than constants:

![scope of name in def](https://user-images.githubusercontent.com/64384/83309103-a067ae00-a1c5-11ea-82d6-2b59bf9e26f0.png)

