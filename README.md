# WordPress Sublime Completions

WordPress Sublime Completionsis a collection of WordPress snippets and autocompletions for Sublime Text. It contains all of the core functions, filters, actions, and constants.

## Contributing

It would be great if you contributed, but in order to keep things a littlo more sane please follow the guidlines below

### Snippets

Before contributing snippets read [the sippet documentation](http://docs.sublimetext.info/en/latest/reference/snippets.html) to get familiar with the snippet syntax. There are some simple requirements for getting a snippet accepted.
* The snippet must conform to WordPress coding standarts see [http://codex.wordpress.org/WordPress_Coding_Standards](http://codex.wordpress.org/WordPress_Coding_Standards).
* There needs to always be a tab trigger, and it needs to not conflict with any triggers that are currently in the soure. If the snippet is a WordPress core function with some defaults defined you should use the function name as the tab trigger. For example if you are creating a snippet for `register_post_type()` with some base defaults the tab trigger should be `register_post_type`. This help user to not have to remember every snippet while still being able te take advantage of them.
* Always scope your snippets
  * PHP `source.php - source.variable.php`
  * CSS `source.css`
  * JavaScript `source.javascript`
  * HTML `text.html`
* Always include a description and make sure it's short but unique. If you're typing something and a snippet comes up you need to know what it does.

### File Naming

When naming files seperate words with dashes(-). If you're naming a snippet for a function that only contains the function with defaults set use the function name with underscores(_) replaced with dashes(-). So if you've created a snippet for `register_post_type()` the file name would be `register-post-type.sublime-snippet`, but if you have a snippet that isn't just a function with defaults then create a descriptive file name. Example: The snippet below would be named `pet-post-meta-trim.sublime-snippet`.

```xml
<snippet>
	<content><![CDATA[
trim( get_post_meta( get_the_ID(), '${1:key}', true ) )
]]></content>
	<tabTrigger>gpm</tabTrigger>
	<description>Retrieve Custom Field with whitespace trim</description>
</snippet>
```

Fork of: https://github.com/purplefish32/sublime-text-2-wordpress

Original TextMate bundle author : Gipetto - https://github.com/Gipetto/wordpress.tmbundle