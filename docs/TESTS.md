# Tests

You can use the online editor on the Exercism website to run the test suite for an exercise, **or** you can download the exercise to your computer and run the tests locally — which is what this article focuses on.

The first thing you'll need is the Exercism command-line tool (CLI) to download the exercises.
See the [documentation](https://exercism.org/docs/using/solving-exercises/working-locally) for instructions.

Once this is done, open the starter `.clj` file in the `src` directory using your favorite editor and start writing your solution.

* If your editor [integrates with Clojure](https://exercism.org/docs/tracks/clojure/editors), you can test your solution directly from within the editor.
* If your editor doesn't integrate with Clojure, you can test your solution directly using the Clojure CLI or Leiningen.
Their usage is explained below.

### Clojure CLI

The Clojure exercises on Exercism ship with a `deps.edn` file with a `:test` alias to invoke the [cognitect-labs test-runner](https://github.com/cognitect-labs/test-runner).
From the command line, switch to the exercise's root directory and type:

``` bash
$ clj -X:test

Running tests in #{"test"}

Testing bob-test

Ran 25 tests containing 25 assertions.
0 failures, 0 errors.
```

This will scan your exercise's `test` directory for any tests defined using `clojure.test` and run them.

### Leiningen

The Clojure exercises on Exercism ship with a `project.clj` file, which is the configuration file for a Leiningen project.
From the command line, switch to the exercise's root directory and type:

``` bash
$ lein test

lein test bob-test

Ran 25 tests containing 25 assertions.
0 failures, 0 errors.
```
