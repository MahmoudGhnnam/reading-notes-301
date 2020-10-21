# Regex 

A RegEx, or Regular Expression, is a sequence of characters that forms a search pattern.

RegEx can be used to check if a string contains the specified search pattern.

One of the most interesting features is that once you’ve learned the syntax, you can actually use this tool in (almost) all programming languages ​​(JavaScript, Java, VB, C #, C / C++, Python, Perl, Ruby, Delphi, R, Tcl, and many others) with the slightest distinctions about the support of the most advanced features and syntax versions supported by the engines).

## Regex tutorial

## some examples and explanations

Basic topics

- Anchors — ^ and $

* ^The        matches any string that starts with The 
* end$        matches a string that ends with end
* ^The end$   exact string match (starts and ends with The end)
* roar        matches any string that has the text roar in it

- Quantifiers — * + ? and {}

* abc*        matches a string that has ab followed by zero or more c
* abc+        matches a string that has ab followed by one or more c
* abc?        matches a string that has ab followed by zero or one c
* abc{2}      matches a string that has ab followed by 2 c

- OR operator — | or []

* a(b|c)     matches a string that has a followed by b or c (and captures b or c) -> Try it!
* a```[bc]```      same as previous, but without capturing b or c

- Character classes — \d \w \s and .

* \d         matches a single character that is a digit
* \w         matches a word character (alphanumeric character plus underscore) -> Try it!
* \s         matches a whitespace character (includes tabs and line breaks)
* .          matches any character -> Try it!

# CSS Grid Reference


CSS Grid Layout is the most powerful layout system available in CSS. It is a 2-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system. You work with Grid Layout by applying CSS rules both to a parent element (which becomes the Grid Container) and to that element’s children (which become Grid Items).

## Properties for the Parent (Grid Container)

* display

Defines the element as a grid container and establishes a new grid formatting context for its contents.

Values:

grid – generates a block-level grid
inline-grid – generates an inline-level grid

--------------------------------------

* grid-template-columns grid-template-rows

Defines the columns and rows of the grid with a space-separated list of values. The values represent the track size, and the space between them represents the grid line.

Values:

```<track-size>``` – can be a length, a percentage, or a fraction of the free space in the grid (using the fr unit)

```<line-name>``` – an arbitrary name of your choosing

----------------------------------------

* grid-template-areas

Defines a grid template by referencing the names of the grid areas which are specified with the grid-area property. Repeating the name of a grid area causes the content to span those cells. A period signifies an empty cell. The syntax itself provides a visualization of the structure of the grid.

Values:

```<grid-area-name>``` – the name of a grid area specified with grid-area

. – a period signifies an empty grid cell
none – no grid areas are defined

-----------------------------------------

* grid-template

A shorthand for setting grid-template-rows, grid-template-columns, and grid-template-areas in a single declaration.

Values:

none – sets all three properties to their initial values

```<grid-template-rows> / <grid-template-columns>``` – sets grid-template-columns and grid-template-rows to the specified values, respectively, and sets grid-template-areas to none

------------------------------------------

## Properties for the Children (Grid Items)

* grid-column-start grid-column-end grid-row-start grid-row-end

Determines a grid item’s location within the grid by referring to specific grid lines. grid-column-start/grid-row-start is the line where the item begins, and grid-column-end/grid-row-end is the line where the item ends.

Values:

```<line>``` – can be a number to refer to a numbered grid line, or a name to refer to a named grid line

span ```<number>``` – the item will span across the provided number of grid tracks

span ```<name>``` – the item will span across until it hits the next line with the provided name

auto – indicates auto-placement, an automatic span, or a default span of one

-------------------------------------------

* grid-column grid-row

Shorthand for grid-column-start + grid-column-end, and grid-row-start + grid-row-end, respectively.

Values:

```<start-line> / <end-line>``` – each one accepts all the same values as the longhand version, including span

--------------------------------------------

* grid-area

Gives an item a name so that it can be referenced by a template created with the grid-template-areas property. Alternatively, this property can be used as an even shorter shorthand for grid-row-start + grid-column-start + grid-row-end + grid-column-end.

Values:

```<name>``` – a name of your choosing

```<row-start> / <column-start> / <row-end> / <column-end>`` – can be numbers or named lines

--------------------------------------------

* justify-self

Aligns a grid item inside a cell along the inline (row) axis (as opposed to align-self which aligns along the block (column) axis). This value applies to a grid item inside a single cell.

Values:

* start – aligns the grid item to be flush with the start edge of the cell

* end – aligns the grid item to be flush with the end edge of the cell

* center – aligns the grid item in the center of the cell

* stretch – fills the whole width of the cell (this is the default)