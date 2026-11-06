# Automated Testing in C

A Software Tools lab at the University of Bristol exploring automated testing and continuous integration using C, Unity, Git hooks and GitHub Actions.

## Overview

This project uses a simple calculator to demonstrate how unit tests can be integrated into a development workflow.

The lab covers:

- Writing unit tests using the Unity testing framework.
- Automatically running tests before Git commits.
- Configuring continuous integration with GitHub Actions.
- Identifying test failures and compilation errors.

## Technologies

- **C** — calculator implementation
- **Unity** — unit testing framework
- **Git** — version control and pre-commit hooks
- **GitHub Actions** — continuous integration
- **Clang / GCC** — C compilers

## Running the Tests

Install the [Unity testing framework](https://github.com/ThrowTheSwitch/Unity).

On macOS, with Unity installed under the Homebrew prefix:

```bash
clang -I"$(brew --prefix)/include/unity" \
      -L"$(brew --prefix)/lib" \
      -o tests test.c -lunity

./tests
```

## Automated Testing

### Pre-commit Hook

A local Git hook compiles and runs the test suite before each commit. Failed compilation or tests prevent the commit from being created.

### GitHub Actions

The GitHub Actions workflow automatically builds and tests the project whenever changes are pushed to the `main` branch.

The workflow runs on Ubuntu using GCC and the Unity testing framework.

## Learning Outcomes

This lab demonstrates the fundamentals of unit testing, automated testing, Git hooks and continuous integration.

## Acknowledgements

Based on a Software Tools lab exercise at the University of Bristol.

## Licence

Licensed under the MIT License. See [LICENSE](LICENSE) for details.