# Conventions

## Branch Naming Conventions

### Main Branch

- **Branch Name:** ``main``
- **Description:**
  - This is the default branch where the source code of ``HEAD`` always reflects a production-ready state.

### Feature Branches

- **Branch Name:** ``feature/{short-description}``
- **Description:**
  - These branches are used to develop new features for the upcoming releases.
  - A feature branch should always be created from the ``main`` branch.
  - Example: ``feature/user-authentication``

## Commit Conventions using Conventional Commits

[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) - A specification for adding human and machine readable meaning to commit messages.

### Overview

The commit message should be structured as follows:

```code
    <type>[optional scope]: <description>

    [optional body]

    [optional footer(s)]
```

The commit contains the following structural elements, to communicate intent to the consumers of your library:

fix: a commit of the type ``fix`` patches a bug in your codebase (this correlates with PATCH in Semantic Versioning).
feat: a commit of the type ``feat`` introduces a new feature to the codebase (this correlates with MINOR in Semantic Versioning).
BREAKING CHANGE: a commit that has a footer ``BREAKING CHANGE:``, or appends a ?? after the type/scope, introduces a breaking API change (correlating with MAJOR in Semantic Versioning). A BREAKING CHANGE can be part of commits of any type.
types other than ``fix:`` and ``feat:`` are allowed, for example [@commitlint/config-conventional](https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/config-conventional) (based on the Angular convention) recommends ``build:``, ``chore:``, ``ci:``, ``docs:``, ``style:``, ``refactor:``, ``perf:``, ``test:``, and others.
footers other than ``BREAKING CHANGE: <description>`` may be provided and follow a convention similar to git trailer format.
Additional types are not mandated by the Conventional Commits specification, and have no implicit effect in Semantic Versioning (unless they include a BREAKING CHANGE). A scope may be provided to a commit’s type, to provide additional contextual information and is contained within parenthesis, e.g., ``feat(parser): add ability to parse arrays``.
