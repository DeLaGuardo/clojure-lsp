# Development

For `clojure-lsp` development, there are 3 possible ways of finding a bug or implementing a new feature:

- Create a test for your bug/feature, then implement the code following the test (TDD).
- `clojure-lsp` starts a NREPL server if built with `clj -X:debug-jar && clj -X:bin`, with that it's possible to change the code of a running instance and see the changes on your client in real time. To get the NREPL port, you can check the `/tmp/clojure-lsp.*.out` log, it will print the NREPL port on server startup or you can get it via `server-info` custom LSP command.
- Build `clojure-lsp` with your changes and test it manually in your client, this is the slowest option, but it makes sense for final tests.
- For debugging purposes, there is two custom commands `server-info` and `cursor-info`.
