Github Flavored Markdown syntax
===============================

Paragraphs are separated by empty lines, **bold** uses __two__ asterisk or underline while *italic* uses _one_ only. ~~Strikethrough~~ and ``monospace`` by tilde and backquote. Inline `code` has only one backquote. Escape can be \*done\* by backslash preceding any of ``\ ` * _ { } [ ] ( ) # + - . !``. You can even [link to Google!](http://google.com "with optional tooltip") using a parenthesis for URL and square bracket for text.

Code block can be done by indentation of paragraph by 1-4 spaces

    like this

or without indentation but quoted by triple backquote (optionally language for syntax highlight):

```ruby
require 'red carpet'
markdown = Redcarpet.new("hello world")
```

Block quotes is indicated by >:
> like this, with *markups* supported

* ordered list
* with multiple
   - levels
   - with \* or - or + as bullets

1. Ordered list
2. is preceded by a number
    1. with nesting
    2. supported
3. List item in paragraph form or multiple lines.

   Like this one, can be done with leading spaces. Or to have  
   a line break without paragraph, keep two trailing space at  
   the line above. (GFM don't need trailing spaces)
4. Or a list item with code block

        needs to be indented by 8 spaces

And horizontal rules can be done by three or more

---
hyphens
***
asterisks
___
or underscores


Tables
------
GFM supports tables.

Tables  | Can be done
--------|------------
By using|pipes
and     |hyphens
even dashes and pipes|not perfectly line up
and markups|can *also* ~~be~~ used

|Left-aligned|Center-aligned|Right-aligned    |
|:-----------|:------------:|----------------:|
|columns     |can be done   |with             |
|colons      |at the        |header row       |
|extra pipes |at both ends  |are only aesthetic|


Headers
-------
Headers are underlined by = (H1 header) or - (H2 header). Alternatively, H1 to H6 of HTML can also be marked by 1 to 6 leading # sign at the line, like

### this is h3
#### and this is h4 with optional close hashes ########


Links
-----
Besides [link like this](http://www.google.com), we can also have [relative links](../dir/file.txt) or [reference-style link][myref] or [numbered-reference][1] or [simply the link text] or type in URL directly http://slashdot.org or <http://github.com>

Remember to define the links somewhere.

[myref]: http://example.com/
[1]: http://example.org/
[simply the link text]: http://example.net/


Images
------
Images are links with leading exclamation mark (hover to see the title text):

Inline-style: 
![alt text](https://github.com/favicon.ico "Fav Icon")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/favicon.ico "Fav Icon"


Task list
---------
Part of GFM,
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

HTML
----
Markdown supports inline HTML, such as linking youtube

<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>


Others
------
Emoji :smile: :alien: :v: at http://www.emoji-cheat-sheet.com/
