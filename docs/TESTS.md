# Tests

You can use the online editor on the Exercism website to run the test suite for an exercise, **or** you can download the exercise to your computer, and run the tests locally — which is what this article focuses on.

## Exercism CLI

The first thing you'll need is the Exercism command-line tool (CLI) to download the exercises.
See the [cli documentation](https://exercism.org/docs/using/solving-exercises/working-locally) for instructions.

Once this is done, you can open the starter file found inside the `src` directory of the exercise in the editor of your choice.

* If your editor provides [integration with Clojure](https://exercism.org/docs/tracks/clojure/editors), you can test your solution directly from within the editor.
* If your editor does not provide integration with Clojure, you can use either the **Clojure CLI** or **Leiningen** to test your solution.
The next section shows how to use these tools to run the tests.

## Testing

### Clojure CLI

The Clojure exercises on Exercism ship with a `deps.edn` file with a `:test` alias to invoke the [cognitect-labs test-runner](https://github.com/cognitect-labs/test-runner).
From the command line, switch to the exercises's root directory and type:

``` bash
$ clj -X:test

Running tests in #{"test"}

Testing bob-test

Ran 25 tests containing 25 assertions.
0 failures, 0 errors.
```

This will scan your exercises's `test` directory for any tests defined using `clojure.test` and run them.

### Leiningen

The Clojure exercises on Exercism ship with a `project.clj` file.
From the command line, switch to the exercises's root directory and type:

``` bash
$ lein test

lein test bob-test

Ran 25 tests containing 25 assertions.
0 failures, 0 errors.
```
