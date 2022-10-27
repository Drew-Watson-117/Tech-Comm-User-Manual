# Markdown
Markdown is a light markup language. It enables easy and quick formatting of headers, lists, and text formatting. It is an alternative to systems such as Word and Latex. In Markdown we use symbles around text to denote heades, bolding, or lists. This creates a system that is faster to create and edit than Word and less complex than Latex. It is also able to be converted into HTML and PDF's with ease. Because of these reasons it will be used as the editor for the manual. This also provides us with our baseline styling.

We will be using the default options that come in Markdown. This controls the font size, spacing and the color. While these could be changed, it provides us with a strong base line. The font that is used in Markdown is Noto Sans with black text (#000000) on white background to maintain a professional look. Markdown also controls the heading, subheading, and body text. A ```#``` is used to change the text to headers, more denotes smaller text. The largest challenge with Markdown will be the page numbers and the table of contents. Pandoc will be used to generate these for use. This means each chapter must be its own seperate Markdown file so it can be generated into a PDF at the end.

## Our Header Styles:

# Our Titles Will Be Header 1
## Our Main Sections Will Be Header 2
### Subheading will be Header 3, 4,... as appropriate
The way we to create a Headers in Markdown is using the **``#``** symbol. For Header 1 it will be a single ``#`` in front of our Titles. Inside of Markdown, each additional ``#`` symbol creates a smaller header up to 6. 

## Our List Styles:
- Unordered lists will be bullet points
	- With sub bullets being tabbed over

1. Ordered list will be numbers
	1. With sub bullets also being numbers and tabbed over

## Our Code Block Style:
In Markdown there are several ways to format code blocks. The two ways would be indenting the entirety of the code by four spaces or using backticks before and after the code block; one backtick for a single line code block, and three backticks for a multi-line code block. For our documentation for all code blocks we will be using the backticks before and after a code block. One backtick will be used for single line code blocks, and three backticks will be used for a multi-line comment. A line of white space will be put before and after each code block. When code blocks are used in an in-line fashion, single backticks will be used. An example of the formatting for code blocks is given below:

`Single line code block goes here`

 ```
 Multi-line code block goes here
```

## Our Images Style:

Images in our style guide will include alterante text for screen readers and other accsesibility features. Images will include a 10 dp padding margin to offset any elements that surround our image. Images will also be formatted to stlye around text and not be large enough to override page dimensions like height and width. 

For any document links, the style guide specifies they must be imbedded into text that most closely corresponds with information about the link. (Example - "There is more info *[here](https://github.com/Drew-Watson-117/Tech-Comm-User-Manual/blob/master/Style%20Guide.md)*)" 

Emails will also follow the same format as links but when clicked upon, prompt the user to send an email to the selected email. (Example - "This is my *[email](mailto:dummyemail@email.com)*.")

## Our Quotes Style
For any long quote passages potentially referencing academic sources, our style guide will use blockquotes. Blockquotes will offset text to indicate a quote and distinuish the text from the rest of the document. The symbol for that would just be ```>``` for the start of the block quote.
Example - 
>Dorothy followed her through many of the beautiful rooms in her castle.

## Our Math Style
To indicate any mathematical symbols the style guide will use the code formatting from markdown and use the built in math notatation for mathematical operations. 
The symbol for math would be the same as MatLab and would be ```$``` before and after the code.  
Example - 
$E=mc^2$