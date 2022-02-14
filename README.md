# learning-git

This repo was used to learn Git from amigoscode.

https://youtu.be/3fUbBnN_H2c

1:25:47 -- Git Workflow

# git test
Hello Odin!

# git cheatsheet
Commmands related to a remote repository:
.. git clone git@github.com:km3gna/learning-git.git
.. git push or git push origin main

Commands related to workflow:
.. git add .
.. git commit -m "Memo describing what was done to make this snapshot different"

Commands related to checking status or log history:
.. git status
.. git log

Basic Git syntax is "program | action | destination":
.. git add .  >>  git | add | . (period represents everything in current directory)
.. git commit -m "message"  >>  git | commit -m | "message"
.. git status  >>  git | status | (no destination)

Best practices:
.. atomic commits (commit that includes changes related to only one feature or task of your program)
.. leveraging those atomic commits

Why?
.. (1) if something you change turns out to cause problems, it is easy to revert the specific change without losing other changes
.. (2) enables you to write better commit messages

Changing the Git Commit Message Editor:
.. Using VSCode and don't want to get stuck writing a commit message in Vim (git commit without message flag, -m)
.. git config --global core.editor "code --wait"
.. above command will open a new tab in VSCode with the ability to write commit message and an optional description below it; save, exit

# HTML
macOS/navigate to directory containing file and use:
open ./index.html

VSCode built-in shortcut to generate boilerplate in one go.
In index.html, type '!' on the first line, press enter (choose first one).

.. HTML ELEMENTS
    - <div> (empty container; for simplicity)
    - <h1> to <h6>
    - <p>

.. SELECTORS
    - * (Universal Selector; every element)
    - div, p, etc. (Type Selector)
    - .class-attribute (Class Selector)
    - #id-attribute (ID Selector; use sparingly; cannot be repeated on a single page, should not contain any whitespace)
    - .selector1, .selector2 (Grouping Selector)
    - .selector1.selector2 (Chaining Selector)
    - .selector1 .selector2 (Descendant Combinator)

.. SPECIFICITY (highest to lowest)
    - ID selectors
    - Class selectors
    - Type selectors
    - Last rule defined

.. CSS

    <link rel="stylesheet" href="styles.css">
    /* styles.css */

    OR

    <style>
    </style>

    OR

    <selector_type style="...">...</selector_type>


# The Box Model

.. master POSITIONING and LAYOUT
.. make sure elements are just the right size with MARGIN, PADDING, and BORDERS
.. every single thing on a webpages is a RECTANGULAR BOX    (Can use browser's inspector to add the CSS ( * {border: 2px solid red;} )
.. PADDING -- space between the edge of a box and the content inside of it
.. MARGIN -- space between a box and any others that sit next to it
.. BORDER -- space (even a pixel or two) between the MARGIN and the PADDING

?? PX vs EM vs REM vs %

.. BOX-SIZING -- turn on the alternative model for an elements
    .box {
        box-sizing: border-box;
    }
    ( tells browser to use the border box as the defined area )
    
    html {
        box-sizing: border-box;
    }
    *, *:: before, *::after {
        box-sizing: inherit;
    }
    ( common choice among developer is to set the box-sizing property on the <html> element, then set all other elements to inherit that value )

.. BLOCK BOXES and INLINE BOXES ( INNER DISPLAY TYPE and OUTER DISPLAY TYPE )
    .. OUTER DISPLAY TYPE (details whether the box is BLOCK or INLINE)
    .. INNER DISPLAY TYPE (dictates how elements inside the box are laid out; default is NORMAL FLOW)
        .. Can change the INNER DISPLAY TYPE by using display values like FLEX
            - If ( display: flex; ) on an element, outer display is BLOCK but inner display type is FLEX
            - Any direct children of this box will become FLEX items (FLEXBOX rules)
                - FLEXBOX -- 1D layout method (arranging items in rows or columns)
                - FLEX = expand; fill additional space or shrink to fit smaller spaces)
                - AUTO is only useful for horizontal centering; specified width and L/R MARGINS set to AUTO (will not center vertically)
                - 

    .. BLOCK (OUTER) ("Y-AXIS") (In vertical writing mode, laid out horizontally; BLOCK = "X-AXIS", INLINE = "Y-AXIS")
        - break onto a new line
        - extend in the inline direction (box becomes as wide as its container, filling 100% space available)
        - width and height properties are respected
        - padding, margin and border will cause other elements to be pushed away from the box
        - some HTML elements (<h1>, <p>, ...) use BLOCK as OUTER DISPLAY by default

    .. INLINE (OUTER) ("X-AXIS")
        - does NOT break onto a new line
        - width and hegith properties do NOT apply
        - vertical padding, margin and border apply but does NOT cause other inline boxes to move away from the box
        - horizontal padding, margin and border apply and cause other inline boxes to move away from the box
        - some HTML elements (<a>, <span>, <em>, <strong>, ...) use INLINE as OUTER DISPLAY by default
    
    .. COLLAPSING MARGINS
        - Vertical margins (T/B) on different elements touching each other (no content, padding, or borders separating them) >> Collapse
        - Collapse -- forming a single margin equal to the greater of the adjoining margins
        - Does not apply to horizontal margins (L/R)
        - Useful because...
            - prevents empty elements from adding extra (undesirable) vertical margin space
            - allow for a more consistent approach to declaring universal margins across page elements
            - applies to nested elements (removes need to redefine any of the top margins)
    
    .. NEGATIVE MARGINS
        - Pulls element in that direction or other elements towards it

    .. INLINE FORMATTING
        ?? ANONYMOUS BOXES...
        - LINE BOX SIZE (block direction) is defined by the tallest box inside it

    
 
