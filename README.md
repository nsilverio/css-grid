# Solutions for [css-grid](https://cssgrid.io/) by [Wes Bos](https://github.com/wesbos/)

## Live examples

3.  [CSS Grid Fundamentals](#css-grid-fundamentals)
4.  [Grid Auto-flow](#grid-auto-flow)
5.  [Sizing tracks in CSS Grid](#Sizing-Tracks-in-CSS-Grid)
6.  [CSS Grid repeat function](#CSS-Grid-repeat-function)
7.  [Sizing Grid Items](#Sizing-Grid-Items)
8.  [Placing Grid Items](#Placing-Grid-Items-)
9.  [auto-fit and auto-fill](https://jsfiddle.net/d1pLngzx/)
10. [Using minmax() for Responsive Grids](https://jsfiddle.net/xthszm2j/)
11. Grid Template Areas:
    - [Area Line Names](https://jsfiddle.net/tkyxomht/)
    - [Areas](https://jsfiddle.net/p0sn7L7v/)
12. [Naming Lines in CSS Grid](https://jsfiddle.net/ygpmn0xh/)
13. [grid-auto-flow dense Block Fitting](https://jsfiddle.net/sxj83p70/)
14. [CSS Grid Alignment + Centering](https://jsfiddle.net/eyL9a2gv/)
15. [Re-ordering Grid Items](https://jsfiddle.net/uscf9mk0/)
16. [Nesting Grid with Album Layouts](https://jsfiddle.net/yn7jak0y/)
17. [CSS Grid Image Gallery](https://jsfiddle.net/cbjzped2/)
18. Flexbox vs CSS Grid:
    - [Axis Flipping](https://jsfiddle.net/pt8hym9s/)
    - [Controls on Right](https://jsfiddle.net/4o7gavuj/)
    - [Flex on Item](https://jsfiddle.net/1u264ftd/)
    - [Perfectly Centered](https://jsfiddle.net/sgbrtrjo/)
    - [Self Control](https://jsfiddle.net/c6gg8pkn/)
    - [Stacked Layout](https://jsfiddle.net/mnfm1sw0/)
    - [Unknown Content Size](https://jsfiddle.net/4ze02bkj/)
    - [Unknown Number of Items](https://jsfiddle.net/Lg7r3jmy/)
    - [Variable Widths on Each Row](https://jsfiddle.net/qymhootd/)
19. [Recreating Codepen](https://jsfiddle.net/br6n54qt/)
20. [Bootstrappy Grid with CSS Variables](https://jsfiddle.net/gLLht2hd/)
21. [Responsive Website](https://jsfiddle.net/bh16ofp8/)
22. [Full Bleed Blog Layout](https://jsfiddle.net/j8w6v3mh/)

# CSS Grid Fundamentals

Defines:

- Gap between grid elements `display: grid;`
- Columns width `grid-template-columns: 200px 400px;` (first column to 200px, second column to 400px)
- Rows height `grid-template-rows: 50px 100px;` (first column to 50px, second column to 100px)
- Remaing rows default height `grid-auto-rows: 250px 500px;`

```
.container {
        display: grid;
        grid-gap: 20px;
        grid-template-columns: 200px 400px;
        grid-template-rows: 50px 100px;
        grid-auto-rows: 250px 500px;
      }
```

# Grid Auto-flow

Determines if new elemens will be added as rows (default behaviour) or as columuns

- Define thw two first columns `grid-template-columns: 200px 400px;` (first column to 200px, second column to 400px)
- Add new elements as columns `grid-auto-flow: column;`
- Define auto flow columns size `grid-auto-columns: 250px`

```
<div class="container">
      <div class="item">1</div>
      <div class="item">2</div>
      <div class="item">auto-flow</div>
      <div class="item">auto-flow</div>
</div>

<style>
.container {
        display: grid;
        grid-gap: 20px;
        grid-template-columns: 200px 400px;
        grid-template-rows: 50px 100px;
        grid-auto-rows: 250px 500px;
      }
</style>
```

# Sizing Tracks in CSS Grid

Fractional unit (fr) represents the amount of space left after all the elemens are laid out, including its margins, paddings and borders.

- `grid-template-columns: 200px 2fr 1fr 2fr;` will divide the remaning space of `<div= class="container">` after adding a 200px column into 3 other columns, the first one will use 2 fractional units, the second 1 fractional unit and the last 2 fractional units.

```
.container {
  display: grid;
  grid-gap: 20px;
  border: 10px solid var(--yellow);
  grid-template-columns: 200px 2fr 1fr 2fr;
}
```

![fractional-units](https://github.com/nsilverio/css-grid/blob/master/assets/images/fractional-unit.png)

- For `grid-template-rows` the default height of an element is just however hight the element is and default width of an element is as wide as the actual view port.

```
.container {
  display: grid;
  grid-gap: 20px;
  border: 10px solid var(--yellow);
  grid-template-columns: 200px 2fr 1fr 2fr;
}
```

![fractional-units2](https://github.com/nsilverio/css-grid/blob/master/assets/images/fractional-unit2.png)

- `auto` keyword automatcly sizes the column / row to the the wider / highest grid element.

```

    .container {
      display: grid;
      height: 400px;
      grid-gap: 20px;
      border: 10px solid var(--yellow);
      grid-template-columns: 200px 1fr 1fr auto;
    }

```

![fractional-units2](https://github.com/nsilverio/css-grid/blob/master/assets/images/auto-keyword.png)

# CSS Grid repeat function

- `repeat` function cuts down the amout of line codes

```
.container {
        display: grid;
        grid-gap: 20px;
        grid-template-columns: repeat(2, 150px) 2fr repeat(2,100px);
      }
```

![fractional-units2](https://github.com/nsilverio/css-grid/blob/master/assets/images/repeat-function.png)

# Sizing Grid Items

- Grid items by default naturally flows one after another and fit themselves as into the grid as they can.
- `grid-column: span 2` and `grid-row: span 2` changes the natural flow of the column/row.

![fractional-units2](https://github.com/nsilverio/css-grid/blob/master/assets/images/grid-span.png)

# Placing Grid Items

- Grid items position and size can be changed either using the abreviation `grid-column` / `grid-row` setting where the item should start, end and its size

```
/* Make item 20 start at row 4 and go for 3 */
  .item20 {
    grid-row: 4 / span 3;
  }
```
