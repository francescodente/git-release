# Git Release

A command line tool to simplify releases based on [semantic versioning](https://semver.org/) using Git and Annotated Tags.
This tool works on the assumption that a release is made by tagging a particular state of the repository with an annotated tag (`git tag -a`) and pushing it to the source repository. This tool increments one of the components of the current version (obtained via the `git describe` command) according to the rules of semantic versioning.

## Installation guide

Place the `git-release` file in any directory inside your system, then add the directory to the PATH environment variable.

## Command syntax
```
$ git-release <component-to-increment> [<remote-source>]
```
where `<component-to-increment>` is one of `major`, `minor` or `patch`.

## Examples

Assuming the current version is `v1.2.3`.

```sh
$ git-release major # Will tag the current commit with v2.0.0 and push to origin.
```

```sh
$ git-release minor # Will tag the current commit with v1.3.0 and push to origin.
```

```sh
$ git-release patch # Will tag the current commit with v1.2.4 and push to origin
```

```sh
$ git-release major myremote # Will tag the current commit with v2.0.0 and push to myremote
```
