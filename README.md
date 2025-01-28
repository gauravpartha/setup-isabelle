# setup-isabelle
Composite GitHub action to set up the [Isabelle interactive theorem prover](https://isabelle.in.tum.de/).
That means, the GitHub action downloads and extracts Isabelle and adds Isabelle to the path environment variable.
Currently, the action only supports Linux versions of Isabelle, and thus only works for Linux runners.

This action takes a single parameter `isabelle-version` indicating the version of Isabelle that should be set up.
See the [CI](https://github.com/gauravpartha/setup-isabelle/blob/main/.github/workflows/ci.yml) for this repository, which showcases how the action can be used.
