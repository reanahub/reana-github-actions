# REANA-GitHub-Actions

[![image](https://github.com/reanahub/reana-github-actions/workflows/CI/badge.svg)](https://github.com/reanahub/reana-github-actions/actions)
[![image](https://img.shields.io/badge/discourse-forum-blue.svg)](https://forum.reana.io)
[![image](https://img.shields.io/github/license/reanahub/reana-github-actions.svg)](https://github.com/reanahub/reana-github-actions/blob/master/LICENSE)

## About

REANA-GitHub-Actions provides CI actions that can be used in multiple GitHub repositories.

## Features

- validate the REANA specification file of demo examples
- execute demo examples
- build and publish the container images of REANA's cluster components

## Usage

To use one of the actions, simply reference it from the YAML specification file of the CI workflow.
For example, to validate the `reana.yaml` file of a demo example, you can add the following job to the workflow:

```yaml
validate:
  runs-on: ubuntu-24.04
  steps:
    - name: Checkout
      uses: actions/checkout@v3

    - name: Validate workflow spec
      uses: reanahub/reana-github-actions/local-validate@v1
      with:
        reana_specs: reana.yaml
```

To find out which inputs are accepted by each action, please have a look at the corresponding `action.yml` file.

## Useful links

- [How to create composite actions](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action)
- [REANA project home page](http://www.reana.io/)
- [REANA user documentation](https://docs.reana.io)
- [REANA user support forum](https://forum.reana.io)
- [REANA-GitHub-Actions known issues](https://github.com/reanahub/reana-message-broker/issues)
- [REANA-GitHub-Actions source code](https://github.com/reanahub/reana-message-broker)
