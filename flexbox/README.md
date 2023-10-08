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

## Tasks

### 0. Add display flex

Use the starter HTML and CSS files from this task to task 7. Copy the contents of the starter files into the files that you need to produce and make the necessary changes according to the task description.

When using display: flex; on a container, all direct children become flex-items (and no more inline or block elements).

With display flex, margins are not collapsing as they would with block items. Also remember that flexbox is 1-dimensional system (vs CSS Grid which is a 2 dimensional system)

In the /\* Grid section within your CSS

- Add a selector for the row class - Property: display, Value: flex
  => Now, all children from the row class are flex items
- Entirely remove the row::after declaration
- Remove the float: left inside [class*='col-']
  => All elements should appear same than before using the float

### 1. Add new classes on sections

Using the files from the previous task as the base for this task:

In the outermost section tag for services

- Add the class section-services
  In the outermost section tag for works

- Add the class section-works
  In the outermost section tag for about

- Add the class section-about-us
  In the outermost section tag for latest_news

- Add the class section-latest-news
  In the outermost section tag for testimonial

- Add the class section-testimonial
  In the outermost section tag for contact

- Add the class section-contact

2. Reverse order Latest news cards

Using the files from the previous task for this task:

The flex-direction property says how flex items are placed on the main axis and their direction (normal or reversed).

flex-direction is sometimes used when doing responsive design. Some elements may appear better when they are in column mode on mobile and row when on desktop.

row-reverse and column-reverse should be used in specific situation. The visual order of elements should be the same visually and in the HTML code. Refer to flex-direction - CSS: Cascading Style Sheets | MDN for more information

In your CSS file:

Before /**_ 4. CARD _**/, add a new comment: /_ Section Latest news ============================= _/

Under that comment section, target the row class inside section-latest-news class

- Property: flex-direction, Value: row-reverse
  The Latest news should appear in a reverse order.

### 3. Simplify services list

Using the files from the previous task for this task:

flex-wrap is a property that can force the flex items to be in one or multiple lines. Learn more about it here.

In the Services section of 3-index.html, remove the second ul and put the 3 lielements under the first ul

Now, in your CSS file, before /**_ 4. CARD _**/, add a new comment: /_ Section SERVICES ============================= _/

Under that comment section, add a new selector targeting the row class inside the section-services class

- Property: flex-wrap, Value: wrap

### 4. Playing around with the spacing between flex service items

mandatory
Score: 100.0% (Checks completed: 100.0%)
Using the files from the previous task for this task:

In 4-styles.css file, within the Grid section

- In .col-1-3 selector
  - Replace the current width with calc((100% / 3) - 2rem)
- In .col-1-2 selector

  - Replace the current width with calc((100% / 2) - 2rem)

- In [class*='col-']

      - Remove the padding declaration
      - Set Property: margin to 1rem

  In ul.row declaration

- Replace the current margin with -1rem

### 5. Flexify the header

Using the files from the previous task for this task:

In your 5-index.html file, inside the Header section

- Wrap the div with class header-logo and the div with class navbar-menu with a div that has header-container as a class
  In your 5-styles.css file,
- Inside the /\* Header section
- Add a selector for the header-container class
  - Property: display, Value: flex
  - Property: justify-content, Value: space-between
- Remove header-logo and header-logo a rules
- Remove the navbar-menu rule

- In the variables section
  - Remove
    - header-logo-position
    - header-logo-link-display
    - header-logo-link-position
    - header-logo-link-top
    - header-logo-link-left

### 6. Flexify the navbar

Using the files from the previous task for this task:

in 6-styles.css, inside the /\* Navbarsection

- In the nav class selector
  - Property: display, Value: flex
- Inside the .nav .nav-item selector, remove the display declaration
- Target .nav-item + .nav-item inside nav class
  - Move the margin declaration from .nav .nav-item inside the new selector.
- In the variables section
  - Change the value of the variable nav-item-margin to be 0 0 0 2rem

### 7. Align center logo and navbar

Using the files from the previous task for this task:

In 7-styles.css, inside the /\* Header section, in the header-container class selector, set the property align-items to center
