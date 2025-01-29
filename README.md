# setup-isabelle
Composite GitHub action to set up the [Isabelle interactive theorem prover](https://isabelle.in.tum.de/).
That means, this GitHub action downloads and extracts Isabelle and adds Isabelle to the path environment variable.
Currently, this action supports only Linux versions of Isabelle, and thus only works for Linux runners.
Caching of the downloaded Isabelle version across workflows is implemented using the [cache action](https://github.com/actions/cache).

This action takes a single parameter `isabelle-version` indicating the version of Isabelle that should be set up.
The following code shows how the action can be used within another Isabelle action to set up Isabelle 2024:
```yaml
- name: Set up Isabelle
  uses: gauravpartha/setup-isabelle@v1
  with: 
    isabelle-version: 2024

- name: Isabelle version
  run: isabelle version
```
