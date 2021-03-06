# jotgit

Git-backed real time collaborative editor built with meteor.

Here's a quick demo: [http://youtu.be/z-_wSiGS18U](http://youtu.be/z-_wSiGS18U)

The current version of jotgit is a prototype that lets you collaboratively edit Markdown files in a local git repository. Then you can save the files (with an optional commit message), and they'll be committed to the repository.

## Getting Started

If you have not yet installed Meteor, do that:
```
curl https://install.meteor.com | /bin/sh
```
(This assumes that you're on unix.)

Clone this repository:
```
git clone https://github.com/jdleesmiller/jotgit.git
```

Start up meteor:
```
meteor
```
It should pull in all of the required dependencies. Make some tea.

Then visit [localhost:3000](http://localhost:3000) in your browser. Be sure to try with multiple windows!

By default, it loads up the test repository in `tests/demo`. To point it at another repository, you can either edit `server/jotgit.coffee` or use [meteor settings](http://docs.meteor.com/#meteor_settings) to specify an alternative `projectPath`.

## About

Jotgit ...

* is written in [CoffeeScript](http://coffeescript.org/), a language that feels a bit like Python and compiles to JavaScript.

* is built with [Meteor](https://www.meteor.com/), which is an up-and-comping web framework for real time web apps. It is remarkably developer-friendly, and it already has [very good documentation](http://docs.meteor.com/).

* is powered by [operational transformation](http://en.wikipedia.org/wiki/Operational_transformation), and in particular the excellent [ot.js](https://github.com/operational-transformation/ot.js) implementation.

* uses [CodeMirror](http://codemirror.net/) for the editing component.

The code is structured in the usual way for a meteor app: the files in `server` run on the server, the files in `client` run on the client, and the files in `lib` run on both. There's also a `jotgit-core` package in `packages/jotgit-core` that contains most of the core classes (stuff that is not very meteor-specific).

## Roadmap

* allow remote pushes to the repository

* auto-saves

* multiple projects

* user accounts

* some way of handling multiple commit authors (apparently not supported by git)

* option to commit to github instead of a local git repo

* file type handling (various text files, binary files)

* file uploads

## License

MIT --- see LICENSE file.

