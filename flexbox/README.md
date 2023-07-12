## Flexbox

# Learning Objectives
- What is Flexbox?
    # Flexbox is a layout system optimized for building user interfaces. Use this interactive reference tool to recall flexbox properties and experiment with layouts.
- How to convert float positioning to a flex display
- How to horizontally and vertically align elements using Flexbox
- The difference between the main and cross axes
- Properties that work on flex elements vs flex container
- Shorthands for flex
- How to create a new page with flex in mind

## container
# display
<p>Enables flex for all children.</p>

- display: flex;
- display: inline-flex;

# flex-direction
<p>Establishes the main axis.</p>

- flex-direction: row;
- flex-direction: row-reverse;
- flex-direction: column;
- flex-direction: column-reverse;

# flex-wrap
<p>Wraps items if they can't all be made to fit on one line.</p>

- flex-wrap: nowrap;
- flex-wrap: wrap;
- flex-wrap: wrap-reverse;

# justify-content

<p>Attempts to distribute extra space on the main axis.</p>
 
- justify-content: flex-start;
- justify-content: flex-end;
- justify-content: center;
- justify-content: space-between;
- justify-content: space-around;
- justify-content: space-evenly;

# align-items
<p>Determines how items are laid out on the cross axis.</p>

- align-items: flex-start;
- align-items: flex-end;
- align-items: center;
- align-items: baseline;
- align-items: stretch;

# align-content
<p>Only has an effect with more than one line of content. Examples shown here use flex-wrap.</p>

- align-content: flex-start;
- align-content: flex-end;
- align-content: center;
- align-content: space-between;
- align-content: space-around;
- align-content: stretch;

## children

# order
<p>Allows you to explictly set the order you want each child to appear in</p>

- order: 1;

# flex-grow
<p>Defines what amount of available space inside a flexible container the item should take up.</p>
<p>Allows you to determine how each child is allowed to grow as a part of a whole</p>

- flex-grow: 1; (applied to all )
- flex-grow (1, 2, and 3)

# flex-basis
<p>Defines the size of an element before remaining space is distributed.</p>

- flex-basis: 50%;
- flex-basis: 20% 40%; (First item 20% and second item 40%)


# flex-shrink
<p>Allows an item to shrink if necessary. Only really useful with a set size or flex-basis.</p>

- flex-shrink: 1; both want to be 100% wide, 2nd item has flex-shrink: 2
 
# align-self
<p>Sets alignment for individual item. See "align-items" for options</p>

- align-self: flex-start|flex-end|center|baseline|stretch; (3rd item has align-self:flex-end)
