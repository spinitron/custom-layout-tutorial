Web Integration with Spinitron
==============================

- JS Widgets
- Iframes
- API https://spinitron.github.io/v2api/
    ...and now also...
- Custom layout https://www.testradio.org/



Intro: The problem and solution
===============================

https://www.kcsb.org/schedule/

- widget
    - navigating to Spinitron pages from here is a problem

- iframe
    - has custom styles to make it look good
    - navigating Spinitron pages is ok
    - rectangle height doesn't adapt to the content
    - navigating elsewhere is weird
        - https://www.kcsb.org/6080-2/
        - in an iframe



## Principle: CSS is powerful medicine

http://www.csszengarden.com/



## Magic show 1

- https://www.artxfm.com/   beautiful!
- https://spinitron.com/WXOX/calendar?layout=1
    - navigation works: around spinitron pages
        - to-from artxfm pages
        - to elsewhere, e.g. paypal
- Web customization form in Spinitron: Admin



## Magic show 2

- https://www.wpr.org/   beautiful!
- https://spinitron.com/TEST/show/35116/Gold-Rox?layout=1
- https://www.wpr.org/news
- Web customization form



Test Radio dot ORG
==================

## Principle: Custom layouts is powerful medicine too

Switch PERSONA to TEST

- https://www.testradio.org/
    - has widgets
    - links
    - hamburger
- Web customization form: _SAVE CHANGES_
- https://spinitron.com/TEST/calendar?layout=1
- VIEW SOURCE



Simplest example
================

- https://spinitron.github.io/custom-layout-tutorial/index.html
    - view page source. close
- https://spinitron.github.io/custom-layout-tutorial/programs.html
    - view page source. close
- Web customization form
    - Only a layout. _SAVE CHANGES_
- https://spinitron.com/TEST/?layout=1
- Open dev tools: Inspect
## Principle: Browser Dev Tools also powerful medicine

- change background color, save in custom stylesheet
        .content .view-page {
            background: bisque;
        }
- hide the station head, save in custom stylesheet
        .content .view-page .head {
            display: none;
        }
- explain ancestors, more and less specific selectors, collisions



Tools
=====

- Text editor: e.g. MS Notepad, Apple Text Editor, VS Code, ...
- web search: CSS tutorial
- Browser dev tools
- https://github.com/spinitron/custom-layout-tutorial
    - hosting site for code repositories
    - web hosting for static web pages
- https://codepen.io/pen/
- https://jsfiddle.net/7bca8mvL/




Full example from scratch
=========================

- https://kxci.org/ and nav to https://kxci.org/programs/
- View page source, copy paste to NEW editor, stuff.html
- Inspect https://kxci.org/programs/ and choose a container
- in editor
    - get rid of `<div class="gridBlock">...</div>`
    - replace with `{{SPINITRON_CONTENT}}`
    - give container div `class="spinitron-content"`
- add rules one at a time from



Advanced example
================

WXOX



Advanced topics
===============

- Absolute/relative URLs
- The `<base>` tag
- Your vhost on our server with your host name
- CNAME in your domain records
- HTTPS
