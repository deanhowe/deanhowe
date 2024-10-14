---
title: 'Markdown 2024'
icon: 'o-rocket-launch'
-icon-class: ''
-link-url: '#moof-digital'
-link-title: 'Moof Digital'
-link-icon: 's-arrow-small-right'
-content: 'snippets/04b-moof-digital.md'
-figure-background: 'images/thumbs/moof-digital.png'
-figure-alt: 'MOOF Digital'
---

# Markdown

Markdown is a *__style__* of writing.

It is the __simplest__ way to write *formatted* content for the web without the need for additional programs or tools.
It should be easy to read and write, I promise.

The code snippet below is an example of writing a large header in a document.

```markdown
# Titles or "_Headers_" come in sizes [1-6] - __H1__ (*Header One*)
```

When you read the snippet above (you need to read the snippets) it should read as follows:
 > Titles or Headers come in sizes one to six - this is a H1 (Header One)…

We don’t tend to pronounce the hashtag `#`, underscore `_`, square brackets `[]` or astrix `*` when reading Markdown, those symbols are there instead to denote the styling of the word. 

Titles or "_Headers_" come in sizes [1-6] they are denoted by the number of `#` symbols before the text. For historical, SEO, and schematic reasons documents should only ever have one `<H1>` tag. So the Markdown above is not rendered om this page :sadface:  (neither is that emoji?) hold my :coffee: :smirk:.

From this point on, the Markdown will be displayed first, then the rendered HTML (formatted text), followed by the raw HTML.


```markdown
## Title or "_Header_" in 2nd size - __H2__ (*Header Two*) = \#\#
```

## Title or "_Header_" in 2nd size - __H2__ (*Header Two*) = \#\#

```html
<h2>Title or "<em>Header</em>" in 2nd size 
    - this is a <strong>H2</strong> (<em>Header Two</em>) = ##</h2>
```

As you can see the HTML is much longer than the Markdown, so long it required a line break to fit on the page, and the Markdown is much easier to read?

Admittedly, the theme isn't doing any justice to the HTML.

Yes, HTML is more powerful, but the Markdown is easier to read and write. Have you spotted the [emoji's](./markdown-emoji) yet? :smirk:

We follow the [CommonMark Spec](https://spec.commonmark.org/0.31.2/) for Markdown, which is a standard for Markdown. @daringfireball the creator of Markdown, has a [Markdown Syntax Guide](https://daringfireball.net/projects/markdown/syntax) that is worth a read.

The following text a common example of the power of Markdown:

```markdown
1.  List item one.
```

1. List item one opens with an open block of text and another ordered list.

    This paragraph (open block) is part of the preceding list item.

    1. This list is nested and does not require explicit item continuation.

       This paragraph is part of the preceding list item.

       Notice the Markdown does not require actual numbers for the list.

   1. List item 2 of the nested list.
      
      This text is __bold__ this text is _italic_

      This text is **bold** this text is *italic*

      This text is _**bold and italic**_ this text is *__bold and italic__*

   1. List item three of the nested block, take note of the formatting difference from above

      This text is __bold__ this text is _italic_
      This text is **bold** this text is *italic*
      This text is _**bold and italic**_ this text is *__bold and italic__*

   This paragraph belongs to the outer list item, notice the indent.

   Well done for reading this far. Did you notice formatting difference? It was todo with line-break, carriage returns, pressing enter. <br><br>
   Now I know we said no `HTML` but we might need use the `<br>` tag here and there :hmm:… 
 
1. List item two, you're still reading right?

    List item two continues with a second paragraph followed by an
    Indented block that gets wrapped in a fancy code block `<code></code>`.

        $ ls *.sh
        $ mv *.sh ~/tmp

    List item two continues with a third paragraph. And the reason I'm wondering if you're still reading is because most people skim read this stuff.
    Notice how code is denoted `inline` with backticks __`__. 

1. We are still making an ordered list
2. I've numbered this incorrectly, on purpose, it's :one_oclock:
1. And I'm skipping the spacing
1. My friends are literally all out partying :party_popper: :partying_face:
13. Are these numbered correctly?
666. Markdown 
     * doesn't really care…
     * it can also create **_un-ordered lists_**
     * which can…
       * be nested
         * just as
           * deep
             * as you
               * like
           * ROMAN :classical_building: Numerals
             1. do they work {type="i"}
               > check this out
                >> :exploding_head: 
             1. not sure
     * Numerals or letters?
1. What else can we do?[^1] 
1. Add code blocks…[^codeblocks]

   ```php{1,2}{3}
   <?php

   echo "Hello World";
   echo "We're highlighting line 1 and 2";
   echo "And focusing line 3";

   ?> 
   ```
    
   Should be a "Hello World" in PHP, above?. With a highlight on lines 1 & 2 and focus on line 3?

This is *red*{style="color: red"}, *green*{class="text-green-500"}, *blue*{class="text-blue-900"}.

{#purple-heading style="color:purple;"}
### A Purple heading

{#crimson-heading style="color:crimson;"}
### A Crimson heading


Apple{style="color:crimson;"}
:   Pomaceous fruit of plants of the genus Malus in the family Rosaceae.
:   An American computer company.

Orange
:   The fruit of an evergreen tree of the genus Citrus.

#### Quick Question - Does pineapple belong on pizza?
( ) Yes, pineapple belongs on pizza!
( ) Are you serious? Pineapple on pizza?!
( ) Pineapple on pizza is a crime against pizza!

```mermaid
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
```

> [!NOTE]
> Highlights information that users should take into account, even when skimming.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]
> Critical content demanding immediate user attention due to potential risks.

1. [emoji](./markdown-emoji.md)
1. [embeds](./markdown-embeds.md)

The formula for water is H<sub>2</sub>O
while the equation for the theory of relativity is E = mc<sup>2</sup>.

Press <kbd>Enter</kbd> to go to the next page.


[^1]: This text is inside a footnote.
[^codeblocks]: Code blocks should be styled & themed depending on the language.
