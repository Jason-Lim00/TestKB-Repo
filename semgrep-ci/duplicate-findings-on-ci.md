# Duplicate findings on CI

Duplicate findings in CI are due to a misconfiguration of diff scans vs. a full scans.

The same rule and code will produce a finding for every branch it is found on. This is why we recommend doing diff scans on PR's and full scans only on the main branch.

Refer to our [<mark style="color:purple;">**CI docs**</mark>](https://semgrep.dev/docs/semgrep-ci/overview/) for more info regarding how to set up diff scans or full scans.

{% embed url="https://semgrep.dev/docs/semgrep-ci/overview" %}
