# Submit

if you're working locally, you should use the [Exercism CLI](https://exercism.org/docs/using/solving-exercises/working-locally) to upload and submit your solution so that it appears on the Exercism website.

As an example, for the `bob` exercise, switch to the its root directory from the command line and type:

```bash
$ exercism submit src/bob.clj

Your solution has been submitted successfully.
View it at:

https://exercism.org/tracks/clojure/exercises/bob
```

~~~~exercism/note
Submitting via the Exercism CLI allows you to submit an incomplete solution, which in turn unlocks community solutions and lets you request help from a mentor.
However, if you're submitting via the online editor, your solution must pass all tests before you can do either.
~~~~

## It works locally — so why is it failing online?

When working locally, a solution that passes all tests using Clojure CLI or Leiningen may sometimes fail after submission in the online editor.
This can happen if there's a temporary issue with Exercism's infrastructure.
In that case, simply try rerunning the tests in the online editor later.

However, another common reason involves differences in how tests are executed locally versus online.
The tools mentioned above — Clojure CLI and Leiningen — run full JVM Clojure, providing access to the entire language and ecosystem, including Java interop and dynamic class loading.

### Babashka

Exercism, on the other hand, uses [Babashka](https://babashka.org) as its test runner.
Babashka, is a lightweight and fast Clojure interpreter built on GraalVM and it supports only a subset of Clojure and libraries.

As a result, code that runs fine with Clojure CLI or Leiningen may not work in Babashka — especially if it relies on unsupported features or libraries.
If that happens, you can either remove those features from your code before submitting again, **or** use the online editor to write and test your solution directly in Exercism's environment.

**Read more about Babashka:**

* [Babashka goals](https://github.com/babashka/babashka#goals)
* [Differences with Clojure](https://github.com/babashka/babashka#differences-with-clojure)

**See also:** [Tests pass locally but not online?](https://exercism.org/docs/using/solving-exercises/tests-pass-locally)

Lastly, it is possible — though uncommon — for a solution to pass in Exercism's online editor but fail locally.
If that's the case, please let us know on the [Exercism forum](https://forum.exercism.org).
