+++
date = "2017-02-24T17:05:05+01:00"
title = "Our Git Workflow"
+++

We use both Github and Bitbucket to host our code. Our git workflow is based on the use of branches and pull requests. When trying to add or change something significant in size, the expected workflow is as follows:

<!--more-->

1. Create a new branch, based on `master`.
2. Add commits to the branch. If needed, one can merge `master` into the branch to prevent merge conflicts later on. This is useful when development on the branch is taking a long time and `master` has significantly deviated from when the branch was started.
3. When the branch is in a finished state, the developer(s) submits a pull request. For this, we use Github because of its superior support:
  - **CI**: Github shows the status of the CI server. If some tests fail, Github will warn us.
  - **Reviews**: One can request reviews from other developers, which can then give comments both in general and relating to a specific line of code.
  - **Milestones**: A pull request can be coupled to a milestone in order to better track progress.
4. Based on the feedback, a developer can add more commits (which will show up in Github's interface)
5. When everyone (including the CI server) agrees, the branch is merged into `master` and deleted.

Although the pull requests themselves aren't visible in Bitbucket (they are not part of git), all branches, commits and merges are basic git features and will therefore be perfectly visible in Bitbucket.

Apart from the `master` branch and the feature branches, we have two other branches:

  * `original` is for the original code coming from the central stride repository on Bitbucket. When new functionality is released, this will get merged into `master`.
  * `blessed` will simply be a more stable version of `master`, updated every week.
