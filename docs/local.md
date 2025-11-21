---
layout: default
title: Running locally (optional)
nav_order: 30
---
# Run a local instance of the workshop website
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

GitHub Pages uses Jekyll to turn markdown files into a website. This is done on GitHub's servers, so you can only see how the site will look after pushing your content to GitHub and waiting for GitHub to regenerate your site. 

If you prefer to check your work locally before making it public on GitHub you'll need to run Jekyll on your own computer. Some may prefer this workflow because you can experiment and see the results of your work immediately without affecting public pages.

This assumes you have already followed the steps in [Getting started](https://ubc-library-rc.github.io/rc-workshop-template) and have a local copy of your workshop repository (e.g. using _git clone_).


## 1. Install Ruby and Jekyll

Follow the guide for your operation system available from the [Jekyll installation page](https://jekyllrb.com/docs/installation/#guides). This will help you install Ruby and Jekyll.

## 2. Install Jekyll plugins

After Jekyll is installed, you will also need to install three plugins using the command line:  

```bash
$ gem install jekyll-seo-tag
$ gem install jekyll-remote-theme
$ gem install jekyll-include-cache
```

## 3. Generate the site
Now you can run any workshop site locally by changing to the `docs/` directory of the repository and running the terminal command `jekyll serve`
 
{: .note}
You may wonder why you can't just put `_config.yml` in the root directory and use `source: docs`, then run from the root directory. Well, technically you *can*, but only for a local installation (ie, `jekyll serve`). Github Pages overrides some of the `_config.yml` options, and `source` is one of them. While there is nothing prohibiting you from putting a `_config.yml` into your root directory, if you *do*, **do not** push it to Github. Add it to the `.gitignore` file.

The terminal output will include the local "Server address" (usually `http://127.0.0.1:4000`). `localhost` is usually a synonym for `127.0.0.1`, so you can almost always use `http://localhost:4000`. Paste or type this address into any web-browser to view the site locally. Note that it's **http**, not **https**. 

As long as `jekyll serve` is running the site will update when you save changes to your local files (press _ctrl-c_ to stop serving). That's changes to the Markdown files. If you change `_config.yml`, you will need to restart `jekyll serve`.

Once you're satisfied with your local changes use git to push your commits to GitHub. The changes will appear on the public workshop site within a few minutes.

{: .note}
Jekyll creates two directories in your local repository: _.jekyll-cache/_ and *_site/*. These are only required to serve the site locally. Do not `git add` these directories or push them to GitHub. The default `.gitignore` file already has these, but you should endure that you do not add these files.

