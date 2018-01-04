---
layout: post
title: Basic sections of a .html document
date: 2018-01-01
excerpt: "The HTML5 Basics"
tags: [post, code, html, css, snippet,]
feature: http://i.imgur.com/Ds6S7lJ.png
comments: false
---



HTML5 is the latest version of Hypertext Markup Language, the code that describes web pages. It's actually three kinds of code:
* HTML, which provides the structure;
* Cascading Style Sheets (CSS), which take care of the presentation;
* JavaScript, which helps makes the Website more interactive.


# Basic sections of a .html document
Webpages can and will look pretty different from one another, but they all tend to share similar standard components, unless the page is displaying a fullscreen video or game, is part of some kind of art project, or is just badly structured:

## header
Usually a big strip across the top with a big heading and/or logo. This is where the main common information about a website usually stays from one webpage to another.
navigation bar
Links to the site's main sections; usually represented by menu buttons, links, or tabs. Like the header, this content usually remains consistent from one webpage to another — having an inconsistent navigation on your website will just lead to confused, frustrated users. Many web designers consider the navigation bar to be part of the header rather than a individual component, but that's not a requirement; in fact some also argue that having the two separate is better for accessibility, as screen readers can read the two features better if they are separate.
## main content
A big area in the center that contains most of the unique content of a given webpage, for example the video you want to watch, or the main story you're reading, or the map you want to view, or the news headlines, etc. This is the one part of the website that definitely will vary from page to page!
## sidebar
Some peripheral info, links, quotes, ads, etc. Usually this is contextual to what is contained in the main content (for example on a news article page, the sidebar might contain the author's bio, or links to related articles) but there are also cases where you'll find some recurring elements like a secondary navigation system.
## footer
A strip across the bottom of the page that generally contains fine print, copyright notices, or contact info. It's a place to put common information (like the header) but usually that information is not critical or secondary to the website itself. The footer is also sometimes used for SEO purposes, by providing links for quick access to popular content.

<figure>
	<a href="https://mdn.mozillademos.org/files/12417/sample-website.png"><img src="https://mdn.mozillademos.org/files/12417/sample-website.png"></a>
	<figcaption>
    <a href="https://mdn.mozillademos.org/files/12417/sample-website.png" title="A sample website">A sample website</a>.
  </figcaption>
</figure>


# HTML for structuring content
The simple example shown above isn't pretty, but it's perfectly ok for illustrating a typical website layout example. Some websites have more columns, some are way more complex, but you get the idea. With the right CSS, you could use pretty much any element to wrap around the different sections and get it looking how you wanted, but as discussed before, we need to respect semantics, and use the right element for the right job.

This is because visuals don't tell the whole story. We use color and font size to draw sighted users' attention to the most useful parts of the content, like the navigation menu and related links, but what about visually impaired people for example, who might not find concepts like "pink" and "large font" very useful?

In your HTML code, you can mark up sections of content based on their functionality — you can use elements that represent the sections of content described above unambiguously, and assistive technologies like screenreaders can recognise those elements and help with tasks like "find the main navigation", or "find the main content." As we mentioned earlier in the course, there are a number of <a href="https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals#Why_do_we_need_structure">consequences of not using the right element structure and semantics for the right job</a>.

To implement such semantic mark up, HTML provides dedicated tags that you can use to represent such sections, for example:

 * header: `<header>`.
 * navigation bar: `<nav>`.
 * main content: `<main>`, with various content subsections represented by `<article>`, `<section>`, and `<div>` elements.
 * sidebar: `<aside>`; often placed inside `<main>`.
 * footer: `<footer>`.

# Explore the code for our examples
Look at the example above, and then look over the listing below to see what parts make up what section of the visual.


{% highlight html %}
{% raw %}
<!DOCTYPE html>
<!-- <!DOCTYPE html> This is the page Declaration.-->
<html lang="en">
<!-- <html lang="en"> This is the beginning of the page and we are setting the page language to English (en).-->
  <head>
    <meta charset="utf-8">

    <title>My page title</title>
    <link href="https://fonts.googleapis.com/css?family=Open+Sans+Condensed:300|Sonsie+One" rel="stylesheet" type="text/css">
    <link rel="stylesheet" href="style.css">

    <!-- the below three lines are a fix to get HTML5 semantic elements working in old versions of Internet Explorer-->
    <!--[if lt IE 9]>
      <script src="https://cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7.3/html5shiv.js"></script>
    <![endif]-->
  </head>

  <body>
    <!-- Here is our main header that is used across all the pages of our website -->

    <header>
      <h1>Header</h1>
    </header>

    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Our team</a></li>
        <li><a href="#">Projects</a></li>
        <li><a href="#">Contact</a></li>
      </ul>

       <!-- A Search form is another commmon non-linear way to navigate through a website. -->

       <form>
         <input type="search" name="q" placeholder="Search query">
         <input type="submit" value="Go!">
       </form>
     </nav>

    <!-- Here is our page's main content -->
    <main>

      <!-- It contains an article -->
      <article>
        <h2>Article heading</h2>

        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Donec a diam lectus. Set sit amet ipsum mauris. Maecenas congue ligula as quam viverra nec consectetur ant hendrerit. Donec et mollis dolor. Praesent et diam eget libero egestas mattis sit amet vitae augue. Nam tincidunt congue enim, ut porta lorem lacinia consectetur.</p>

        <h3>subsection</h3>

        <p>Donec ut librero sed accu vehicula ultricies a non tortor. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aenean ut gravida lorem. Ut turpis felis, pulvinar a semper sed, adipiscing id dolor.</p>

        <p>Pelientesque auctor nisi id magna consequat sagittis. Curabitur dapibus, enim sit amet elit pharetra tincidunt feugiat nist imperdiet. Ut convallis libero in urna ultrices accumsan. Donec sed odio eros.</p>

        <h3>Another subsection</h3>

        <p>Donec viverra mi quis quam pulvinar at malesuada arcu rhoncus. Cum soclis natoque penatibus et manis dis parturient montes, nascetur ridiculus mus. In rutrum accumsan ultricies. Mauris vitae nisi at sem facilisis semper ac in est.</p>

        <p>Vivamus fermentum semper porta. Nunc diam velit, adipscing ut tristique vitae sagittis vel odio. Maecenas convallis ullamcorper ultricied. Curabitur ornare, ligula semper consectetur sagittis, nisi diam iaculis velit, is fringille sem nunc vet mi.</p>
      </article>

      <!-- the aside content can also be nested within the main content -->
      <aside>
        <h2>Related</h2>

        <ul>
          <li><a href="#">Oh I do like to be beside the seaside</a></li>
          <li><a href="#">Oh I do like to be beside the sea</a></li>
          <li><a href="#">Although in the North of England</a></li>
          <li><a href="#">It never stops raining</a></li>
          <li><a href="#">Oh well...</a></li>
        </ul>
      </aside>

    </main>

    <!-- And here is our main footer that is used across all the pages of our website -->

    <footer>
      <p>©Copyright 2050 by nobody. All rights reversed.</p>
    </footer>

  </body>
</html>
{% endraw %}
{% endhighlight %}

Take some time to look over the code and try to understand it — the comments inside the code might also help you to understand it. No-one is asking you to do much else in this post, because the key to understanding the HTML document layout is writing a clean HTML structure, and then laying it out with CSS..
