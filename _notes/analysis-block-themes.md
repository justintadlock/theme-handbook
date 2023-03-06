# [Block Themes](https://developer.wordpress.org/themes/block-themes/)

Since this is a chapter landing page, it'd be helpful to have a "What's in this Chapter?" section. This page is very different than other chapter landing pages, and it'd help to have consistency across them so that people know what to expect.

Sub-pages in this chapter all use sentence case for their titles, which is inconsistent with the rest of the handbook, which uses title case.

## [Block Theme Setup](https://developer.wordpress.org/themes/block-themes/block-theme-setup/)

This page needs an intro section that introduces the reader to the content of the doc.

### [File Structure](https://developer.wordpress.org/themes/block-themes/block-theme-setup/#file-structure)

The information in this section is accurate, but it could use some more-detailed explanations of the example structure. It could also use links to other locations in the handbook for learning about things like patterns, templates, etc.

### [Theme Setup Function](https://developer.wordpress.org/themes/block-themes/block-theme-setup/#theme-setup-function)

Note: This section has duplicate content from the [Theme Functions doc](https://developer.wordpress.org/themes/basics/theme-functions/) earlier in the handbook.

### [Theme Support](https://developer.wordpress.org/themes/block-themes/block-theme-setup/#theme-support)

This section dives into `theme.json` concepts before the reader really understands what `theme.json` does, unless they jumped ahead. The table also really deals more with classic theme `functions.php`-style support than anything that block theme developers need to know.

Additionally, `appearance-tools` is not listed in the table.

I'm not a fan of the location of the table. I'd rather see it on a page dealing with classic themes or `theme.json`.

## [Templates and Template Parts](https://developer.wordpress.org/themes/block-themes/templates-and-template-parts/)

I began reviewing and analyzing each section of this page, but it quickly became apparent that this page needed a 100% rewrite from the ground up. I have left my notes in the sub-sections below that I had already written for historical sake. However, my recommended approach is to tackle this anew.

Primarily, this page could be broken up into two separate pages:  Templates and Parts. While there is a need to introduce parts alongside templates, the information could be better broken down and more deeply explored in separate docs.

Overall, I found this page often confusing, but the pathway to learning these concepts were not taught in a way that I feel would be conducive to the reader actually learning to build block themes.

### [Block Markup](https://developer.wordpress.org/themes/block-themes/templates-and-template-parts/#block-markup)

We really don't need to spend time talking about block themes in comparison to classic themes. Some readers will---hopefully after a rewrite of the handbook---not really know anything about classic themes (other than them being the old way of doing things). They'll be learning [block] theme development for the first time, so it's best not to confuse them.

### [Adding attributes to the block markup](https://developer.wordpress.org/themes/block-themes/templates-and-template-parts/#adding-attributes-to-the-block-markup)

I had to read this section three times to understand what it was explaining. There is barely any text that describes anything here.

### [How to find which block markup to use](https://developer.wordpress.org/themes/block-themes/templates-and-template-parts/#how-to-find-which-block-markup-to-use)

Needs a more-thorough explanation.

### [Templates](https://developer.wordpress.org/themes/block-themes/templates-and-template-parts/#block-798d87ea-3c2f-4065-a24e-215b644acc95)

The first paragraph here is entirely made up of improperly-formatted and incomplete sentences. Overall, the section just lacks information.

### [How to create templates with code](https://developer.wordpress.org/themes/block-themes/templates-and-template-parts/#how-to-create-templates-with-code)

I'm not really sure this even passes as an explanation.

## [Theme.json](https://developer.wordpress.org/themes/advanced-topics/theme-json/)

This page is massive. It is already ~2,800 words and will only grow over time. This will be tough to digest for any reader, but it also becomes tough to navigate the 25 different sections and sub-sections on the page. Essentially, it is too overwhelming.

Having had the experience of contributing to this page, the current page's size heavily impacted what I was able to add. I felt like I had to limit my explanations to not add too much weight to the page. This situation was a disservice to readers because it meant cutting back on useful information that might have helped them learn.

The page is also missing current information, and many of the existing sections barely have any written documentation.

`theme.json` is one of the primary tools for theme development, and it needs more breathing room than the single-page treatment it currently has. My early recommendation would be to have an introduction page with high-level overviews of each of the `theme.json` concepts (e.g., settings, styles, etc.). Then, at the very least, separate those concepts into individual pages. 

The "settings" page might even be best served via individual pages for each type of setting (e.g., typography, spacing, etc.). It is easily the heaviest bit of documentation that could use more-detailed explanations than the handbook currently provides.

There is also a need for documentation on `theme.json` filters, but this is likely something more catered to the "advanced" section in the current handbook's structure or a page of its own.

## [Converting a classic theme to a block theme](https://developer.wordpress.org/themes/block-themes/converting-a-classic-theme-to-a-block-theme/)

The intro mentions child themes, but I don't recall the child theme concept being explored at this point in the handbook, which are [explored](https://developer.wordpress.org/themes/advanced-topics/child-themes/) later in the Advanced section. At the very least, this should be linked.

As a whole, this page could really use some high-quality screenshots of what these features look like. It'd go a long way toward describing exactly what a theme author is enabling for their theme. Remember that many readers will be building block themes for the first time.

### [Gradually adopting Site Editing features](https://developer.wordpress.org/themes/block-themes/converting-a-classic-theme-to-a-block-theme/#gradually-adopting-the-full-site-editing)

This section describes a "universal theme" as a block theme that enables customizer options. I'm not entirely sure that the statement is accurate or if there's really a solid definition of a universal theme out there. My understanding was that a universal theme is one that fully supported both block editor and classic usage, depending on the user's choice, but I could be wrong. The terminology seems a bit muddied. Even if the existing definition is considered a universal theme, why the additional terminology for supporting a single feature? Instead, this is simply a block theme with some customizer options.

### [Adding theme.json in classic themes](https://developer.wordpress.org/themes/block-themes/converting-a-classic-theme-to-a-block-theme/#adding-theme-json-in-classic-themes)

This section has inaccurate content. `theme.json` does not erase all need of calling `add_theme_support()` (e.g., `post-formats`, `wp-block-styles`, etc.).

### [Adding block patterns in classic themes](https://developer.wordpress.org/themes/block-themes/converting-a-classic-theme-to-a-block-theme/#adding-block-patterns-in-classic-themes)

Mostly, this explanation could be a little better. It seems to be specifically catering to whole-page layouts. It doesn't make for an ideal pathway if the reader is not interested in that aspect. Patterns are so much more than that, and the handbook could "sell" the concept much better.

### [Enabling the template editor](https://developer.wordpress.org/themes/block-themes/converting-a-classic-theme-to-a-block-theme/#enabling-template-editor)

_What is the template editor?_ There's no explanation about what it is.

### [Disabling the template editor](https://developer.wordpress.org/themes/block-themes/converting-a-classic-theme-to-a-block-theme/#disabling-template-editor)

This should be coupled with the "enabling" section. Provide a full explanation of this feature instead of breaking it down into the tiniest bits.

### [Converting customizer settings to block patterns](https://developer.wordpress.org/themes/block-themes/converting-customizer-settings-to-block-patterns/)

I had no idea what this sub-page was going to be about when diving in. The title made no sense to me. _Why would settings convert to patterns?_ The two are seemingly so unrelated that I couldn't fathom why there'd be a page for it.

The page isn't really about converting customizer settings to block patterns at all.

It is about one highly-specific scenario where theme authors used the customizer to pigeon-hole content creation into theme settings. Then, taking the specifics of this scenario (a call-to-action homepage section) and converting it to a pattern.

This content would be better served as a tutorial on the Developer Blog. It's not bad content; it's just in the wrong place.

## [Creating new themes using the Site Editor](https://developer.wordpress.org/themes/block-themes/creating-new-themes-using-the-site-editor/)

### [Editing an existing theme](https://developer.wordpress.org/themes/block-themes/creating-new-themes-using-the-site-editor/#editing-an-existing-theme)

This section talks about using a GPL theme to make sure the theme is licensed correctly. However, it stops short of noting copyright. While this page shouldn't delve too much into licensing and copyright, it is worth noting that maintaining the original theme's copyright is necessary. Much of this is likely exported since WP 6.0, however in unchanged files like `style.css` and `functions.php`.

### [Creating a theme from exported files](https://developer.wordpress.org/themes/block-themes/creating-new-themes-using-the-site-editor/#creating-a-theme-from-the-exported-files)

The WordPress 5.9 section should be removed. New themes shouldn't be built using an outdated version of WordPress. If anyone feels strongly about keeping it, it should not be shown first in this section.

The 6.0 section is missing information about updating the screenshot.

## [Internationalization](https://developer.wordpress.org/themes/block-themes/internationalization/)

### [Using text in block patterns](https://developer.wordpress.org/themes/block-themes/internationalization/#using-text-in-block-patterns)

I'd recommend updating the example code to using a pattern via the `/patterns` folder. It should be the standard recommended method of registering patterns. Plus, it's less-prone to escaping issues.
