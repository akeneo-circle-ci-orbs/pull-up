# Description

This orbs is useful to merge a branch into another one push the result in a PR for approval. It can also notify on Slack if the merge is susccessful or not.

# Use case

It allows to pull up fixes done in one branch to another one, automatically, when there is no merge conflict. For example, it can pull up a fix merged in branch 1.0 in the branch 2.0.

Of course, if there is an unresolvable conflict, the merge have to be done manually. In that case, the slack notification will warn the user in that case.

# Deployment

It automatically increments the patch version and publishes the orb when merging a PR in the `main` branch.For example, if there is an existing version `1.0.0`, the next PR merged in `main` branch will create a new orb version `1.0.1`.

If there is a new feature that doesn't break anything for the users using this orb, please publish manually in your CLI a new minor version (such as 1.1.0).
If there is a new feature that breaks something for the users using this orb, please publish manually in your CLI a new major version (such as 2.0.0).
