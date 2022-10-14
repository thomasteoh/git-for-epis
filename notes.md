# Introduction

`git` is a free tool to do version control

Version control allows us to save checkpoints of our files and to back them up 
on the `git` repository provider.

There are many services online that provide git repository hosting, often with 
most basic functionality available for free. Github and Azure DevOps are 
examples of such services.

Used very commonly in software development circles but doesn't mean we can't use it as well!


# `git` and epidemiology

`git` is particularly useful for anything stored as plain text

- Code
- Notes
- Configurations

Facilitates collaboration by centralising and organising codebase

Provides mechanisms for working concurrently, resolving conflicts, identifying 
changes and reverting problematic code

Opens the door to automations and other cool things! 🚀

# Getting started

Install `git`

- Windows: download the `git-scm` package
- Mac: download the `git-scm` package
- Linux: from your package manager 
    - e.g. `sudo dnf install git` or `sudo apt-get install git`

Sign up for access to a `git` service.

[Optional] Install a `git` compatible code editor or IDE

## Initial configuration

A few steps need to be done before you are able to start working with `git`

### Authorise access from your computer

Usually two options, a personal access token or using SSH key-pairs

- Personal access token: generate this on your `git` service
    - Use it like a password
    - You can save this PAT in a keyring to reuse
- key-pair: generate this in your development environment and save in service
    - Authentication automatically occurs when connecting via `ssh`

### Set `git` configuration locally

So that `git` can ascribe commits to you when you make them

Only have to do once

```
git config --global user.name "Your Name"
git config --global user.email "youremail@yourdomain.com"
```

# Clone a repository

If a repository already exists that you want to access, navigate to it online 
and find the instructions on the web interface to clone the repository.

Take the details that you find and use...

```
git clone <repository>
```

... to clone the entire thing


# Committing changes to the repository

Committing your changes is a manual process that involves identifying that you 
have made a change (or partial change!) and describing the work that you've 
done.

This is typically completed in a few steps as follows...


## Identify changed files

You can also see through this process what within each file has changed, if they
are a plain text file. This can be useful for checking the code is changed as
intended and can help you when providing comments to your commit.

```
git status
git log
```

A condensed version can be seen using the following

```
git log --pretty=oneline
```

## Stage your changes

Add the files that you have changed so that they are ready for you to capture in 
your commit. 

```
git add <filename>
```

If you would like to stage all changes you can use the following command

```
git add --all
```

> ⚠️ Note
> 
> Only saved changes in files will be able to be staged, make sure you save
> 
> Staging your changes won't commit them, that comes next

## Commit your changes

When you have finished staging your changes so that they are prepared, commit
them to the tree.

```
git commit
```

This will open up a text editor for you to provide comments about what tasks
have been done or actions taken

Make sure you provide enough context here to give you a good description of
what code changes you have made

You can also commit changes inline

```
git commit -m "Your commit message here"
```

# Using branches to encapsulate your work

Branches are pointers to a snapshot and are useful for encapsulating your 
changes. They are also useful to ensure that contributions from multiple users
are able to be tracked and integrated safely

A list of all the branches in your repository can be obtained using the 
following command

```
git branch
```

## Create a branch

Using the current active branch as the template, you can create a new branch
to start working on your fixes or features

```
git branch <branch>
```

After you create the branch you will need to switch to it by checking it out
before you start making changes; you can use the following command

```
git checkout
```

## Compare changes across branches

After you've finished putting in your changes and made your commits in your 
feature branch, you can see how it differs from another branch by issuing the
following command

```
git diff main..<branch>
```

This is useful to do to work out what overall changes may be occurring were
the code bases to be merged

## Merging branches

We may want to move the updates and improvements in your feature branch into
the main branch so that they can be used by others. To do this we can 
raise a pull request, which triggers a review and merge process. This checking
process is important to ensure that code to be incorporated is of good quality.

### Raise a pull request

GitHub demo


# Common things to look out for

Not all data is appropriate to store in a `git` repository

Try to keep on top of commits, or it may get overwhelming managing many
changes

Don't store build artifacts, data or secrets in your git repository

You may need to do an offline merge to resolve merge conflicts before reraising
a pull request
