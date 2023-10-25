---
title: The Table Tag in HTML
---

# The Table Tag in HTML:

The `<table>` tag is one of the most important components for structuring and displaying data in HTML.
This article will examine the `<table>` tag, its attributes, and its use in building structured data layouts for websites.

### Basic Structure of a Table

In HTML, a table is made up of various components, such as:

1. `<table>`: The container element that contains the whole table is this one.

2. `<tr>`: Stands for "table row". It is used to define a row within the table.

3. `<th> `and `<td>`: These are used to create headers and data cells, respectively, inside a `<tr>`. A table data cell is represented by `<td>`, and a table header is denoted by `<th>`.

4. Optional elements `<thead>`, `<tbody>`, and `<tfoot>` can be utilized to organize a table's header, body, and footer content,respectively.

## Let us break things down for you.

### `<table>` Tag

The `<table>` tag is a fundamental HTML element used to create tables, which allow for the organization of data into rows and columns. Tables are commonly used to present information in a structured and visually appealing manner. They are particularly useful for displaying data like schedules, pricing lists, product details, and much more.

```html
<table>
  <!-- All the table elements should be inside this table tag --->
</table>
```

## Table Rows,Table Headers and Table Data `<tr>`,`<th>` &`<td>`

### Table Rows

Each table row starts with a`<tr>` and ends with a `</tr>` tag.

```html
<table>
  <tr>
    <!--to make a 1st row   -->
    <td>data 1</td>
    <td>data 2</td>
  </tr>
  <tr>
    <!--to make a 2st row   -->
    <td>1</td>
    <td>2</td>
  </tr>
</table>
```

### NOTE!!

Remember to include the CSS border property in the table; otherwise, the table will lack a border.

Scroll down to learn about border style.

`<caption>` The tag is used to give the table a heading/name.

