# Introduction

`git` is a tool to do version control

Version control allows us to save checkpoints of our files and to back them up on the `git` repository provider.

There are many services online that provide git repository hosting, often with most basic functionality available for free. Github and Azure DevOps are examples of such services.

Used very commonly in software development circles but doesn't mean we can't use it as well!


# `git` and epidemiology

`git` is particularly useful for anything stored as plain text

- Code
- Notes
- Configurations

Facilitates collaboration by centralising and organising codebase

Provides mechanisms for working concurrently, resolving conflicts, identifying changes and reverting problematic code

Opens the door to automations and other cool things! 🚀

# Getting started

Install `git`

- Windows: 
- Mac: 
- Linux: from your package manager e.g. `sudo dnf install git` or `sudo apt-get install git`

Sign up for access to a `git` service.

[Optional] Install a `git` compatible code editor or IDE

## Initial configuration

### Authorise access from your computer

Usually two options, a personal access token or using SSH key-pairs

- Personal access token: generate this on your `git` service, and use it like a password
- SSH key-pairs: generate this in your development environment, the save the key to your `git` service

### Set `git` configuration locally

So that `git` can ascribe commits to you when you make them

Only have to do once

```
git config --global user.name "Your Name"
git config --global user.email "youremail@yourdomain.com"
```

# Clone a repository

If a repository already exists that you want to access, navigate to it online and find the instructions on the web interface to clone the repository.

Take the details that you find and use...

```
git clone <repository>
```

... to clone the entire thing


# Committing changes to the repository

# Using branches to encapsulate your work

# Common things to look out for

Data and secrets