# Guaranteeing full scans on CI

With all CI config files, the field <mark style="color:purple;">**`SEMGREP_BASELINE_REF:`**</mark> is the main source for <mark style="color:purple;">**diff-aware scanning**</mark>.&#x20;

For example, if you were to put your main branch as the parameter, Semgrep would run diff-aware scans between the changed branch and the main branch. Therefore, to guarantee full scans, you should remove <mark style="color:purple;">**`SEMGREP_BASELINE_REF:`**</mark>altogether**.**
