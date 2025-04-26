---
layout: post
tags:
  - github
  - jekyll
  - obsidian
date: "2025-02-20 12:00:00 +0000"
created: "2025-02-20 17:49:44"
updated: "2025-04-26 16:42:12"
title: "Obsidian, Jekyll, and Github"
categories:
  - Knowledge Management
mermaid: true
---

<!--
This file was automatically converted by Jekyll Publisher for Obsidian.
https://github.com/jsade/obsidian-jekyll-plugin

Version: 1.0.1
Conversion date: 2025-04-26 14:00:09 +0000
-->


![](../assets/img/obsidian/obsidian-logo-text-white-purple.svg){:width="150px"}

These days I'm using [Obsidian](https://obsidian.md) for all my note taking needs. Obsidian is a super-flexible, [markdown](https://www.markdownguide.org/)-based note-taking app that lets you easily link ideas, organize knowledge, and customize your workflow just the way you like.

There's very little I'm _not_ using it for right now, as it covers my requirements for writing meeting minutes, diary entries, project plans, requirement specifications, and blog posts. But I've also been using it lately for business presentations instead of Keynote, for personal task management (I've stopped using Todoist), and its canvas functionality for drawing charts and diagrams (instead of Miro). Not to forget inline [Mermaid](https://mermaidjs.org) diagrams such as the one below. And this list of use cases seems to be growing periodically.

## From Obsidian to Web

Sometimes my writing includes content or topics that I think might be interesting to others. So, why not make it easy to publish these notes straight from Obsidian to some public web server?

After some consideration I've settled into the following workflow:

1. **Content Creation in [Obsidian](https://obsidian.md)**: All writing happens in Obsidian, taking full advantage of its markdown editor, internal linking, and preview features. This keeps my content in a format that's both human-readable and future-proof.
2. **Automated Processing**: My custom plugin (obsidian-jekyll-plugin) handles the technical heavy lifting. It converts Obsidian-specific markdown features to standard web formats and manages all assets (images, PDFs, etc.) to ensure they're web-ready.
3. **Static Site Generation**: [Jekyll](https://jekyllrb.com) transforms the processed markdown into a modern, responsive website. It handles all the templating, creates category pages, generates RSS feeds, and ensures proper SEO structure.
4. **Seamless Deployment**: The built site is automatically committed to [GitHub](https://github.com), which triggers a [GitHub Action](https://github.com/features/actions) to deploy to [GitHub Pages](https://pages.github.com/). This provides version control, rollback capability, and reliable hosting without any manual intervention.

<div class="mermaid">
%%{init: {"flowchart": {"defaultRenderer": "elk"}} }%%
graph LR;
A("**Obsidian**<br>Markdown editing") --> B("**obsidian-jekyll-plugin**<br>Process files & assets")
    B --> C[/"**Jekyll**<br>Build static site"/]
    C --> D("**GitHub Repo**<br>Version control")
    D --> E{"**GitHub Pages**<br>Web hosting"}

</div>

## Why This Setup?

This workflow combines the best of both worlds: the powerful editing and organization features of Obsidian with the reliability and simplicity of static site hosting. There are several benefits to this approach:

- **Write Once, Use Everywhere**: My notes remain in plain markdown format, accessible from any device or editor. The same content can be used for personal reference or public sharing without duplication.
- **Zero Hosting Costs**: GitHub Pages provides free hosting for static websites, with excellent uptime and performance. There's no need for managing servers or dealing with complex hosting setups.
- **Version Control Built-in**: Since everything goes through Git, I have a complete history of all changes to my published content. This makes it easy to track changes, rollback if needed, and collaborate with others.

## Obsidian to Jekyll Plugin

The custom plugin (**obsidian-jekyll-plugin**) handles the heavy lifting of preparing content for Jekyll, including:

- **Markdown Conversion**:
	- Converting Obsidian's wiki-style links (`[link](link)`) to standard markdown links
	- Converting highlights (`<mark>text</mark>`) to HTML marks
	- Handling superscript and subscript notation
	- Converting Obsidian-specific callouts to standard HTML
- **Frontmatter Management**:
	- Maintaining existing frontmatter fields
	- Ensuring Jekyll-required fields (layout, title, date)
	- Proper YAML formatting with quotes when needed
	- Preserving tags and categories
	- Auto-detecting and enabling Mermaid diagrams
- **File Organization**:
	- Creating Jekyll-compatible filenames (YYYY-MM-DD-title.md)
	- Converting spaces and special characters to web-friendly formats
	- Managing file creation dates
	- Organizing assets in the Jekyll structure

Using the plugin is straightforward through the Obsidian interface - either via the command palette, ribbon icon, or right-click menu. This means I can write naturally in Obsidian and publish with just a few clicks.

When I have the time, I'll give the plugin a bit of polish and publish it for all.
