---
layout: default
title: Generic content 
nav_order: 30
---
# Generic content page 

Fill these pages with workshop content. Your life will be easier if you name your file(s) in the format:

`[nav_order]_[description].md`

`nav_order` should match `nav_order` in the header of this file, and `description` is just the description. Note that you don't *have* to do this, it's just a a suggestion.

Fill this page with any markdown or HTML that you need. You can even mix and match markdown with html!

**Here are some handy snippets of code that you can copy/paste as required.**

### Line breaks

Line breaks can be indicated with<br />
Alternately, you can break a line  
by putting two spaces at the end. It is hard to see but easy to read.

### Code blocks.

Append the type of code to the end of the first backtick.

#### Large code block
```md
---
layout: default
title: Generic content 
nav_order: 30
---
```

For terminal outputs, use backticks with `sh`:

```sh
$echo "I have no idea what I am doing."
I have no idea what I'm doing 
```

And with no highlighting:

```no-highlight
$echo "I have no idea what I am doing."
I have no idea what I'm doing 
```

#### Small code block

Use single backticks `to indicate code`

### Coloured circles 

* *1*{: .circle .circle-blue} `.circle-blue`
* *2*{: .circle .circle-red} `.circle-red`
* *3*{: .circle .circle-yellow} `.circle-yellow`
* *4*{: .circle .circle-green} `.circle-green`
* *5*{: .circle .circle-purple} `.circle-purple`
## *2*{: .circle .circle-red} Number combined with a header

### Callouts of various kinds

A note. Note that the tag is on a different line.
{: .note}

A warning
{: .warn}

A prerequisite
{: .prereq}

### Steps in order

Step one
{: .label .label-step}

Instruction goes here
{: .step}

Step two
{: .label .label-step}

Further instructions
{: .step}


### Coloured labels

Red label
{: .label .label-red}

Green label
{: .label .label-green}


### Dropdowns
#### Closed
<details>
<summary>This is the dropdown title</summary>
This is the hidden dropdown content. There are two spaces at the end of the previous line to insert a line break.
</details>

---

Use three (or more) dashes for horizontal lines

---

#### Open
<details open>
<summary>This dropdown is open</summary>  
This is the dropdown content. Same line break as above.
</details>

