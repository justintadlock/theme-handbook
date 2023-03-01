# [Getting Started](https://developer.wordpress.org/themes/getting-started/)

I'm not a fan of these extremely short pages. Often, they are just an annoyance when you're trying to walk through the learning process. Mostly, the text here could just be fleshed out a bit more with details about what's in this chapter.

I could also see this being written out as more of a step-by-step list.

**Note for design:** it'd be great to have a block style or pattern for each of these "chapter intro" pages to add a "What's in This Chapter?" section with a list of links. Essentially, a ToC for the chapter. Then, we could potentially dive more into descriptions of the chapter's content further down the page. _Just thinking out loud here..._

## [Who Should Read This Handbook?](https://developer.wordpress.org/themes/getting-started/who-should-read-this-handbook/)

The intro doesn't really directly answer the question the title asks. The focus should be more on the person reading than what the handbook provides. Otherwise, it should be titled "What's in This Handbook?" The original title sounds more interesting, though, and we can use the intro to put the focus back on the reader.

The [Your Skill Level](https://developer.wordpress.org/themes/getting-started/who-should-read-this-handbook/#your-skill-level) section of this page is currently out of date. It currently says that newcomers require some understanding of PHP, HTML, and CSS. This is also a bit vague on what level of understanding is required.

There is also now more of a push bring no-code designers more and more into the theme development world with block themes. It is entirely possible to build themes without any of this requisite knowledge. I'd argue some baseline HTML, CSS, and PHP are generally helpful, even with block themes, but it's not necessarily a requirement. Plus, now that the [Create Block Theme](https://wordpress.org/plugins/create-block-theme/) plugin is an official WordPress project, it lowers the barrier to entry.

This section might be a good place to start introducing some pathways to learning.

The [What This Handbook Will Cover](https://developer.wordpress.org/themes/getting-started/who-should-read-this-handbook/#what-this-handbook-will-cover) section can likely be rewritten after the completion of this project. I feel like saying that it only "provides the **basic** information required to develop block themes or classic WordPress themes" is selling ourselves short and a bit of a disservice to the theming community. I'd like to be able to say that you can learn everything (or at least most things) from the handbook. 

This page would also be an opportunity to provide learning pathways via links as visitors read through it. There's a missed opportunity to guide the reader here.

I also wonder if this information would be better on the landing/index page.

## [What is a Theme?](https://developer.wordpress.org/themes/getting-started/what-is-a-theme/)

This page is generally well written and provides a good definition of themes. There are some areas that could be fleshed out some more and generally make things a bit less dry and more exciting. In general, I'd recommend a full copy review.

I'd also like to see some more imagery to capture the visitor's imagination. This is an opportunity to showcase great designs and sell WordPress to a potential new theme author---make them believe that they can do this too. At the same time, imagery can really emphasize the guiding principle of this page that themes are the visual representation of a site.

This page should also have a "Differences Between Block and Classic Themes" or "What Are...?" section. Since these concepts are mentioned here, an intro section would help alleviate any confusion.

## [WordPress Licensing & the GPL](https://developer.wordpress.org/themes/getting-started/wordpress-licensing-the-gpl/)

The page title should use "and" instead of an ampersand. But, overall, this page looks pretty solid.

## [Setting up a Development Environment](https://developer.wordpress.org/themes/getting-started/setting-up-a-development-environment/)

Minor gripe: "up" in the title should be capitalized since it is part of the phrasal verb "Setting Up."

This page also jumps directly from local dev environment to enabling `WP_DEBUG`. There's no mention of actually installing WordPress first. There is existing documentation elsewhere on DotOrg for doing this, but there should be a section on installation that links to the appropriate resources.

The [Your WordPress Local Development Environment](https://developer.wordpress.org/themes/getting-started/setting-up-a-development-environment/#your-wordpress-local-development-environment) section should link out to each of the options that it mentions (don't make the reader hunt them down). Make it a list of links and separate by operating system. This is easily the hardest part of the theme dev process, so let's do everything we can to lower the barrier to entry.

I would probably create entire page section for the "Text Editor" part here. Again, provide a list of links and separate by operating system. The list should also be reviewed to make sure that it's current (e.g., Atom was sunset in 2022).

The [Supporting Older WordPress Versions](https://developer.wordpress.org/themes/getting-started/setting-up-a-development-environment/#supporting-older-versions-of-wordpress) sections says that it is "standard practice" to support two older versions. With version checking and easy upgrades built into core WordPress now, I don't see a reason for this to necessarily be considered standard. 

At best, this section is a side note. At worst, it is off-topic and takes away from the primary goal of talking about the development environment. I'd recommend this to be covered in a more general "FAQs" or "best practices" page in the handbook.

### [WP_DEBUG](https://developer.wordpress.org/themes/getting-started/setting-up-a-development-environment/#wp-debug)

A first-time reader doesn't know what `WP_DEBUG` means. This should be retitled to something like "Setting Up Debugging" (or similar).

The section also starts with this sentence: "Configuring debugging is an essential part of WordPress theme development." But, it doesn't explain why it is essential. More info is needed to explain this importance to new theme authors. Otherwise, we're throwing a lot of technical stuff at them with no explanation. The "why" is just as important as the "how."

There is also no explanation of `WP_DISABLE_FATAL_ERROR_HANDLER` here, despite the reader being told to enable it.

The [Test Data](https://developer.wordpress.org/themes/getting-started/setting-up-a-development-environment/#test-data) section could use a general intro about what test data is and how to use it. The Theme Unit Test page also links to the old Codex. It should have its own page in the handbook.

The [Plugins](https://developer.wordpress.org/themes/getting-started/setting-up-a-development-environment/#plugins) section could use a general intro about how plugins can be a useful part of testing and development. The list could probably use a review to make sure it's current. Some are not relevant to block themes (e.g., Monster Widgets).

## [Theme Development Examples](https://developer.wordpress.org/themes/getting-started/theme-development-examples/)

Primarily, this page needs to be fleshed out a bit more textually, providing more details about how it would be useful to look at these things. It wouldn't hurt to describe what audience each of the example themes cater to if possible (yes, most of the Twenty* themes are pretty general).

I'd also have separate "example sections" for both block and classic themes instead of mixing them in the same list.

I'll probably say this a lot in the analysis, but the page needs more visual _oomph_. Give the visitor something to look at to draw them into the provided examples.