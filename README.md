# Dolenworks portfolio site

A static site forked from [Eleventy](https://github.com/11ty/eleventy) static site generator.

## Visit

* [Gitlab](https://wullaski.gitlab.com/dolenworks/)

## Local Dev

### Install dependencies

```
npm install
```

### Run Eleventy

```
npx eleventy
```

Or build and host locally for local development
```
npx eleventy --serve
```

Or build automatically when a template changes:
```
npx eleventy --watch
```

Or in debug mode:
```
DEBUG=* npx eleventy
```

### Implementation Notes

* `about/index.md` shows how to add a content page.
* `projects/` has the blog projects but really they can live in any directory. They need only the `project` tag to be added to this collection.
* Add the `nav` tag to add a template to the top level site navigation. For example, this is in use on `index.njk` and `about/index.md`.
* Content can be any template format (blog projects needn’t be markdown, for example). Configure your supported templates in `.eleventy.js` -> `templateFormats`.
	* Because `css` and `png` are listed in `templateFormats` but are not supported template types, any files with these extensions will be copied without modification to the output (while keeping the same directory structure).
* The blog project feed template is in `feed/feed.njk`. This is also a good example of using a global data files in that it uses `_data/metadata.json`.
* This example uses three layouts:
  * `_includes/layouts/base.njk`: the top level HTML structure
  * `_includes/layouts/home.njk`: the home page template (wrapped into `base.njk`)
  * `_includes/layouts/project.njk`: the blog project template (wrapped into `base.njk`)
* `_includes/projectlist.njk` is a Nunjucks include and is a reusable component used to display a list of all the projects. `index.njk` has an example of how to use it.
