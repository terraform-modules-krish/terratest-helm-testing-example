***WARNING: THIS REPO IS AN AUTO-GENERATED COPY.*** *This repo has been copied from [Gruntwork’s](https://gruntwork.io/) GitHub repositories so that you can consume it from your company’s own internal Git repositories. This copy is automatically created and updated by the `repo-copier` CLI tool. If you need to make changes to this repo, you should make the changes in a separate fork, and NOT make changes directly in this repo, as otherwise, the `repo-copier` will overwrite your changes! Please see the `repo-copier` [documentation](https://github.com/terraform-modules-krish/repo-copier) for more information on how the code is copied, how cross-references are updated, how the changelog is handled, etc.*

***

_You may find it valuable to view the following resources in the original repo. If these links give you a 404, visit https://app.gruntwork.io to gain access or email support@gruntwork.io if you need assistance._

[Home Page](https://github.com/gruntwork-io/terratest-helm-testing-example/) |
[Pull Requests](https://github.com/gruntwork-io/terratest-helm-testing-example/pulls) |
[Issues](https://github.com/gruntwork-io/terratest-helm-testing-example/issues) |
[Releases and Assets](https://github.com/gruntwork-io/terratest-helm-testing-example/releases)

_Alternatively, you can view a copied version of the resources listed above._

[Pull Requests](https://github.com/terraform-modules-krish/terratest-helm-testing-example/blob/master/.github/PULL_REQUESTS.md) |
[Issues](https://github.com/terraform-modules-krish/terratest-helm-testing-example/blob/master/.github/ISSUES.md) |
[ChangeLog](https://github.com/terraform-modules-krish/terratest-helm-testing-example/blob/master/.github/CHANGELOG.md)

***

# Helm Chart Testing Example using Terratest

This repository contains the example code from the blog post ["Automated Testing for Kubernetes and Helm Charts using Terratest"](https://blog.gruntwork.io/automated-testing-for-kubernetes-and-helm-charts-using-terratest-a4ddc4e67344).

The directory structure represents a typical helm chart repository containing various charts in the `charts` directory
and the tests for those charts under the `test` directory. The `test` folder contains the corresponding terratest code
for testing each of the charts in the `charts` directory.

## Quickstart

### Prerequisites

To run the tests, you will need a working go install. See [here](https://golang.org/doc/install) for instructions on
installing go on to your platform. Make sure to use a version >=1.13.

### Kubernetes cluster

Some of the tests (specifically the integration tests) require a Kubernetes cluster to run. The easiest way to get a
Kuberenetes cluster is to use [`minikube`](https://kubernetes.io/docs/setup/minikube/), which is a local single node
installation of Kubernetes. Follow the instructions in the link to install and setup `minikube`.

Once `minikube` is installed, you will also need to install the helm client run the tests based on `helm install`.
Follow the [official guide](https://helm.sh/docs/intro/install/) for instructions on installing `helm`.

### Running the tests

To run the tests, first change directory to the `test` folder of this repository, and then use `go test` to run the tests:

```
cd test
go test -v .
```
