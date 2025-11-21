---
layout: default
title: Technical notes 
nav_order: 30
description:
---

## How to perform technical tasks with git

### Updates to Just the Docs

UBC has some customizations to [Just the Docs](https://just-the-docs.com), but we still want to keep everything up to date. We do this by serving content from a different branch, so we can have the default theme, our UBC theme, or anything else we need but still manage to keep things up to date.

There are a few technical steps.

Because we are using a fork of Just the Docs, we must link to it so that we can pull updates. Note that this refers to the `rc-theme` repo at <https://github.com/ubc-library-rc/rc-theme>, **not** the template repo.

Ensure that you have the upstream repo available. Your `origin` may look different; don't worry about it.

```zsh
git remote -v
origin	ssh://git/ubc-library-rc/rc-theme (fetch)
origin	ssh://git/ubc-library-rc/rc-theme (push)
upstream	https://github.com/just-the-docs/just-the-docs (fetch)
upstream	https://github.com/just-the-docs/just-the-docs (push)
```

If you don't have `upstream`:

```
git remote add upstream https://github.com/just-the-docs/just-the-docs
```

Checkout the UBC branch (or whichever branch you wish to use):
```
git checkout ubc
```

Pull the main Just the Docs repo

```
git fetch upstream
```

Merge the changes into the branch

```
git merge upstream/main
```

Ideally, there will be no merge conflicts but how to deal with those is beyond the scope of this. Assuming all is well:

```
git push origin ubc
```

Done!

### Managing your reveal.js installation

#### Getting reveal.js code to work with a local jekyll installation
By default, the template comes with a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) which is a link to the code of [reveal.js](https://revealjs.com/). What this means, in practice, is that when you copy or pull the repository, the reveal.js code is not copied locally; there's just an empty directory. While this behaviour is normal, it makes difference when you try to test your reveal.js presentation locally using `jekyll serve`.

You may want or need to intialize the code for reveal.js, and get its code to your computer (instead of a just a link on Github). To do this you can perform the following:

```
git submodule init
git submodule update
```

**This will download the code into your local files so that you can run `jekyll serve`.** For more detailed information, see the [Atlassian Git section on submodules.](https://www.atlassian.com/git/tutorials/git-submodule)

{: .important}
From the site above: "A Git submodule is a record within a host Git repository that points to a specific commit in another external repository. Submodules are very static and only track specific commits. Submodules do not track Git refs or branches and are not automatically updated when the host repository is updated."

You can use a specfic commit of reveal.js if you need to by changing to the reveal.js directory and performing a `git checkout`. For example, assuming you are already in the `docs/` directory and you need commit 622c734:

```zsh
cd reveal.js
$ git checkout 622c734
```
switch back to the most current release with:

```zsh
$ git checkout [master/main/whatever branch you need]
```

Don't forget to commit your changes, because in this case Github needs to know where to point everything.

#### Updating reveal.js

Like the Just the Docs theme, reveal.js needs periodic updating. This will normally be done as a above with `git checkout [whatever branch]`, or `git pull origin master`. We are, under normal circumstances, not making any changes to the reveal.js framework, so you can just keep pulling any changes, hopefully none of which will break anything.
 
