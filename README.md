# Exercise - Git Pull Requests

We're going to learn how to make pull requests on GitHub. This will be how you request feedback going forward.

## Contents <!-- omit in toc -->

- [What Is A Pull Request](#what-is-a-pull-request)
- [The Submission Flow](#the-submission-flow)
- [Practicing Pull Requests](#practicing-pull-requests)
  - [Fork And Clone This Repository](#fork-and-clone-this-repository)
  - [Create `hello.txt`](#create-hellotxt)

## What Is A Pull Request

Pull requests are the main channel multiple developers use to collaborate on a single project. If one developer has changes they want to contribute to a project, they:

1. Create a new branch called, e.g., `cool-feature`
1. Make any changes they want to add to the main project on that new branch.
1. Submit request to merge their changes in `cool-feature` into `master` — this is the **pull request**
1. The team is notified that someone has opened a pull request.

## The Submission Flow

Let's say we're working on the [JavaScript Fundamentals I][github-fundamentals-i] exercises. This would be the flow (we'll share the git commands later):

1. Fork the main project/exercise repository to create your own copy
1. Start working on an exercise or iteration, e.g., the `isPrime` function.
1. Create a new branch on your copy and give it a sensible name like `is-prime`
1. Do the `isPrime` exercises, which might involve many commits, but they all live on the `is-prime` branch
1. Open a pull request to merge `is-prime` into **YOUR** forks's `master` branch.
1. Go to the pull request page and request a code review from an instructor. This is built into GitHub.

The feedback will happen on the pull request.

This process is called the *[feature branch workflow][atlassian-feature-branch-flow]* and is the most commonly used workflow for teams collaborating on a single repository.

1. Each new feature starts on its own branch (the so-called **feature branch**).
1. When the feature is ready, a pull request is submitted to merge the feature branch into the `master` branch.
1. A code review happens
1. If something need to be changed based on the review, those
1. Once everything looks good, the feature branch is merged into `master`.

## Practicing Pull Requests

### Fork And Clone This Repository

First, fork this repository to create your own copy.

Next, clone **your fork** using the `git clone` command. This will create a copy of your repository on your computer (called a *local copy*).

**Note**: Replace `YourGitHubUsername` with your *actual* GitHub username.

```console
git clone https://github.com/YourGitHubUsername/exercises-git-pull-request.git
```

This will create a directory named `exercises-git-pull-request` inside the current working directory. Enter the directory with the following command:

```console
cd exercises-git-pull-request
```

### Create `hello.txt`

**Note**: Remember to use commands like `ls` and `pwd` to verify you're in the correct directory and looking at the right files.

Inside `exercises-git-pull-request`, create a file named `hello.txt` that contains the following text:

```text
This is my first pull request!
```

Make sure to save the file.
