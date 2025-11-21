---
layout: default
title: Formatting Markdown 
nav_order: 5
description:
---

## Selected text formatting options
Below are some formatting options that may be useful in RC workshop sites. For more configuration options see [Just the Docs](https://justthedocs.com/) documentation.

The `generic_content.md` that comes with a blank template contains examples of these as well, so don't panic if you forget where this page is.

### Callouts

Use this syntax...

```  
{: .note}
Wash your hands frequently
```
... to include a note that will look like this on the workshop website:

{: .note}
Wash your hands frequently


```
{: .warn}
Don't step on the snails!
```
{: .warn}
Don't step on the snails!

```
{: .prereq}
Basic slug identification; comfortable in the woods.
```

{: .prereq}
 Basic slug identification; comfortable in the woods.

### Step-by-step instructions
```
{: .label .label-step}
Step 1
{: .step}
Do this thing

{: .label .label-step}
Step 2
{: .step}
Do this other thing

```

{: .label .label-step}
Step 1
{: .step}
Do this thing

{: .label .label-step}
Step 2
{: .step}
Do this other thing


### Terminal input/output

Sometimes it's helpful to distinguish between what a workshop participant should input into the terminal or command line, and what they should expect as output. This code for an input...

~~~
Input
{: .label .label-green }
```sh
$ git status
```
~~~
... will appear like this in the workshop website:

Input
{: .label .label-green }
```sh
$ git status
```

Similarly, this code shows the output from a command:

~~~
Output
{: .label .label-yellow }
```sh
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean
```
~~~

Output
{: .label .label-yellow }
```sh
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean
```

### Code block syntax highlighting  
Add syntax highlighting to code blocks by specifying the language after the three backticks at the beginning of a block. The example below is for markdown (md). Other syntax options include _html, xml, js, py, sql, sh, yaml_, and many more.

~~~
```md
Code block with [markdown](https://markdownguide.org) syntax highlighting.
```
~~~

```md
Code block with [markdown](https://markdownguide.org) syntax highlighting.
```


### Circled numbers

This synax...

```
*1*{: .circle .circle-blue} Number in normal text
```
...will look like this:

*1*{: .circle .circle-blue} Number in normal text

You can also use this in headers, lists and other markdown suported elements, e.g.,

```
* *1*{: .circle .circle-blue} `.circle-blue`
* *2*{: .circle .circle-red} `.circle-red`
* *3*{: .circle .circle-yellow} `.circle-yellow`
* *4*{: .circle .circle-green} `.circle-green`
* *5*{: .circle .circle-purple} `.circle-purple`

## *2*{: .circle .circle-red} Number in h2

### *10*{: .circle .circle-yellow} Number in h3
```

...will look like this:

* *1*{: .circle .circle-blue} `.circle-blue`
* *2*{: .circle .circle-red} `.circle-red`
* *3*{: .circle .circle-yellow} `.circle-yellow`
* *4*{: .circle .circle-green} `.circle-green`
* *5*{: .circle .circle-purple} `.circle-purple`

## *2*{: .circle .circle-red} Number in h2
{: .no_toc }

### *10*{: .circle .circle-yellow} Number in h3
{: .no_toc }

### Dropdowns

To create hidden content in a dropdown use this:

~~~
<details>
<summary>This is the dropdown title</summary>
<br>
This is the hidden dropdown content.
</details>
~~~

<details>
<summary>This is the dropdown title</summary>  
<br>
This is the hidden dropdown content.
</details>  
<br />  
If you want it open by default:
~~~
<details ope
<summary>This is the dropdown title</summary>
<br>
This is the dropdown content that you can hide if you want to.
</details>
~~~

### Table of contents
See [In-page navigation with Table of Contents](https://pmarsceill.github.io/just-the-docs/docs/navigation-structure/#in-page-navigation-with-table-of-contents) for options to add a TOC within a page (like at the top of this page).
