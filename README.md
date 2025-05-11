# Madeline Bacon — Personal Website

This is the source code for my personal academic website built with [Hugo](https://gohugo.io/) using the [hugo-coder](https://github.com/luizdepra/hugo-coder) theme.

The site is deployed using GitHub Pages.

## Installation

This site uses Hugo Modules and the `hugo-coder` theme.

### 1. Install Hugo (Extended Version)

Check your Hugo version:

```
hugo version
```

Ensure it includes `extended`. If not, install it.

**macOS (Homebrew):**

```
brew install hugo
```

**Other systems:**  
Download the extended version from https://gohugo.io/getting-started/installing/

### 2. Initialize Hugo Modules

If cloning this repo for the first time:

```
hugo mod init github.com/yourusername/yourproject
hugo mod get github.com/luizdepra/hugo-coder
```

Then in `config.toml`, include:

```
theme = "github.com/luizdepra/hugo-coder"

[module]
  [[module.imports]]
    path = "github.com/luizdepra/hugo-coder"
```

### 3. Run the Development Server

To run the local server with drafts:

```
hugo server -D
```

Then visit:

```
http://localhost:1313
```

## Creating Posts

To create a new blog post:

```
hugo new posts/my-new-post.md
```

This creates a file at:

```
content/posts/my-new-post.md
```

Open the file and edit the front matter:

```
---
title: "My New Post"
date: 2025-05-11
draft: false
tags: ["research", "neuroscience"]
---
```

Then write your content below the front matter.

To preview it locally:

```
hugo server -D
```

Make sure `draft` is set to `false` to include it in production.

## Build and Deploy

To build the site for GitHub Pages using the `/docs` folder:

```
hugo --minify -d docs
```

Then push:

```
git add docs/
git commit -m "Build site"
git push
```

Ensure GitHub Pages is configured to use:

- Branch: `main`
- Folder: `/docs`

## Cleanup

To remove generated files:

```
rm -rf public/ resources/ docs/
```

## License

Content © Madeline Bacon.  
Source and theme released under the MIT License.
