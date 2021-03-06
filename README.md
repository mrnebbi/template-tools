# Template Tools


[![version 2.0.0](https://img.shields.io/badge/version-2.0.0-brightgreen.svg)](https://github.com/mrnebbi/craft-template-tools)


A Craft plugin to provide twig filters to help with template building.

***
Please note: As of version 2.0, I've removed the Query Strings functionality from template tools. Please use my [Query Strings plugin](https://github.com/mrnebbi/craft-query-strings).
***

## firstTag

Easily add a class, ID, or other attribute to the first element of a specific type. Useful for adding a class to the first paragraph.

### Add a class

```
{{ content|firstTag('classname') }}
```

By default this adds a class name to the first P tag.
Add a `.` or `#` to set an ID or Class.

### Add an ID

```
{{ content|firstTag('#idname') }}
```

### Add to a non paragraph
Sets a class name or ID to the first tag of a type specified by you. e.g.

```
{{ content|firstTag('classname','h2') }}
```
Add a `.` or `#` to set an ID or Class.

### Add custom attribute and value to a non paragraph
Sets a value for a specified attribute to the first tag of a type specified by you.
```
{{ content|firstTag('slider1','img','data-slider') }}
```


```
{{ content|firstTag('lead','h2','data-heading') }}
```



## getFirstParagraph

Retrieve the first paragraph from content.

### Get paragraph only

```
{{ content|getFirstParagraph }}
```

### Get paragraph and remove P tags

Add a flag of true to remove the P tags from the content.

```
{{ content|getFirstParagraph(true) }}
```


## wrapLinesInTag

This wraps any lines in multiline text in a tag of your choosing.

```
{{ content|wrapLinesInTag('span') }}
```

## preserveQueryStrings

Removed Query Strings functionality. Please use my [Query Strings plugin](https://github.com/mrnebbi/craft-query-strings).

~~The Preserve Query String filter allows you to add `|preserveQueryStrings` to any URL output in twig, and it will keep the query strings as they should appear in the URL.~~


## getQueryStrings

Removed Query Strings functionality. Please use my [Query Strings plugin](https://github.com/mrnebbi/craft-query-strings).

~~Pull an array of query strings from Craft. This gets around the problem of duplicated query string keys being lost, turning them into an array you can loop through.~~

~~An array will be returned with objects. Use `.key` and `.value`.~~
