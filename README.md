# Kreativ

A minimalistic theme for [Ghost](https://ghost.org/).

![Kreativ](assets/images/layout.jpg)

## Installation

1. Download the theme from GitHub.
2. Upload the theme as described in the [Ghost Documentation](http://docs.ghost.org/usage/settings/).

Looking for more instructions? Sorry, it's just that easy.

## Enabling Disqus Comments

If you want to enable comments, simply open `post.hbs` and remove the exclamation mark in the comments block, so `{{!> comments}}` becomes `{{> comments}}`.

You'll also need to enter your Disqus "shortname". Just head on over to the [Disqus](http://disqus.com/) website and register for an account. They'll give you a small snippet of code, but all we need from it is the following line:

    var disqus_shortname = 'YOUR_SHORTNAME_HERE';

Once you have that, just open `partials/comments.hbs` and replace the `YOUR_SHORTNAME_HERE` variable with the one Disqus gave you. Try not to edit any other settings or replace the code though, it's preconfigured to work with Ghost.

## Featured images

While featured images are not part of Ghost (yet), there are ways to implement them with some hacky Javascript. If you want to enable featured images, simply open `post.hbs` (and/or `page.hbs`) and remove the exclamation mark in the comments block, so `{{!> featured}}` becomes `{{> featured}}`. You can also remove the background-cover code from each file to prevent flashing content:

```
{{#if @blog.cover}}style="background-image: url({{@blog.cover}})"{{/if}}
```

This will remove the first image in your article and use it as the cover photo, so make sure you put a featured image at the top of your article.

