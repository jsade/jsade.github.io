---
layout: post
created: "2025-02-23T23:26"
updated: "2025-02-23T23:39"
title: "Markdown Test"
date created: "2025-02-23 23:26:58"
date modified: "2025-02-23 23:39:23"
date: 2025-02-23 21:26:58 +0000
tags:
  - do
---

<!--
This file was automatically converted by Jekyll Publisher for Obsidian.
https://github.com/jsade/obsidian-jekyll-plugin

Version: 1.0.0
Conversion date: 2025-02-23 21:40:32 +0000
-->


## Inline code

This is an example of `Inline Code`.

## Filepath

Here is the `/path/to/the/file.extend`{: .filepath}.

## Code blocks

### Common

```text
This is a common code snippet, without syntax highlight and line number.
```

### Specific Language

```bash
if [ $? -ne 0 ]; then
  echo "The command was not successful.";
  the needful / exit
fi;
```

### Specific filename

```sass
@import
  "colors/light-typography",
  "colors/dark-typography";
```

{: file='_sass/jekyll-theme-chirpy.scss'}

## Mathematics

The mathematics powered by [**MathJax**](https://www.mathjax.org/):

$$
\begin{equation}
  \sum_{n=1}<sup>\infty 1/n</sup>2 = \frac{\pi^2}{6}
  \label{eq:series}
\end{equation}
$$

We can reference the equation as \eqref{eq:series}.

When $a \ne 0$, there are two solutions to $ax^2 + bx + c = 0$ and they are

$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$

## Mermaid SVG
