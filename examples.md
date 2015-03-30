# Sample Github Flavored Markdown File for Testing

## Overview

GitHub uses "[GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/)," or GFM, across the site--in issues, comments, and pull requests. It differs from _standard Markdown_ (SM) in a few significant ways, and adds some additional functionality.

### Differences from traditional Markdown

#### Fenced code blocks

<!--- Standard Markdown converts text with four spaces at the beginning of each line into a code block; GFM also supports fenced blocks. Just wrap your code in ``` (as shown below) and you won't need to indent it by four spaces. Note that although fenced code blocks don't have to be preceded by a blank line—unlike indented code blocks—we recommend placing a blank line before them to make the raw Markdown easier to read.

Here's an example: --->

```
function test() {
  console.log("notice the blank line before this function?");
}
```

<!--- Keep in mind that, within lists, you must indent non-fenced code blocks eight spaces to render them properly. --->

#### Syntax highlighting

<!--- Code blocks can be taken a step further by adding syntax highlighting. In your fenced block, add an optional language identifier and we'll run it through syntax highlighting. For example, to syntax highlight Ruby code: --->

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
GitHub uses [Linguist](https://github.com/github/linguist) to perform language detection and syntax highlighting. You can find out which keywords are valid by perusing [the languages YAML file](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml).

#### Strikethrough

GFM adds syntax to create ~~strikethrough text~~, which is missing from standard Markdown.

#### Tables

<!--- You can create tables by assembling a list of words and dividing them with hyphens - (for the first row), and then separating each column with a pipe |:

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

For aesthetic purposes, you can also add extra pipes on the ends. The dashes at the top don't need to match the length of the header text exactly. You can also include inline Markdown such as links, bold, italics, or strikethrough:

| Name | Description          |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |

Finally, by including colons : within the header row, you can define text to be left-aligned, right-aligned, or center-aligned: --->

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| data 1     | ~~wrong text~~ | 11 |
| data 2      | **centered**        |   22 |
| [company](http://www.outlearn.com)  | *teaches*        |    33 |

<!--- A colon on the **left-most** side indicates a left-aligned column; a colon on the **right-most** side indicates a right-aligned column; a colon on **both** sides indicates a center-aligned column. --->

#### Multiple underscores in words

Where Markdown transforms underscores into italics, GFM ignores underscores in words, like this:

>do_this_and_do_that_and_another_thing.

<!--- This allows code and names with multiple underscores to render properly. To emphasize a portion of a word, use asterisks. --->

#### URL autolinking

GFM will autolink standard URLs, so if you want to link to a URL (instead of setting link text), you can simply enter the URL and it will be turned into a link to that URL: http://example.com

#### HTML

You can use a subset of HTML within your READMEs, issues, and pull requests. A full list of our supported tags and attributes can be found in the [README for github/markup](https://github.com/github/markup/tree/master#html-sanitization).

### Syntax for Regular Markdown

#### Strong and Emphasize

**strong** or __strong__

*emphasize* or _emphasize_

**Combine bold and _italics_ in on place.**

#### Blockquotes

> Right angle brackets &gt; are used for block quotes.

> > This is nested blockquote.
>
> Back to the first level.

#### Regular code highlighting

`` Code here to be read ``

A single backtick in a code span: `` ` ``

A backtick-delimited string in a code span: `` `foo` ``

#### Links and Email

Sample email: <example@outlearn.com>.

Inline link <http://www.outlearn.com>, another inline link [Outlearn](http://www.outlearn.com), one more inline link with title [Outlearn](http://www.outlearn.com "Developer Learning").

A [reference style][id] link. Define link content later.

[id]: http://www.outlearn.com "Open Source Learning"


#### Images

An inline image ![Outlearn icon](http://www.outlearn.com/favicon.ico "Title here"), title is optional.

A ![Resize icon][2] reference style image.

[2]: http://www.outlearn.com/favicon.ico "Outlearn Title"

####  Ordered Lists

1. list item
2. list item
3. list item

#### Unordered Lists

* list item
- list item
+ list item

*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.
*   A list item with a code block:

		     <code goes here>

#### Hard Linebreak

End a line with two or more spaces to create a hard brake.  
Above line ended with 2 spaces.

#### Horizontal Rules

Three or more asterisks or dashes:

***

---

- - - -


#### Headers

Setext-style:

This is an H1
=============

This is an H2
-------------

atx-style:

# This is H1
## This is H2
### This is H3
#### This is H4
##### This is H5
###### This is H6


### Extra Syntax

#### Footnotes

GitHub does not support footnotes. But here is a sample footnote for other platforms.

Main text.[^1]

[^1]: Footnote.
