# Submit

If you're working locally, you should use the [Exercism CLI](https://exercism.org/docs/using/solving-exercises/working-locally) to upload and submit your solution so that it appears on the Exercism website.

As an example, for the `bob` exercise, switch to the its root directory from the command line and type:

```bash
$ exercism submit src/bob.clj

Your solution has been submitted successfully.
View it at:

https://exercism.org/tracks/clojure/exercises/bob
```

## It works locally — so why is it failing online?

The two tools mentioned previously — Clojure CLI and Leiningen — run full JVM Clojure, giving access to the entire language and ecosystem, including all Java interop and dynamic classloading.

Exercism, on the other hand, uses [Babashka](https://babashka.org/) as its test runner.
Babashka, is a lightweight and fast Clojure interpreter built on GraalVM and it supports only a subset of Clojure and libraries.

As a result, code that runs fine with Clojure CLI or Leiningen may not work in Babashka — especially if it relies on unsupported features or libraries.
If that happens, you can either remove those features from your code before submitting again, **or** use the online editor to write and test your solution directly in Exercism's environment.

**Read more about Babashka:**

* [Babashka goals](https://github.com/babashka/babashka#goals)
* [Differences with Clojure](https://github.com/babashka/babashka#differences-with-clojure)

**See also:** [Tests pass locally but not online?](https://exercism.org/docs/using/solving-exercises/tests-pass-locally)

Lastly, it is possible — though uncommon — for a solution to pass in Exercism's online editor but fail locally.
If that's the case, please let us know on the [Exercism forum](https://forum.exercism.org).
