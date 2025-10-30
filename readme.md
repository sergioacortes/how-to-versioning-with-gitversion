# How to version with gitversion

This repository intend to explain the use of GitVersion as a solution con manage the version through PR/CI pipelines.

GitVersion is a tool that use the git repository history to calculate a [Semantic Version Number](https://semver.org/).

The version number generated can be used for different purposes, such as:

1. Stamping a version number to the compiled assemblies.
2. Stamping a version number on artifacts.
3. Expose the version number to set the build version.

GitVersion can be use on different ways

1. Continous integration server pipeline like Azure DevOps or GitHub actions.
2. Command line interface
3. MSBuild task
4. Nuget package library
5. Docker

In this example we are goint to focus on Continous Integration pipeline and command line interface

## Create gitversion configuration

In this repository you can find a Gitversion.yaml file configure to version using Trunk Based Development strategy.

For more information about Trunk Based Development read the following [AWS guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/choosing-git-branch-approach/trunk-branching-strategy.html).

## PR Pipeline

Under the .github folder you can find the workflows folder. 

In this repo we are going to work with the following workflows

* Pull request
* Continous integration
* Continous deployment

For more information about github actions, please refer the to [Official Documentation](https://docs.github.com/es/actions/get-started/quickstart)