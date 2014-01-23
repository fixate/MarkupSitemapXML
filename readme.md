# MarkupSitemapXML - Index Children Of 404 Version

## Purpose

Ensure that the sitemap indexes all pages that are accessible to the guest user, including children of 404'd templates.

## Reasoning

By default, [MarkupSitemapXML](https://github.com/Notanotherdotcom/MarkupSitemapXML) does not add pages to the sitemap that are children of templates that have been set to 404.

Sometimes we have may a top-level navigation item that is purely categorical, and does not have its own page, but has children that you would like indexed.

The children of that page should be indexed, but we don't want the parent that is set to 404 to be indexed.

i.e. if we have the following structure:

```
  ├── home
	   ├── page 1
	   ├── page 2						// category without page - i.e. uses 404
			   ├── child 1
			   └── child 2
	   ├── page 3
	   └── page 4
```
the generated sitemap will have the following links:

```
/home
/page-1
/page-2/child-1
/page-2/child-2
/page-3
/page-4
```

## Usage

As with other modules:

- place this module in your `modules/` folder
- check for new modules in your admin
- install the module
- visit /sitemap.xml


Visit the [ProcessWire forum topic](http://processwire.com/talk/topic/799-module-xml-sitemap/) for a discussion on this module.
