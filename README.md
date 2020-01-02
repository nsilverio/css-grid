# Solutions for [css-grid](https://cssgrid.io/) by [Wes Bos](https://github.com/wesbos/)

## Live examples

3.  [CSS Grid Fundamentals](#css-grid-fundamentals) - [[jsfiddle]](https://
4.  [Grid Auto-flow](#grid-auto-flow)
5.  [Sizing tracks in CSS Grid](https://jsfiddle.net/q8h3r8yb/)
6.  [CSS Grid repeat function](https://jsfiddle.net/8f8xyx86/)
7.  [Sizing Grid Items](https://jsfiddle.net/wqs6tcuk/)
8.  [Placing Grid Items](https://jsfiddle.net/hs5xhvpp/)
9.  [Spanning and Placing Cardio](https://jsfiddle.net/2z7z6o9k/)
10. [auto-fit and auto-fill](https://jsfiddle.net/d1pLngzx/)
11. [Using minmax() for Responsive Grids](https://jsfiddle.net/xthszm2j/)
12. Grid Template Areas:
    - [Area Line Names](https://jsfiddle.net/tkyxomht/)
    - [Areas](https://jsfiddle.net/p0sn7L7v/)
13. [Naming Lines in CSS Grid](https://jsfiddle.net/ygpmn0xh/)
14. [grid-auto-flow dense Block Fitting](https://jsfiddle.net/sxj83p70/)
15. [CSS Grid Alignment + Centering](https://jsfiddle.net/eyL9a2gv/)
16. [Re-ordering Grid Items](https://jsfiddle.net/uscf9mk0/)
17. [Nesting Grid with Album Layouts](https://jsfiddle.net/yn7jak0y/)
18. [CSS Grid Image Gallery](https://jsfiddle.net/cbjzped2/)
19. Flexbox vs CSS Grid:
    - [Axis Flipping](https://jsfiddle.net/pt8hym9s/)
    - [Controls on Right](https://jsfiddle.net/4o7gavuj/)
    - [Flex on Item](https://jsfiddle.net/1u264ftd/)
    - [Perfectly Centered](https://jsfiddle.net/sgbrtrjo/)
    - [Self Control](https://jsfiddle.net/c6gg8pkn/)
    - [Stacked Layout](https://jsfiddle.net/mnfm1sw0/)
    - [Unknown Content Size](https://jsfiddle.net/4ze02bkj/)
    - [Unknown Number of Items](https://jsfiddle.net/Lg7r3jmy/)
    - [Variable Widths on Each Row](https://jsfiddle.net/qymhootd/)
20. [Recreating Codepen](https://jsfiddle.net/br6n54qt/)
21. [Bootstrappy Grid with CSS Variables](https://jsfiddle.net/gLLht2hd/)
22. [Responsive Website](https://jsfiddle.net/bh16ofp8/)
23. [Full Bleed Blog Layout](https://jsfiddle.net/j8w6v3mh/)

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

.container {
        display: grid;
        grid-gap: 20px;
        grid-template-columns: 200px 400px;
        grid-template-rows: 50px 100px;
        grid-auto-rows: 250px 500px;
      }
```
