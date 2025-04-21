# testkube-poc

A PoC for the Test Framework TestKube.

## Getting Started

### Prerequisites

- MacOS or Linux
- Docker
- [KSail](https://github.com/devantler-tech/ksail)
- [TestKube CLI](https://docs.testkube.io/articles/install/cli)

### Usage

Setup the test cluster with KSail:

```bash
# Ensure your working directory is at the root of the project
ksail up
```

Now TestKube is installed and running on a local Kind cluster, and a simple test is created for checking the health of the podinfo service.

You can now run the test using the TestKube CLI:

```bash
# Ensure your current kubernetes config and context is set to the Kind cluster
# The test is located at k8s/apps/podinfo/tests/health-check-test.yaml
testkube run testworkflow podinfo-health-check-test -f
```

That's it! You should see the test result in the terminal.

## Want to learn more?

TestKube supports a many, many different test types. Check the docs for more information on how to create and run tests:

- [TestWorkflow examples](https://docs.testkube.io/articles/test-workflows-examples-basics)
- [Running tests](https://docs.testkube.io/articles/test-workflows-creating)
