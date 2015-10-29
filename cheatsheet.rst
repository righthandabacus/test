=======================
reStructuredText syntax
=======================
:Author: Adrian
:Info: This file is located at http://github/righthandabacus
:Date: Thu Oct 29 01:02:11 EDT 2015
:Revision: 0.1
:Description: Experimenting all rst features. This is the "docinfo block"
              for bibliographic data

Paragraphs are separated by empty lines, **bold** uses two asterisk while *italic* uses one. ``Monospace`` by backquote. Escape can be \*done\* by backslash preceding any character.

Literal block is introduced by double colon::

    like this with indentation

or > if no indent::

> like this

or without colons, as block quotes:

    like this with indentation
        and they may nest

But it is a doctest block if we

>>> print "type like python shell"
type like python shell

| Line blocks is to preserve line breaks.
| We simply begin the lines with pipe to make
  a line block. But a line without leading pipe
  is continuation of last line.

Other supported inline markups are `interpreted text`, `interpreted text with role`:emphasis:, standalone links http://www.google.com

----

and horizontal rule is four or more dashes.

.. Two leading dots marks comment, which will not be shown in output
   but preserved in raw text. (empty comment is two dots with empty
   lines before and after)


Lists
=====
* unordered list
   - with multiple
     + levels
* with \* or - or + as bullets

1. Ordered list
2. Is preceded by ``1.`` or ``A.`` or ``(i)`` or ``#.`` (auto numbered), etc.
    a. with nesting
    b. supported
3. List item in paragraph form or multiple lines.

   Like this one, is also supported.
4. Or a list item with code block

        needs to be indented by 8 spaces


Tables
======
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
=======
Headers are underlined or under- and overlined by ``-`` ``=`` or ``~``. Same style means section of same level. Document title is the unique section header at the beginning of document.


Links
=====
Besides [link like this](http://www.google.com), we can also have [relative links](../dir/file.txt) or [reference-style link][myref] or [numbered-reference][1] or [simply the link text] or type in URL directly http://slashdot.org or <http://github.com>

Remember to define the links somewhere.

[myref]: http://example.com/
[1]: http://example.org/
[simply the link text]: http://example.net/


Images
======
Images is a directive with optional parameters

.. image:: favicon.co
    :height: 50
    :width: 50
    :scale: 100



================  ============================================================
Explicit Markup   Examples (visible in the `text source`_)
================  ============================================================
Footnote          .. [1] Manually numbered or [#] auto-numbered
                     (even [#labelled]) or [*] auto-symbol
Citation          .. [CIT2002] A citation.
Hyperlink Target  .. _reStructuredText: http://docutils.sf.net/rst.html
                  .. _indirect target: reStructuredText_
                  .. _internal target:
Anonymous Target  __ http://docutils.sf.net/docs/ref/rst/restructuredtext.html
Directive ("::")  .. image:: images/biohazard.png
Substitution Def  .. |substitution| replace:: like an inline directive
Comment           .. is anything else
Empty Comment     (".." on a line by itself, with blank lines before & after,
                  used to separate indentation contexts)
================  ============================================================


Inline Markup
=============
*emphasis*; **strong emphasis**; `interpreted text`; `interpreted text
with role`:emphasis:; ``inline literal text``; standalone hyperlink,
http://docutils.sourceforge.net; named reference, reStructuredText_;
`anonymous reference`__; footnote reference, [1]_; citation reference,
[CIT2002]_; |substitution|; _`inline internal target`.

Directive Quick Reference
=========================
See <http://docutils.sf.net/docs/ref/rst/directives.html> for full info.

================  ============================================================
Directive Name    Description (Docutils version added to, in [brackets])
================  ============================================================
attention         Specific admonition; also "caution", "danger",
                  "error", "hint", "important", "note", "tip", "warning"
admonition        Generic titled admonition: ``.. admonition:: By The Way``
image             ``.. image:: picture.png``; many options possible
figure            Like "image", but with optional caption and legend
topic             ``.. topic:: Title``; like a mini section
sidebar           ``.. sidebar:: Title``; like a mini parallel document
parsed-literal    A literal block with parsed inline markup
rubric            ``.. rubric:: Informal Heading``
epigraph          Block quote with class="epigraph"
highlights        Block quote with class="highlights"
pull-quote        Block quote with class="pull-quote"
compound          Compound paragraphs [0.3.6]
container         Generic block-level container element [0.3.10]
table             Create a titled table [0.3.1]
list-table        Create a table from a uniform two-level bullet list [0.3.8]
csv-table         Create a table from CSV data [0.3.4]
contents          Generate a table of contents
sectnum           Automatically number sections, subsections, etc.
header, footer    Create document decorations [0.3.8]
target-notes      Create an explicit footnote for each external target
math              Mathematical notation (input in LaTeX format)
meta              HTML-specific metadata
include           Read an external reST file as if it were inline
raw               Non-reST data passed untouched to the Writer
replace           Replacement text for substitution definitions
unicode           Unicode character code conversion for substitution defs
date              Generates today's date; for substitution defs
class             Set a "class" attribute on the next element
role              Create a custom interpreted text role [0.3.2]
default-role      Set the default interpreted text role [0.3.10]
title             Set the metadata document title [0.3.10]
================  ============================================================


Interpreted Text Role Quick Reference
=====================================
See <http://docutils.sf.net/docs/ref/rst/roles.html> for full info.

================  ============================================================
Role Name         Description
================  ============================================================
emphasis          Equivalent to *emphasis*
literal           Equivalent to ``literal`` but processes backslash escapes
math              Mathematical notation (input in LaTeX format)
PEP               Reference to a numbered Python Enhancement Proposal
RFC               Reference to a numbered Internet Request For Comments
raw               For non-reST data; cannot be used directly (see docs) [0.3.6]
strong            Equivalent to **strong**
sub               Subscript
sup               Superscript
title             Title reference (book, etc.); standard default role
================  ============================================================


Others
======
Emoji :smile: :alien: :v: at http://www.emoji-cheat-sheet.com/
