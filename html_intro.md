# Introduction to HTML:
## What is HTML?
HTML (Hypertext Markup Language) is the code that is used to structure a web page and its content. 

HTML is a markup language that defines the structure of your content. HTML consists of a series of elements, which you use to enclose, or wrap, different parts of the content to make it appear a certain way, or act a certain way. The enclosing tags can make a word or image hyperlink to somewhere else, can italicize words, can make the font bigger or smaller, and so on.

![HTML Structure](img/img_sem_elements.gif)


1. ### Getting started with HTML:
    - Document structure

        ```
        <!DOCTYPE html>
        <html lang="en">
            <head>
                <meta charset="utf-8">
                <title>HTML & CSS Learning Workshop Blog</title>
                <meta content="width=device-width, initial-scale=1" name="viewport" />
            </head>
            <body>

            </body>
        </html>
        ```
        - ```<!DOCTYPE html> ```
            The first thing in any HTML document is the preamble. For HTML, all you need is ```<!DOCTYPE html>```. This may look like an HTML element, but it isn't. It's a special kind of node called "doctype". The doctype tells the browser to use standards mode. If omitted, browsers will use a different rendering mode known as quirks mode. Including the doctype helps prevent quirks mode.

        - ```<html>```
            The `<html>` element is the root element for an HTML document. It is the parent of the `<head>` and `<body>`, containing everything in the HTML document other than the doctype. If omitted it will be implied, but it is important to include it, as this is the element on which the language of the content of the document is declared.

        - ```<html lang="en">```
            The lang language attribute added to the `<html>` tag defines the main language of the document.

        - ```<head>```
            The `<head>`, or document metadata header, contains all the metadata for a site or application. The body contains the visible content. The rest of this section focuses on the components found nested inside the opening and closing `<head></head>`

            - Components inside the `<head>`

                - The document metadata, including the document title, character set, viewport settings, description, base URL, stylesheet links, and icons, are found in the <head> element. While you may not need all these features, always include character set, title, and viewport settings.

                - Character encoding #
                    The very first element in the <head> should be the charset character encoding declaration. It comes before the title to ensure the browser can render the characters in that title and all the characters in the rest of the document.

                - Document title #: Your home page and all additional pages should each have a unique title. The contents for the document title, the text between the opening and closing `<title>` tags, are displayed in the browser tab, the list of open windows, the history, search results, and, unless redefined with `<meta>` tags, in social media cards.

                - Viewport metadata #: The other meta tag that should be considered essential is the viewport meta tag, which helps site responsiveness, enabling content to render well by default, no matter the viewport width. While the viewport meta tag has been around since June 2007, when the first iPhone came out, it's only recently been documented in a specification. As it enables controlling a viewport's size and scale, and prevents the site's content from being sized down to fit a 960px site onto a 320px screen, it is definitely recommended.


    - Basic structure of HTML Element. Consider the following example:

        ```
        <p>My First HTML Code.</p>

        ```
    - The anatomy of our element is:

        - The opening tag: This consists of the name of the element (in this example, p for paragraph), wrapped in opening and closing angle brackets. This opening tag marks where the element begins or starts to take effect. In this example, it precedes the start of the paragraph text.
        - The content: This is the content of the element. In this example, it is the paragraph text.
        - The closing tag: This is the same as the opening tag, except that it includes a forward slash before the element name. This marks where the element ends. Failing to include a closing tag is a common beginner rror that can produce peculiar results.

    - Nesting Elements:
        - Elements can be placed within other elements. This is called nesting.
        
        ```
        - <p>My First <strong>HTML</strong> Code.</p>

        ```
    - Block and Inline Elements
        - A Block level element appears on a new line following the content that preceds it. Any content that follows a block-level element also appears on a new line. Example `<div>`, `<p>`, `<section>`.
        - A Inline elements are contained within block-level elements, and surrond only small parts of the document's content. Example `<a>`, `<em>`, `<strong>`

    - Empty Elements:
        - Not all elements follow the pattern of an opening tag, content, and a closing tag. Example `<img />`, `<br />`, `<hr />`
    
