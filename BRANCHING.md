# Branching Strategy

## Source of truth

The "source of truth" for the codebase will always be the dev branch of the original project. For some projects, this is actually the `master` branch, others use `dev`, and others use something else.

**No commits will ever be made to this branch, and no pull requests will be made into that branch on our fork.**

This is so that we can:

- Always have a "clean" branch to start a new feature from.
- Merge in changes in the dev branch made to the original project, to keep ours up to date as we develop.

## Feature Branches

Before starting work on a new issue, you always first:

```
git checkout SOURCEOFTRUTH
git pull
```

This ensures you are always starting from the most up-to-date point. Then:

```
git checkout -b FEATURE
```

FEATURE will be replaced with the feature branch name for your issue. This will be in the format:

```
f-###-DESC
```

Where ### is the issue number you are working on, and DESC is some word or short phrase that describes the goal or work.

It's very important that the branches are named correctly, so that we don't accidentally have two developers name their branches the same and then do different work.
