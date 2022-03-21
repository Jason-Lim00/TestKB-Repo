# Listing the rules that would be run with 'semgrep --config auto' in the CLI

For any further usage of other options within the CLI, refer to our [<mark style="color:purple;">**CLI Command-line options reference page**</mark>](https://semgrep.dev/docs/cli-usage/).

{% embed url="https://semgrep.dev/docs/cli-usage" %}

To show what rules would be run when running something like `semgrep --config auto` or any other ruleset, use the `--verbose` option.

For example, when running `semgrep --verbose --config=p/ci [TARGET]`, the following would be output:

```
downloading config from https://cdn.semgrep.dev...
running 135 rules from 1 config remote-url_0
running 135 rules...
rules:
- go.lang.security.audit.crypto.bad_imports.insecure-module-used
- go.lang.security.audit.crypto.use_of_weak_crypto.use-of-DES
- go.lang.security.audit.crypto.ssl.ssl-v3-is-insecure
- go.lang.maintainability.useless-ifelse.useless-if-body
- java.lang.security.audit.crypto.no-null-cipher.no-null-cipher
...
...
...
```
