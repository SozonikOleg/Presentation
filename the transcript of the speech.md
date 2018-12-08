Task Presentation RS2018.
Hello!

What is flexbox?

The Flexible Box Module, usually referred to as flexbox, was designed as a one-dimensional layout model, and as a method that could offer space distribution between items in an interface and powerful alignment capabilities.


HISTORY
Pre 2008 Css Working Group proposes idea for Flexbox

2009 Flexbox's first working draft published

2011 Tab Atkins takes over as Flexbox spec edition Flexbox spec edition

Late 2011 "Tweener" syntax published

2012 Becomes a W3C Candidate Recommendation

2013 W3C Working Draft published

2015 New syntax


FLEXBOX OVERVIEW
Flexbox uses two types of boxes that we’ve never seen before: “flex containers” and “flex items”. The job of a flex container is to group a bunch(банч) of flex items together and define how they’re positioned.

DISPLAY
This defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.

ALIGNING A FLEX ITEM
After you’ve got a flex container, your next job is to define the horizontal alignment of its items. That’s what the justify-content property is for.

This has the same effect as adding a margin: 0 auto declaration to the (.menu) element. But, notice how we did this by adding a property to the parent element (the flex container) instead(инстэд) of directly to the element we wanted to center (the flex item)
Other values for justify-content:

center
flex-start
flex-end
space-around
space-between

DISTRIBUTING MULTIPLE FLEX ITEMS
“Big deal,” you might be saying: we can do left/right alignment with floats and centering with auto-margins. True. Flexbox doesn’t show its real strength until we have more than one item in a container. The justify-content property also lets you distribute items equally inside a container.

GROUPING FLEX ITEMS
Flex containers only know how to position elements that are one level deep (i.e., their child elements). They don’t care one bit about what’s inside their flex items. This means that grouping flex items is another weapon(вепен) in your layout-creation arsenal. Wrapping a bunch of items in an extra results in a totally different web page.

CROSS-AXIS (VERTICAL) ALIGNMENT
So far, we’ve been manipulating horizontal alignment, but flex containers can also define the vertical alignment of their items. This is something that’s simply not possible with floats.

THE AVAILABLE OPTIONS FOR ALIGN-ITEMS IS SIMILAR TO JUSTIFY-CONTENT:
center
flex-start (top)
flex-end (bottom)
stretch
baseline


WRAPPING FLEX ITEMS
Flexbox is a more powerful alternative to float-based grids. Not only can it render items as a grid—it can change their alignment, direction, order, and size, too. To create a grid, we need the flex-wrap property.

Adding the following (flex-wrap:wrap) property forces items that don’t fit to get bumped down to the next row.


FLEX CONTAINER DIRECTION
“Direction” refers to whether a container renders its items horizontally(хоризОнтали) or vertically(вЕртикали).So far, all the containers we’ve seen use the default horizontal direction, which means items are drawn one after another in the same row before popping down to the next column when they run out of space.
One of the most amazing things about flexbox is its ability to transform rows into columns using only a single line of CSS.



FLEX CONTAINER ORDER
Up until now, there’s been a tight(тайт) correlation between the order of our HTML elements and the way boxes are rendered in a web page.
The flex-direction property also offers you control over the order in which items appear(опИя) via the row-reverse and column-reverse properties.

FLEX ITEM ORDER
Adding an order property to a flex item defines its order in the container without(визАутс) affecting surrounding(суравдинг) items. Its default value is 0, and increasing(инкрИсен) or decreasing it from there moves the item to the right or left, respectively.

FLEX ITEM ALIGNMENT
We can do the same thing with vertical alignment.

This is where the (align-self) property comes in. You can align elements in other ways using the same values as the align-items property, listed below for convenience(конвИниансе).

center
flex-start (top)
flex-end (bottom)
stretch
baseline

Sozonik Oleg, [08.12.18 11:31]
FLEXIBLE ITEMS
Flex items are flexible: they can shrink and stretch to match the width of their containers. The flex property defines the width of individual items in a flex container.


The flex property defines the width of individual items in a flex container. Or, more accurately, it allows them to have flexible widths. It works as a weight that tells the flex container how to distribute extra space to each item.


STATIC ITEM WIDTHS
We can even mix-and-match flexible boxes with fixed-width ones. flex: initial falls back to the item’s explicit width property. This lets us combine static and flexible boxes in complex ways.


FLEX ITEMS AND AUTO-MARGINS
Auto-margins in flexbox are special. They can be used as an alternative to an extra div when trying to align a group of items to the left/right of a container. Think of auto-margins as a “divider” for flex items in the same container.



Flexbox gave us a ton of amazing new tools for laying out a web page.
          Compare these techniques to what we were able to do with floats, and it should be pretty clear that flexbox is a cleaner option for laying out modern websites:

SUMMARY
Use display: flex; to create a flex container.
Use justify-content to define the horizontal alignment of items.
Use align-items to define the vertical alignment of items.
Use flex-direction if you need columns instead of rows.
Use the row-reverse or column-reverse values to flip item order.
Use order to customize the order of individual elements.
Use align-self to vertically align individual items.
Use flex to create flexible boxes that can stretch and shrink.


The flexbox layout mode should be used for most of your web pages, but there are some things it’s not-so-good at, like gently tweaking element positions and preventing them from interacting with the rest of the page.
