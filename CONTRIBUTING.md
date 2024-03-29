# Contributing to pipelines-examples

:+1::tada: First off, thank you for taking the time to contribute! :tada::+1:

This page contains information about reporting issues as well as some tips and guidelines useful to experienced open source contributors.

## Reporting issues
A great way to contribute to the project is to send a detailed report when you encounter an issue. I always appreciate a well-written, thorough bug report, and will thank you for it!

Check [issue database](https://github.com/valeriano-manassero/helm-charts/issues) doesn't already include that problem or suggestion before submitting an issue. If you find a match, you can use the "subscribe" button to get notified on updates. Do not leave random "+1" or "I have this too" comments, as they only clutter the discussion, and don't help resolving it. However, if you have ways to reproduce the issue or have additional information that may help resolving the issue, please leave a comment.

## Contributing code
Pull requests are always welcome! Not sure if that typo is worth a pull request? Found a bug and know how to fix it? Do it! I appreciate the help. Any significant improvement should be documented as [a GitHub issue](https://github.com/valeriano-manassero/helm-charts/issues) before starting working on it.

### Pull Requests

Before you submit a new PR:

* Check your branch with `helm lint`
* Update `version` in `Chart.yaml` according [semver](https://semver.org/) rules
* Substitute `annotations` section in `Chart.yaml` annotating implementations (useful for Artifecthub changelog)
* Update chart README using [helm-docs](https://github.com/norwoodj/helm-docs)

In your PR include:

* A reference to the issue it addresses
* A brief description of the approach you've taken for implementing
