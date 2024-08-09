# Hugo documentation

A CYBERTEC themed "fork" of the [geekdoc](https://github.com/thegeeklab/hugo-geekdoc) theme for hugo.

## Requirements

- `go`
- `hugo`

## Usage

Initialize a new hugo site:

```shell
hugo new site <site-name>
cd <site-name>
```

Initialize the site as a go module:

```shell
hugo mod init github.com/cybertec-postgresql/<repository-name>
```

Add this repository as a dependency into your `hugo.toml`:

```toml
# hugo.toml
[module]
[[module.imports]]
path = 'github.com/cybertec-postgresql/hugo_documentation'
```

Fetch the module

```shell
hugo mod get -u
```

Build your page
```shell
hugo --minify
# You may optionally overwrite the `baseURL`
hugo --minify -b "/docs/"
```

## Update

To retrieve the latest version of this theme, simply run

```shell
hugo mod get -u
hugo mod tidy
```

## "Fork"

This repository uses the built release, taken from https://github.com/thegeeklab/hugo-geekdoc/releases/latest/download/hugo-geekdoc.tar.gz.

The following customizations have been done to achieve a CYBERTEC look and feel:

- Use the CYBERTEC logo in `./static/brand.svg`
- Add the `./config/_default/hugo.toml` config

In case that `geekdoc` is updated, we will have to fetch the latest release, merge those files into this repository, and handle possible merge conflicts.
