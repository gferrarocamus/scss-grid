# SCSS Grid & Typography Library

## Introduction
Based on [a prior project](https://github.com/gferrarocamus/grid-based-framework), this minimal SCSS library was built to provide a basic 12-column layout, essential typography styles, and some commonly-used utilities in CSS.

I drew inspiration from [Bootstrap](https://getbootstrap.com/), although I was not trying to recreate it. My aim was *not* to provide an exhaustive collection of styles and components, but rather to create a lean, customizable resource to be used as a foundation to build upon.

## Description

### Grid

<ul>
    <li>The grid uses a hierarchy of <code>.container</code>, <code>.row</code>s, and <code>.col-</code>s.</li>
    <li><code>.container</code>s come with 15px padding on each side and a maximum width of 1140px.</li>
    <li>There's a <code>.container-fluid</code> option that covers 100% of the width, minus the 15px paddings.</li>
    <li>Rows use flexbox and have 20px gutters between them.</li>
    <li>Column classes are named <code>.col-</code> followed by the number of slots it should span in the grid, from 1 to 12.</li>
    <li>Four breakpoints are included as Sass variables:
    <ul>
        <li><code>$xs: 575.98px;</code></li>
        <li><code>$sm: 767.98px;</code></li>
        <li><code>$md: 991.98px;</code></li>
        <li><code>$lg: 1199.98px;</code></li>
    </ul>
    To make columns expand to 100% width, there are corresponding utility classes: <code>.expand-col-xs</code>, <code>.expand-col-sm</code>, <code>.expand-col-md</code> and <code>.expand-col-lg</code>. Note that columns will expand in the given screen size <i>or smaller</i>.</li>
    <li>Columns can also be made responsive with ad hoc media queries changing the <code>flex</code> and <code>max-width</code> properties as desired. For example:
<pre><code>@media (max-width: 1199.98px) {
    .expand-1199 {
        flex: 0 0 100%;
        max-width: 100%;
    }
}</code></pre>
    This would make the targeted column(s) expand to 100% width for devices with a max-width of 1199.98px.</li>
</ul>

### Typography

<ul>
    <li>Two common font stacks are used, sans-serif for headings and buttons, and serif for most other text elements.</li>
    <li>For a consistent <a href="https://drewish.com/tools/vertical-rhythm/">vertical rhythm</a>, increasing font sizes, line-heights and margins have been applied to headings. I've used <code>em</code> units in relation to a <code>body</code> font-size of 16px.
    <li>I also created the following classes because I find myself using these in nearly every project: <code>.bold</code>, <code>.uppercase</code>, and <code>.decoration-none</code>.</li>
</ul>

### Other Utilities

<ul>
    <li>Box-sizing is applied by default.</li>
    <li>Different display classes are available for the main display property values, for example: <code>.d-none</code> and <code>.d-flex</code>.</li>
    <li>There are <code>.float-left</code> and <code>.float-right</code> classes, as well as a <code>.clearfix</code> class that can be applied to containers of floated elements, to clear both floats.</li>
    <li>For text-alignment, there's <code>.left</code>, <code>.right</code>, and <code>.center</code>.</li>
    <li>I've used <a href="https://gist.github.com/terkel/4373420">these SCSS functions</a> to handle decimals, which are now part of this library as a partial.</li>
    <li>I've included <a href="https://meyerweb.com/eric/tools/css/reset/">Eric Meyer's reset</a> as a starting point.</li>
</ul>

### Instructions

To use this library, you can link the [styles.css stylesheet](https://github.com/gferrarocamus/scss-grid/blob/master/library/styles.css) directly in your HTML. A [compressed version](https://github.com/gferrarocamus/scss-grid/blob/master/library/css-compressed/styles.css) of the stylesheet is also available.

## Sample

You can see a live demo of the grid and typography styles that come with this library [here](https://gferrarocamus.github.io/scss-grid/sample-page.html).

## License

MIT © 2020 [Giuliana Ferraro](https://www.giulianaferraro.com/) <[giuliana.ferraro.dev@gmail.com](mailto:giuliana.ferraro.dev@gmail.com)>
