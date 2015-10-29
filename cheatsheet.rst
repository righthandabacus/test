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


In summary, these are supported inline markup:

*italic*; **bold**; `interpreted text`; `interpreted text
with role`:emphasis:; ``inline literal text``; standalone hyperlink,
http://docutils.sourceforge.net; named reference, reStructuredText_;
`anonymous reference`__; footnote reference, [1]_; citation reference,
[CIT2002]_; |substitution|; _`inline internal target`.


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


Links, footnotes, and citations
===============================
.. _`this section`:

External links, like Google_ or `Slashdot <http://slashdot.org>`_ or anonymously __http://duckduckgo.com. Note the underscore character.

.. _Google: http://www.google.com

And if you have a target, we can make an `indirect target`__

__ Google_


Internal target like the top of `this section`_, or `Links, footnotes, and citations`_ section title is also a target implicitly. Or define an inline internal target like _this and you can use like this_.

Similar to link is footnotes [1]_ which may be rearranged [#]_ with auto-numbering or [#label]_ labeled. Besides number, we can [*]_ make auto-symboled [*]_ foot notes as well.

.. [1] This is a footnote
.. [#] Auto-numbered footnote
.. [#label] and auto-numbered but labeled footnote, aka label_
.. [*] Symboled footnote
.. [*] Another symbol

Text enclosed in square bracket is citations [CIT01]_. And citation labels can contain alphanumerics (case insensitive), underlines, hyphens, and fullstops [like-this]_. Once a citation is created, it is a target too, like cit01_.

.. [Cit01] John Doe, ''An article'', 2001.
.. [like-this] Citation text here

Images and substitutions
========================
Images is a directive with optional parameters

.. image:: https://github.com/favicon.ico
    :height: 50
    :width: 50
    :scale: 100

And using substitution is the only way to make inline |icon| pictures.

.. |icon| image:: https://github.com/favicon.ico


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

Example

.. math:
     \frac{1}{\sqrt{2\pi\sigma^2}}\int_{-\infty}^{\infty} \exp(-\frac{x^2}{2\sigma^2}) dx


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
