# GitBook

## What is it

> GitBook is a command line tool (and Node.js library) for building beautiful books using GitHub/Git and Markdown (or AsciiDoc).
>
> GitBook can output your content as a website (customizable and extensibles) or as an ebook (PDF, ePub or Mobi).
>
> GitBook.com is the online platform to create and host books built using the GitBook format. It offers hosting, collaboration features and an easy-to-use editor.

## Quick Start

In ternimal, run

```bash
npm install gitbook-cli -g
gitbook init
gitbook serve
```

to launch a GitBook project on localhost.

Then (at least) edit following files to get started:

* `README.md` (the introduction page content)
* `SUMMARY.md` (indicating navigation structure)

See more about [Directory Structure](https://toolchain.gitbook.com/structure.html) and [Pages and Summary](https://toolchain.gitbook.com/pages.html) in its [doc](https://toolchain.gitbook.com/).

## Note

* [`.gitignore`](https://github.com/github/gitignore/blob/master/GitBook.gitignore) for GitBook repo
* [Plugins](https://plugins.gitbook.com/browse) for gitbook
