# [Theme Basics](https://developer.wordpress.org/themes/basics/)

Same feedback as [Getting Started](https://github.com/justintadlock/theme-handbook/blob/master/_notes/analysis-getting-started.md#getting-started) chapter intro page.

## Overall Structure of the Theme Basics Chapter

The current navigation/structure for the chapter is not ideal:

- Theme Functions
- Template Files
- Main Stylesheet (style.css)
- Post Types
- Organizing Theme Files
- Template Hierarchy
- Including CSS & JavaScript
- Categories, Tags, & Custom Taxonomies
- Tools & Resources

The handbook is walking readers through advanced stages (functions) before teaching the basics of getting a theme up and running.

This entire chapter in the handbook primarily deals with theme files. Therefore, it is reasonable to assume that the "Organizing Theme Files" page be listed first (maybe renamed).

The most important theme file, which is required for a theme to be a theme, is the `style.css` file, so it should be second. Theme Functions and Template Files could possibly be switched (functions are a more advanced feature). But, then there's the Template Hierarchy farther down. Understanding the Template Hierarchy goes hand-in-hand with Template Files. Those should likely be combined.

I'm also not sure if Post Types and Categories, Tags, & Custom Taxonomies should have their own pages. Mostly, a theme is concerned with these at a template level, so the relevant info should be in the template documentation. I'm not sure introducing these more advanced concepts is relevant to this "basics" section of the handbook either.

At first glance (and assuming no other major changes to the navigation/structure of the content), this is how I'd list out the current navigation:

- Organizing Theme Files
- Main Stylesheet (style.css)
- Template Files + - Template Hierarchy
- Theme Functions
- Including CSS & JavaScript (_maybe separate pages_)
- ~~Post Types~~
- ~~Categories, Tags, & Custom Taxonomies~~
- Tools & Resources

There's a possibility of creating a "Building Your First Theme" tutorial in here to cover everything learned in the chapter.

## [Organizing Theme Files](https://developer.wordpress.org/themes/basics/organizing-theme-files/)

Ideally, this would be the first page in the chapter. A better title for it would be "Anatomy of a Theme." The goal for this page should be introducing the reader to the files needed for a WordPress theme.

The current proposed structure mixes both classic and block theme concepts. These should be separated into their own sections (the reader has already been introduced to these concepts at this stage in the handbook). While there is some cross-over, it'd still be preferable to not mix the two.

This page could also have more-detailed explanations of the various types of files and what they do. It currently assumes a lot of existing knowledge on the reader's part. The page should also link to other pages in the handbook that covers the files (e.g., `functions.php`, `style.css`, templates).

## [Main Stylesheet (style.css)](https://developer.wordpress.org/themes/basics/main-stylesheet-style-css/)

This intro section says that this file is required but doesn't actually say why. It should provide some info that it is essentially a configuration file as well as a stylesheet at this point.

Mostly, the information provided in this page is generally OK. It covers the high-level things the reader must know. However, it could use more in-depth coverage in its [Explanations](https://developer.wordpress.org/themes/basics/main-stylesheet-style-css/#explanations) section. It introduces many concepts to the user without providing details or links to find more information (for example, _What's a textdomain?_). 

The Explanations list is also very long, almost becoming a wall of text that's tough to parse. Part of this is due to poor design for this type of content. But, there are ways to better format this alongside explanations of what each item means, such as sub-sections instead of a list.

## [Template Files](https://developer.wordpress.org/themes/basics/template-files/)

This page needs a better intro into what templates are. The current intro is just like, "Hey, here's the topic!" which is essentially unnecessary (the reader already knows that's what the topic is, so jump on in).

This entire page needs to be rewritten from the ground up. Honestly, there is not much about it that really walks the reader through the concepts in an easy-to-digest manner. I'm listing some specific problems below, but the entire structure and formatting just feels cobbled together.

### [Template Terminology](https://developer.wordpress.org/themes/basics/template-files/#template-terminology)

The first definition of template in this section isn't entirely accurate:

> Templates files exist within a theme and express how your site is displayed.

CSS determines the display. Templates output the content structure (HTML). This just needs a better explanation, particularly defining that relationship.

I'd probably scrap this entire section and just introduce the basic concept of templates in the intro.

### [Template Files](https://developer.wordpress.org/themes/basics/template-files/#template-files) and [Template Partials](https://developer.wordpress.org/themes/basics/template-files/#template-partials)

I wonder if it'd be helpful to split these into two separate pages: Templates and Template Parts. Allow this "Template Files" page in the chapter to lay the groundwork of these basics, then provide details for each in separate pages.

### [Common WordPress Template Files](https://developer.wordpress.org/themes/basics/template-files/#common-wordpress-template-files)

`style.css` and `rtl.css` are not template files and shouldn't be included.

The `page.php/html` explanation says that this is a "built-in template," which is not correct.

There are no links back to HelpHub pages that explains some of the concepts. For example, when referring to post types, the [Post Types doc](https://wordpress.org/documentation/article/what-is-post-type/) would be helpful here.

This entire section is a bit messy to read through. An overhaul that couples with the Template Hierarchy documentation would probably be ideal.

## [Template Hierarchy](https://developer.wordpress.org/themes/basics/template-hierarchy/)

This page does a lot of the good things that the [Common WordPress Template Files](https://developer.wordpress.org/themes/basics/template-files/#common-wordpress-template-files) section of the Template Files page doesn't do: it gives reasonably thorough explanations of the top-level template files in themes.

The major issue with this page is that it caters to classic rather than block themes. 

Documenting this for block themes could also open more opportunities for adding in screenshots of what these templates look in the editor. The theme author user base is growing to include no-code designers, so teaching the hierarchy to them is important without diving into physical theme files.

This is a long page, and the template hierarchy is exactly the same for both classic and block themes (just different file extensions). So, I'm not keen on creating separate documents for both. However, I could see adding another page that explores this as a visual build via the site editor. There's some exploration of this in a separate [Creating New Themes Using the Site Editor](https://developer.wordpress.org/themes/block-themes/creating-new-themes-using-the-site-editor/) page, but it's about the overall theme and doesn't exclusively focus on templates.

## [Theme Functions](https://developer.wordpress.org/themes/basics/theme-functions/)

"Both" is used to refer to three things instead of two in the intro.

This page doesn't include any information on prefixing/namespacing. It'd be a perfect opportunity to do so and to consistently use this as an example throughout the rest of the handbook.

### [What is functions.php?](https://developer.wordpress.org/themes/basics/theme-functions/#what-is-functions-php)

This statement is factually incorrect:

> Note:The same result can be produced using either a plugin or functions.php.

While this is often true, plugins can execute actions earlier in the load process and do things that themes cannot at that stage.

I don't really understand why this sections spends so much time talking about plugins can do vs. what themes can do. That might be good for a separate "FAQs" page, but it seems so unnecessary here. Let's just dive into what `functions.php` is and what it should be used for.

Minor gripe with the text: "plain-text file named `functions.php`". A plain text file would be `functions.txt`. `functions.php` is a PHP file.

Another gripe: "Adding a function to the child functions file is a risk-free way to modify a parent theme." No, this is not risk-free at all. The next sentence explains that you don't have to worry about losing customizations with updates, but this needs to be reworded to be clearer.

### Intro to hooks

There should be an introduction to hooks section after the explanation of `functions.php`. Any use of this file pretty much means you need to deal with hooks, and it's best to just "rip the Band-Aid" off now by providing a basic explanation with resources to learn more. Since this is the "Basics" section of the handbook, it's probably best not to overwhelm the reader with a deep dive yet.

### [Theme Setup](https://developer.wordpress.org/themes/basics/theme-functions/#load-text-domain)

It's not mentioned until later in this section that block themes do not need most or any of this. I'd like to bring this up earlier. It might be worth restructuring this entire section.

#### [Load Text Domain](https://developer.wordpress.org/themes/basics/theme-functions/#load-text-domain)

Note that WordPress.org-hosted themes do not need to do this.

## [Including CSS & JavaScript](https://developer.wordpress.org/themes/basics/including-css-javascript/)

The title of the page is another use of an ampersand when "and" would be ideal.

There are many uses of the word "enqueue" in this page without any explanation of what it means. It's use is fairly uncommon, and it may throw some readers off. Generally, a new theme author might ask how to "load" a CSS or JS file. So, it'd be helpful to describe that the `wp_enqueue_*()` functions are queueing a style/script to load.

This page does not include any mention of the `wp_register_*()` functions either. There are likely few use cases where registering without enqueueing are necessary for themes, it probably wouldn't hurt to have a short explanation.

`style.css` is frequently mentioned as required on this page, but it's not clear that is merely required to exist in the theme folder. A theme is not required to enqueue it unless the theme author intends to add CSS to it.

### [Stylesheets](https://developer.wordpress.org/themes/basics/including-css-javascript/#stylesheets)

The use of `get_template_directory_uri()` is not technically incorrect, but it shouldn't be considered standard. Instead `get_theme_file_uri()` would often be best. 

There are some caveats to that, so it might be worthwhile to explore file-loading functions at some point. That's probably a more advanced topic, so I'd stick with something that works automatically with parent and child themes here: `get_theme_file_uri()`.

While the handbook hasn't fully explained hooks to the reader at this point, themes should be enqueuing stylesheets on the appropriate hook, typically `wp_enqueue_scripts`. Essentially, the docs are currently just telling the reader to drop code into `functions.php` with no mention of best practices.

There is no coverage for including editor stylesheets on this page.

### [Including CSS for Block Styles](https://developer.wordpress.org/themes/basics/including-css-javascript/#including-css-for-block-styles)

It'd be best to refer to this as "Block Stylesheets" to not confuse it with the common term "Block Styles" (short for Block Style Variations).

### [Scripts](https://developer.wordpress.org/themes/basics/including-css-javascript/#scripts)

The explanation in this section is pretty light. It also has all the same issues as mentioned earlier in the Stylesheets section.

### [Comment Reply Script](https://developer.wordpress.org/themes/basics/including-css-javascript/#the-comment-reply-script)

Again, run on the `wp_enqueue_scripts` hook.

### [Combining Enqueue Functions](https://developer.wordpress.org/themes/basics/including-css-javascript/#combining-enqueue-functions)

Finally, the page gets to mentioning the appropriate hook. But, many readers may not even get to this point or think about reading it if they only need to include a single style/script. The concept of using `wp_enqueue_scripts` should be introduced earlier.

## [Post Types](https://developer.wordpress.org/themes/basics/post-types/)

This page primarily just deals with template files. There's really not much of a reason that it should be introduced separately. Essentially, it's duplicate content. 

There are some custom functions and features that might be worth exploring (not currently on this page), but this certainly wouldn't belong in the "Basics" chapter.

## [Categories, Tags, & Custom Taxonomies](https://developer.wordpress.org/themes/basics/categories-tags-custom-taxonomies/)

_What is it with the use of an ampersand in handbook page titles?_

This page links back to the template hierarchy page for its template explanation, so it's a little different than the Post Types page. Also, most of this information isn't strictly relevant to themes. I'm just not seeing this as a particularly useful page for this section of the handbook.

_I wonder if it would be useful to have a single "terminology" or "concepts" page that explains post types, taxonomies, etc. for the "Basics" section..._

## [Tools & Resources](https://developer.wordpress.org/themes/basics/tools-resources/)

In general, this page looks pretty useful. It'd be nice to have some screenshots of the tools to make the page more inviting.

This could probably use a full resource review to make sure it's current and that we're including other DotOrg resources, such as the Dev Blog posts on themes.
