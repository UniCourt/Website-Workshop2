# Introduction to CSS:
## What is CSS?
CSS (Cascading Style Sheets) is used to style and lay out web pages — for example, to alter the font, color, size, and spacing of your content, split it into multiple columns, or add animations and other decorative features. This module provides a gentle beginning to your path towards CSS mastery with the basics of how it works, what the syntax looks like, and how you can start using it to add styling to HTML.

1. ### Getting started with CSS:
    - **Box Model**: Everything displayed by CSS is a box. Understanding how the CSS Box Model works is therefore a core foundation of CSS.

        ![CSS Box Model](img/box_model.svg)

        - Explanation of the different parts:

            Content - The content of the box, where text and images appear.

            Padding - Clears an area around the content. The padding is transparent.

            Border - A border that goes around the padding and content.

            Margin - Clears an area outside the border. The margin is transparent.

    - **Selectors**: To apply CSS to an element you need to select it. CSS provides you with a number of different ways to do this, and you can explore them in this module.

        ![CSS Box Model](img/css_rule.svg)


    - **Color**: There are several different ways to specify color in CSS. In this module we take a look at the most commonly used color values.

        - Numeric colors #: It is very likely that your first exposure to colors in CSS is via numeric colors. We can work with numerical color values in a few different forms.

        Hex colors #: Hexadecimal notation (often shortened to hex) is a shorthand syntax for RGB, which assigns a numeric value to red green and blue, which are the three primary colors.

        ``` 
        h1 {
            color: #b71540;
        }

        ```
        
    - **Flexbox**: Flexbox is a one-dimensional layout method for laying out items in rows or columns. Items flex to fill additional space and shrink to fit into smaller spaces. This article explains all the fundamentals. After studying this guide you can test your flexbox skills to check your understanding before moving on.

        - What can you do with a flex layout? #: Flex layouts have the following features, which you will be able to explore in this guide.

        - They can display as a row, or a column.
        - They respect the writing mode of the document.
        - They are single line by default, but can be asked to wrap onto multiple lines.
        - Items in the layout can be visually reordered, away from their order in the DOM.
        - Space can be distributed inside the items, so they become bigger and smaller according to the space available in their parent.
    Space can be distributed around the items and flex lines in a wrapped layout, using the Box Alignment properties.
    The items themselves can be aligned on the cross axis.
