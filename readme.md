# Jekyll Basis

## (A work in progress)

A minimal starter for new [Jekyll](http://jekyllrb.com/) projects. This workflow uses Jekyll to build a static site with the help of Node.js command line utilities (managed with [npm](https://www.npmjs.com)). Additionally, Amazon Web Services [Simple Storage Service (S3)](https://aws.amazon.com/s3/) can be used to deploy and host a site affordably. This project can be forked or copied as the basis for a larger Jekyll project (which is how I intend to use it myself).

This repo is [unlicensed](http://unlicense.org/) and you can do what you want with it. Originally created by [Oliver Pattison](https://olivermak.es/).

## Features

- npm’s `run` scripts as a supporting build system for building a fast site.
- Support for development and production deployment with AWS S3.
- SCSS ready to design with (split into modular **blocks**, **containers**, and **themes**).
- Atom syndication feed with escaped HTML5 elements (for valid Atom XML feeds).

## Built-in commands

`npm start`: serve a Jekyll site along with any other build commands specified in npm’s `package.json` configuration file.

`npm run dev`: deploy a Jekyll site to a development S3 site.

`npm run prod`: deploy a Jekyll site to a production S3 site.

Read more about [npm as a build tool](http://blog.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/) and [how npm’s package.json file works](https://docs.npmjs.com/files/package.json).

## Configuration checklist

- [ ] Install [node and npm](https://nodejs.org/en/)
- [ ] Install Ruby and [bundler](http://bundler.io).
- [ ] Run `npm install` in the command line to update node dependencies.
- [ ] Run `bundle install` to update Ruby dependencies.
- [ ] Run `npm start` and make sure that Jekyll builds and serves properly.
- [ ] Change defaults in `config.yml`.
- [ ] Set up [s3_website](https://github.com/laurilehmijoki/s3_website) with development and production buckets (or remove `s3_website.yml` configuration file if not using S3).
- [ ] Before publishing a project publicly, [change the license](http://choosealicense.com) to one that is appropriate for your project. This repo’s license does not require credit and can be completely re-worked.

To find defaults that need attention, search `TODO` in the project.

## Conventions followed

S3 buckets should be named in the style of `dev.example.com` (for development) and `example.com` (for production).

SCSS is used instead of [Sass indented syntax](http://thesassway.com/editorial/sass-vs-scss-which-syntax-is-better).

Custom, minimal normalizing SCSS file is used. It can be completely replaced with something like [Normalize.css](https://necolas.github.io/normalize.css/).

## Notes

Styles are intentionally rudimentary. This is not a theme (although it could be used to make a theme).

Configuration for this project is opinionated. This project requires npm to run properly, unlike many Jekyll projects. It could be made to run on GitHub Pages, but certain dependencies would need to be adjusted.
