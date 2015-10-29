=======================
reStructuredText syntax
=======================
:Author: Adrian
:Info: This file is located at http://github/righthandabacus
:Date: Thu Oct 29 01:02:11 EDT 2015
:Revision: 0.1
:Description: Experimenting all rst features. This is the "docinfo block" for bibliographic data

Paragraphs are separated by empty lines, **bold** uses two asterisk while *italic* uses one. ``Monospace`` by backquote. Escape can be \*done\* by backslash preceding any character.

Literal block is introduced by double colon::

    like this with indentation

or without colons, as block quotes:

    like this with indentation
        and they may nest

or even quote using double colon and > if no indent::

> like this

But it is a doctest block if we

>>> print "type like python shell"
type like python shell

| Line blocks is to preserve line breaks and indents.
|     We simply begin the lines with pipe to make
|  a line block.

Other supported inline markups are 'interpreted text', 'interpreted text with role':emphasis:, standalone links http://www.google.com

----

and horizonal rule is four or more dashes.

.. Two leading dots marks comment, which will not be shown in output
   but preserved in raw text. (comment text can be empty too)


Lists
=====
* unordered list
   - with multiple
     + levels
* with \* or - or + as bullets

1. Ordered list
2. is preceded by "1." or "A." or "(i)" or "#.", etc.
    a. with nesting
    b. supported
3. List item in paragraph form or multiple lines.

   Like this one, is also supported.
4. Or a list item with code block

        needs to be indented by 8 spaces


Tables
------
reStructuredText support grid tables:

+-------+----------+------+
| Table Headings   | Here |
+-------+----------+------+
| Sub   | Headings | Too  |
+=======+==========+======+
| cell  | column spanning |
+ spans +----------+------+
| rows  | normal   | cell |
+-------+----------+------+
| multi | * cells can be  |
| line  | * formatted     |
| cells | * paragraphs    |
| too   |                 |
+-------+-----------------+

and simple tables:

===== ========= =====
Table Headings  Here
--------------- -----
Sub   Headings  Too
===== ========= =====
column spanning no
--------------- -----
cell  cell      row
column spanning spans
=============== =====


Headers
-------
Headers are underlined or under- and overlined by ``-`` ``=`` or ``~``. Same style means section of same level. Document title is the unique section header at the beginning of document.


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
