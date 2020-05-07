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
