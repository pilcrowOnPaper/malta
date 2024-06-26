---
title: "Getting started"
---

# Getting started

## Installation

Binaries for MacOS, Linux, and Windows are available from [GitHub releases](https://github.com/pilcrowOnPaper/malta/releases/latest).

For MacOS/Linux, you can install it with the following commands:

```
curl -o malta.tgz -L https://github.com/pilcrowonpaper/malta/releases/latest/download/<platform>-<arch>.tgz

tar -xvzf malta.tgz

install <platform>-<arch>/malta /usr/local/bin
```

## Create a config file

Create `malta.config.json` in the project root. 

```json
{
    // required (used for open-graph)
    "name": "Malta", // project/library name
    "description": "Malta is a CLI tool for creating documentation sites",
    "domain": "https://example.com",

    // optional
    "twitter": "@pilcrowonpaper", // twitter account associated with the project
    "sidebar": [], // see 'Sidebar' page
    "asset_hashing": true // default: false - hashes the filenames for easy caching
}
```

You can also add the following files next to the config file:

- `favicon.ico`
- `logo.[EXTENSION]`: Adds logo to the sidebar
- `og-logo.[EXTENSION]`: Square image for OG

## Create `pages` directory

Create a `pages` directory next to the config file, and create `index.md`. You must have a `title` attribute.

```md
---
title: "My documentation site"
---

# My documentation site

Welcome to my documentation site.
```

## Generate HTML

Run the `build` command to generate HTML files in the `dist` directory, and the `preview` to preview your site at port 3000 (default)

```
malta build
malta preview
```
