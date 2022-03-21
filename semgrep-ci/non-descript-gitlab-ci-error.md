# Non-descript Gitlab CI error

Seeing something like this in your GitLab CI pipeline?&#x20;

```
$ semgrep-agent
| versions          - semgrep 0.81.0 on Python 3.9.10
| environment       - running in environment gitlab-ci, triggering event is 'pull_request'
| manage            - not logged in
=== setting up agent configuration
| using semgrep rules from https://semgrep.dev/c/p/security-audit
| using semgrep rules from https://semgrep.dev/c/p/secrets
An unexpected error occurred:
 <class 'sh.ErrorReturnCode_1'> 
  RAN: /usr/bin/git merge-base --all b7cb3f8e678d943b4cded2e55d45221fafbde030 FETCH_HEAD
  STDOUT:
  STDERR:
```

You might be setting the <mark style="color:purple;">**git\_depth**</mark> variable to something too low:

```
variables:
  GIT_DEPTH: 1 
```

Semgrep needs to fetch commit history to do a diff-aware scan between the source and target branch, so limiting the <mark style="color:purple;">**git\_depth**</mark> might be the cause of some merge-related errors.
