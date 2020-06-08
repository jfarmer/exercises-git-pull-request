# Exercise - Git Pull Requests

We're going to learn how to make pull requests on GitHub. This will be how you request feedback going forward.

## Contents <!-- omit in toc -->

- [What Is A Pull Request](#What-Is-A-Pull-Request)
- [The Submission Flow](#The-Submission-Flow)
- [Practicing Pull Requests](#Practicing-Pull-Requests)
  - [Fork And Clone This Repository](#Fork-And-Clone-This-Repository)
  - [Create A Feature Branch](#Create-A-Feature-Branch)
  - [Create `hello.txt`](#Create-hellotxt)
  - [Commit `hello.txt`](#Commit-hellotxt)
  - [Create And Commit `goodbye.txt`](#Create-And-Commit-goodbyetxt)
  - [Push Your Local Changes Up To GitHub](#Push-Your-Local-Changes-Up-To-GitHub)
  - [Create A Pull Request](#Create-A-Pull-Request)
- [Requesting Code Review](#Requesting-Code-Review)
- [Merging Pull Request](#Merging-Pull-Request)

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

We're going to create a pull request that contains two individual commits involving different files.

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

### Create A Feature Branch

When we're inside a git repository, there is always an "active" branch. To see a list of all the branches run:

```console
git branch
```

The active branch is whichever one is prefixed with `*`. Because `master` is the only branch, you should see:

```console
$ git branch
* master
$
```

Let's create a new branch and switch to it. Run the following:

```console
git checkout -b first-feature
```

Run `git branch` again and you should see:

```console
$ git branch
* first-feature
  master
$
```

### Create `hello.txt`

**Note**: Remember to use commands like `ls` and `pwd` to verify you're in the correct directory and looking at the right files.

While on the `first-feature` branch, create a file named `hello.txt` that contains the following text:

```text
Hello! This is my first pull request.
```

Make sure to save the file. In the console, run the following command:

```console
git status
```

This gives you information about the current state of your git repository. It will show you which files have been modified, which files are new and have yet to be committed, etc.

Run the following `git add` command:

```console
git add hello.txt
```

Run `git status` again to see how the output changed.

### Commit `hello.txt`

Run the following command to create a new commit:

```console
git commit -m 'hello.txt is a lovely file'
```

Run `git status` and note how the output has changed.

### Create And Commit `goodbye.txt`

Let's create a second commit.

Create a file named `goodbye.txt` that contains the following text:

```text
Goodbye! About to submit my first pull request.
```

Again, run `git status` to see how the output has changed. Add and commit `goodbye.txt`.

To add it:

```console
git add goodbye.txt
```

Run `git status` and note how the output changed.

To commit it:

```console
git commit -m 'Time to say goodbye'
```

Run `git status` and note how the output changed.

### Push Your Local Changes Up To GitHub

Right now, your branch exists on your machine but doesn't yet exist on GitHub. To simultaneously push your changes up to GitHub and create the branch on GitHub, run the following command:

```console
git push --set-upstream origin first-feature
```

Here `origin` refers to GitHub.

Now visit your repository on GitHub.com!

### Create A Pull Request

On GitHub, you should see the following: <https://share.getcloudapp.com/YEud6DE4>

Click the **Compare & Pull Request**. On the next page, click **Create Pull Request**.

Ta-da, first pull request!

## Requesting Code Review

You have two ways to request a code review:

1. Add one or more instructors as collaborators on your project and then select them from the "Request Review" dropdown
1. Leave a comment `@`-mentioning anyone you want a code review from. If you want a review from GitHub user `SnorkleFish` then leave a comment that looks like:

   ```text
   @SnorkleFish I'd like a review!
   ```

## Merging Pull Request

Once you're ready to go, merge your pull request into the `master` branch. Don't wait for a review to merge unless you think it's critical.

[github-fundamentals-i]: https://github.com/jfarmer/exercises-javascript-fundamentals
[atlassian-feature-branch-flow]: https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow
