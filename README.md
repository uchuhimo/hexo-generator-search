# hexo-generator-searchdb

[![npm](https://img.shields.io/badge/npmjs-1.0.4-brightgreen.svg)](https://www.npmjs.com/package/hexo-generator-searchdb)

Generate search data for Hexo 3.0. This plugin is used for generating a search index file, which contains all the neccessary data of your articles that you can use to write a local search engine for your blog. Supports both XML and JSON format output.

- [Demo](http://blog.zzbd.org) - work with Next theme.

## Install

``` bash
$ npm install hexo-generator-searchdb --save
```

## Options

You can configure this plugin in your root `_config.yml`. All the arguments are optional.

``` yaml
search:
  path: search.xml
  field: post
  format: html
  limit: 10000
```

- **path** - file path. By default is `search.xml` . If the file extension is `.json`, the output format will be JSON. Otherwise XML format file will be exported.
- **field** - the search scope you want to search, you can chose:
  * **post** (Default) - will only covers all the posts of your blog.
  * **page** - will only covers all the pages of your blog.
  * **all** - will covers all the posts and pages of your blog.
- **format** - the form of the page contents, works with xml mode, options are:
  * **html** (Default) - original html string being minified.
  * **raw** - markdown text of each posts or pages.
  * **excerpt** - only collect excerpt.
  * **more** - act as you think.
- **limit** - define the maximum number of posts being indexed, always prefer the newest.
