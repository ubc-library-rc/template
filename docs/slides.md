---
layout: default
title: Publishing slides
nav_order: 10
description:
---

# Publishing slides with reveal.js
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


Workshop sites can include slides in [reveal.js](https://revealjs.com/) format. Slides can be presented in the same tab, a separate tab, or even embedded into a page. You can even embed a slide presentation into a slide presentation if you want to, but that way lies madness. 

There is already a template page with sample presentations, ready to edit. It's called `slide_presentation.md`, and links to:

* The newer, better way of making presentations with Markdown, in light and dark themes
* The older, more complicated way of making presentations in HTML, in light and dark themes

Plus, it outlines how to have things in a new tab or embedded in a page.

Presentations are encapsulated in their own directory, called `slide_framework`, but you can easy link to them from a Markdown page in the `docs/` directory. It's what the sample page does.

The structure of presentations:

|File/directory| Purpose|
|--------------|--------|
|docs/slide_presentation.md| A page that links to presentations - an example|
|docs/slide_framework/| Directory holding reveal.js presentations|
|docs/slide_framework/custom/|Directory holding custom CSS for presentations|
|docs/slide_framework/images/|Directory to hold presentation images|
|docs/slide_framework/presentation_markdown|Directory which holds the *Markdown* of the presentation|
|docs/slide_framework/presentation_framework*[md]*.html/|Frameworks for Markdown presentations|
|docs/slide_framework/presentation_framework*html.html/|Frameworks for HTML presentations|
|docs/slide_framework/presentation_markdown/markdown_template.md|Sample file for you to copy/edit; the meat/main vegetable of the presentation|

## How to guide
### Markdown version
Despite *mostly* using Markdown, you will still need a tiny bit of HTML. 

* In the `slide_framework` directory, select which Markdown presentation you would like to use (ie, light or dark. These correspond to `presentation_framework_md.html` and `presentation_framework_dark_md.html`. It you want your html page to have an interesting name, you can rename it.

    * Edit the `<title>` section (line 14)
    * Edit the relevant `<section>` blocks to point to your Markdown file (line 39). You probably only need one section but you can have as many as you want.

Now it's only Markdown and adding images.

* Images get put into `docs/slide_framework/images`
* The Markdown for your presentation is held in `docs/slide_famework/presentation_markdown/`. The sample file has examples of how to do typical presentation things.

### HTML version

* Edit either `presentation_framework_html.html`  or `presentation_framework_dark_html.html` to make a reveal.js presentation using only HTML and JavaScript. Enjoy! 

## Generate PDF of slides
See <https://revealjs.com/pdf-export/> for instructions on exporting reveal.js slides to PDF. (Some formatting may be lost in the export.). Generally, though, you can just print the presentation page and it works reasonably well.

## Where to get help

The main help for reveal.js is, of course, [its website](https://revealjs.com/markdown/). Important sections include:

* [Markdown](https://revealjs.com/markdown/)
* [Markup](https://revealjs.com/markup/), or the HTML section
* [Fragments](https://revealjs.com/fragments/), in case you need to do fancy bullet points


