# Solutions for [css-grid](https://cssgrid.io/) by [Wes Bos](https://github.com/wesbos/)

## Live examples

2.  [Starter Files and original repo](https://github.com/wesbos/css-grid)
3.  [CSS Grid Fundamentals](#css-grid-fundamentals) - [[jsfiddle]](https://jsfiddle.net/natalisilverio/eftmx28n/)
4.  [CSS Grid Dev Tools](https://jsfiddle.net/b55x8vh2/)
5.  [CSS Grid Implicit vs Explicit Tracks](https://jsfiddle.net/mon8xdgb/)
6.  [CSS grid-auto-flow Explained](https://jsfiddle.net/Loq4uj16/)
7.  [Sizing tracks in CSS Grid](https://jsfiddle.net/q8h3r8yb/)
8.  [CSS Grid repeat function](https://jsfiddle.net/8f8xyx86/)
9.  [Sizing Grid Items](https://jsfiddle.net/wqs6tcuk/)
10. [Placing Grid Items](https://jsfiddle.net/hs5xhvpp/)
11. [Spanning and Placing Cardio](https://jsfiddle.net/2z7z6o9k/)
12. [auto-fit and auto-fill](https://jsfiddle.net/d1pLngzx/)
13. [Using minmax() for Responsive Grids](https://jsfiddle.net/xthszm2j/)
14. Grid Template Areas:
    - [Area Line Names](https://jsfiddle.net/tkyxomht/)
    - [Areas](https://jsfiddle.net/p0sn7L7v/)
15. [Naming Lines in CSS Grid](https://jsfiddle.net/ygpmn0xh/)
16. [grid-auto-flow dense Block Fitting](https://jsfiddle.net/sxj83p70/)
17. [CSS Grid Alignment + Centering](https://jsfiddle.net/eyL9a2gv/)
18. [Re-ordering Grid Items](https://jsfiddle.net/uscf9mk0/)
19. [Nesting Grid with Album Layouts](https://jsfiddle.net/yn7jak0y/)
20. [CSS Grid Image Gallery](https://jsfiddle.net/cbjzped2/)
21. Flexbox vs CSS Grid:
    - [Axis Flipping](https://jsfiddle.net/pt8hym9s/)
    - [Controls on Right](https://jsfiddle.net/4o7gavuj/)
    - [Flex on Item](https://jsfiddle.net/1u264ftd/)
    - [Perfectly Centered](https://jsfiddle.net/sgbrtrjo/)
    - [Self Control](https://jsfiddle.net/c6gg8pkn/)
    - [Stacked Layout](https://jsfiddle.net/mnfm1sw0/)
    - [Unknown Content Size](https://jsfiddle.net/4ze02bkj/)
    - [Unknown Number of Items](https://jsfiddle.net/Lg7r3jmy/)
    - [Variable Widths on Each Row](https://jsfiddle.net/qymhootd/)
22. [Recreating Codepen](https://jsfiddle.net/br6n54qt/)
23. [Bootstrappy Grid with CSS Variables](https://jsfiddle.net/gLLht2hd/)
24. [Responsive Website](https://jsfiddle.net/bh16ofp8/)
25. [Full Bleed Blog Layout](https://jsfiddle.net/j8w6v3mh/)

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
