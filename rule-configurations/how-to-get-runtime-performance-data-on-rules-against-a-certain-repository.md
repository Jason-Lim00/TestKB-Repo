# How to get runtime performance data on rules against a certain repository?

Inside of the [<mark style="color:purple;">**CLI Command-line options reference page**</mark>](https://semgrep.dev/docs/cli-usage/) exists a `--time` flag that allows one to generate timing output for each rule that is run.&#x20;

{% embed url="https://semgrep.dev/docs/cli-usage" %}

If used in conjunction with the `--json` flag for output would provide times for each (rule, target) pair.