![table ](https://www.edupointbd.com/wp-content/uploads/2017/11/table-parts.png)

Every new row requires the addition of a `<tr>` tag.

### Table Headers

There are situations when you want your cells to be table header cells.
Use the `<th>` tag rather than the `<td>` tag in those circumstances:

```html
<table>
  <tr>
    <th>Header 1</th>
    <!---text in this cells will be bold and centered--->
    <th>Header 2</th>
  </tr>
  <tr>
    <td>Data 1</td>
    <!-- this cells will ne standard-->
    <td>Data 2</td>
  </tr>
</table>
```

By default styling `<th>` is typically bold and centered, indicating a header cell, while `<td>` is a standard data cell.

### Table Data / Table cell

Each table cell is defined by a `<td>` and a `</td>` tag.
Everything between `<td>` and `</td>` are the content of the table cell.

A table cell can contain all sorts of HTML elements: text, images, lists, links, other tables, etc.

#### Let's make a Table with Rows and Columns

To create a row, you use the `<tr>` tag, and within each row, you can add headers or data cells using `<th>` and `<td>` tags, respectively. Here's an example:

```html
<table>
  <tr>
    <!-----row 1---->
    <th>Name</th>
    <!--header tag------->
    <th>Image</th>
    <th>Link</th>
  </tr>
  <tr>
    <td>Mohan</td>
    <!----text----->
    <td><img scr="mohanimg.png" alt="image of mohan" /></td>
    <!----Image----->
    <td><a>mohan-profile-page</a></td>
    <!----link----->
  </tr>
</table>
```

## `<thead>`, `<tbody>`, and `<tfoot>`

`<thead>`, `<tbody>`, and `<tfoot>` are crucial elements in HTML tables that help structure content more semantically. They allow you to group specific parts of the table together, making it easier for browsers and assistive technologies to understand and process the information.

Here's a quick rundown of each:

### `<thead>`:

Stands for "table head". This element is used to group the header content in a table. It usually contains column names or labels. Anything you put here appears at the top of the table.

```html
<table>
  <thead>
    <tr>
      <th>heading 1</th>
      <th>hearding 2</th>
      <th>heading 3</th>
    </tr>
  </thead>
  <!-- More sections -->
</table>
```

It typically contains one or more `<tr>` elements that define the header row(s) of the table.

### `<tbody>`:

Stands for "table body". This element is used to group the main content of the table. It contains one or more `<tr>` elements that define the data rows of the table.

```html
<table>
  <!-- ... -->
  <tbody>
    <tr>
      <td>data1</td>
      <td>data2</td>
      <td>data3</td>
    </tr>
    <tr>
      <td>data1.1</td>
      <td>data1.2</td>
      <td>data1.3</td>
    </tr>
    <!-- More sections -->
  </tbody>
</table>
```

### `<tfoot>`:

Stands for "table foot". This element is used to group the footer content in a table.
Rarely used but important for semantic reasons, the table footer often contains summary rows or notes.

```html
<table>
  <!-- this  -->
  <tfoot>
    <tr>
      <td colspan="2">Total People</td>
      <td>1</td>
    </tr>
  </tfoot>
</table>
```

It typically contains one or more `<tr>`elements that define the footer row(s) of the table.

Using these elements not only enhances the semantic structure of the table but also provides benefits for accessibility and styling through CSS. It's a best practice to include them, especially in tables with complex content.

## `<colspan>` and `<rowpan>`

You must have seen a `colspan` attribute right in the above `<tfoot>` example.
In an HTML table allows you to merge adjacent cells to create more complex layouts. This is achieved using the `rowspan` and `colspan` attributes.

`rowspan`: This attribute allows a cell to span multiple rows.

`colspan`: This attribute allows a cell to span multiple columns.

![table ](https://cwh-full-next-space.fra1.digitaloceanspaces.com/tutorial/html-tables/colspan-rowspan.png)

Here's an example to illustrate how to use `rowspan` and `colspan`

```html
<table>
  <tr>
    <th>Header</th>
    <th>Header</th>
    <th>Header</th>
  </tr>
  <tr>
    <td rowspan="2">Spanned Data</td>
    <!---allows a cell to span multiple rows.---->
    <td>Data 2</td>
    <td>Data 3</td>
  </tr>

  <tr>
    <td>Data 4</td>
    <td>Data 6</td>
  </tr>

  <tr>
    <td colspan="3">Spanned Column</td>
    <!---allows a cell to span multiple colspan .---->
  </tr>
</table>
```

![table ](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSO50gKvsnLMrn7IPZGtsT6rv-a0o8EbWUIZg&usqp=CAU)

### In this example:

1. The first row contains 4 headers .
2. The second row contains three data cells: Data 1, Data 2, and a cell with `rowspan`="2" which will span the next row.
3. The third row contains Data 3 and Data 4.
4. The fourth row contains a single cell with `colspan`="3" which will span all three columns.

This creates a table with a complex layout, demonstrating the use of `rowspan` and `colspan` attributes.

Remember, `rowspan` and `colspan` should be used thoughtfully, as they affect the overall structure and accessibility of the table. It's important to ensure that the merged cells logically represent the content they contain.

## `<colgroup>` and `<col>`

`<colgroup>` and `<col>` are elements in HTML that allow you to apply styles and properties to entire columns in a table.

They provide a way to group and apply common attributes to multiple columns without having to apply those attributes individually to each `<td>` or `<th>` element.

### `<colgroup>` Tag

The `<colgroup>` element is used to group a set of columns in a table. It is typically placed within the `<table>` element, before any `<thead>`, `<tbody>`, or `<tfoot>` elements.

The `<colgroup>` element contains one or more `<col>`elements, which specify the properties for the grouped columns.

```html
<table>
  <colgroup>
    <col style="background-color: lightblue;" />
    <col style="background-color: lightgreen;" />
    <col style="background-color: lightcoral;" />
  </colgroup>
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
    <th>Header 3</th>
  </tr>
  <tr>
    <td>Data 1</td>
    <td>Data 2</td>
    <td>Data 3</td>
  </tr>
</table>
```

In this example, the `<colgroup>` element is used to group three columns, and each `<col>` element within it sets a background color for the corresponding column.

### `<col>`

The `<col>` element is used within a `<colgroup>` to define the properties for a specific column. It can have various attributes like span, width, align, and others.

```html
<table>
  <colgroup>
    <col span="2" style="background-color: lightblue;" />
    <col span="1" style="background-color: lightgreen;" />
  </colgroup>
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
    <th>Header 3</th>
  </tr>
  <tr>
    <td>Data 1</td>
    <td>Data 2</td>
    <td>Data 3</td>
  </tr>
</table>
```

![colgroup](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT7h59U59jIwz6ArsJZAfhI0Td-RhBYccHp_Q&usqp=CAU)

In this example, we use the span attribute to specify that the first two <col> elements apply to two columns each, and the third <col> element applies to one column.

## Why Use `<colgroup>` and `<col>`?

Using `<colgroup>` and `<col>` allows you to apply styles and attributes to columns efficiently.

This can be especially useful for setting widths, background colors, or other visual properties.

It also enhances the accessibility and semantics of the table.

# Table Borders

HTML tables can have borders of different styles and shapes.

### To add a border

To add a border, use the CSS border property on table, th, and td elements:

```css
table,
th,
td {
  border: 1px solid black;
}
```

![table brder](https://www.jquery-az.com/wp-content/uploads/2015/12/1.1-HTML-simple-table.png)

### Collapsed Table Borders

Border-collapse property to collapse.This will make the borders collapse into a single border:

```CSS
table, th, td {
 border: 1px solid black;
 border-collapse: collapse;
}
```

![table brder collapse](https://media.geeksforgeeks.org/wp-content/uploads/border-collapse1.png)

you can also make different border lines by using `border-style ` andf `color` property

#### EG:-

![border-styling-and-color](https://www.datisnetwork.com/wp-content/uploads/2021/02/bordeer.png)

### Round Table Borders

With the border-radius property, the borders get rounded corners:

```css
table,
th,
td {
  border: 1px solid black;
  border-radius: 10px;
}
/* or */
th,
td {
  /* to show the borders of the th and td */
  border: 1px solid black;
  border-radius: 10px;
}
```

![table brder round ](https://i.stack.imgur.com/oCSS2.png)

# Table Sizes

To have different sizes for each column, row or the entire table.

Use the style attribute with the width or height properties to specify the size of a table, row or column.

```html
<table style="width:50%">
  <!----width of the table s 100%----->
  <tr>
    <th style="width:50%">Firstname</th>
    <!------this makes this column with upto 50% --->
    <th>Age</th>
    <th>country</th>
  </tr>
  <tr>
    <td>rohit</td>
    <td>50</td>
    <td>India</td>
  </tr>
  <tr>
    <td>siji</td>
    <td>94</td>
    <td>India</td>
  </tr>
</table>
```

![table sizing](https://www.programiz.com/sites/tutorial2program/files/html-table.png)

The HTML `<table>` element is a significant tool for organising and presenting data on web pages. Web developers may produce aesthetically attractive and structured material for consumers by employing rows, columns, headers, and data cells. Understanding how to use the `<table>` tag and its accompanying parts successfully is a critical skill for anybody trying to create informative and user-friendly websites.
