&lt;sortable-table&gt;
================

Polymer Web Component that generates a sortable &lt;table&gt; from JSON.

There are many capable Javascript grids, this one aims to:
- leverage browser's native `template` support,
- be declaratively configurable through DOM (requiring no Javascript to use),
- be as simple to use, and
- have all the features of those other grids.

## Built-In Table Features

- Click column headers to sort
- Drag-and-Drop columns to reorder
- Edit rows with Undo
- Row paging, checkbox selection, and multi-select
- Use of HTML5 `template` for customization (Cells, Column Headers and Footers)
- 2-way data binding with the outside world

## Live Examples

> [Data Formats](http://files.stevenskelton.ca/sortable-table/examples/data-formats.html)

> [DOM Elements](http://files.stevenskelton.ca/sortable-table/examples/dom-elements.html)

> [Themes](http://files.stevenskelton.ca/sortable-table/examples/themes.html)

> [Auto-Generated Columns](http://files.stevenskelton.ca/sortable-table/examples/autogenerated-columns.html)

> [Row Templates](http://files.stevenskelton.ca/sortable-table/examples/row-templates.html)

> [Row Editor with Undo Functionality](http://files.stevenskelton.ca/sortable-table/examples/row-editor.html)

> [Selected Rows, Multi-Select](http://files.stevenskelton.ca/sortable-table/examples/selected-rows.html)

> [Dynamically Changing Columns and Templates](http://files.stevenskelton.ca/sortable-table/examples/dynamic-columns.html)

> [Paging, Top-N Rows](http://files.stevenskelton.ca/sortable-table/examples/paging.html)

## Usage

1. Add the library using the Javascript package manager [Bower](http://bower.io/):

	```bower install --save sortable-table```

2. Import Web Components' polyfill:

	```html
	<script src="bower_components/platform/platform.js"></script>
	```

3. Import Custom Element:

	```html
	<link rel="import" href="bower_components/sortable-table/sortable-table.html">
	```

4. Start using it!

	Start simple and use DOM to configure the grid:

	```html
	<sortable-table>
		<sortable-column>fruit</sortable-column>
		<sortable-column>alice</sortable-column>
		<sortable-column>bill</sortable-column>
		<sortable-column>casey</sortable-column>
		<!-- data case be either an Array, JSON, or JSON5 -->
		[
			[ "apple", 4, 10, 2 ],
			[ "banana", 0, 4, 0 ],
			[ "grape", 2, 3, 5 ],
			[ "pear", 4, 2, 8 ],
			[ "strawberry", 0, 14, 0 ]
		]
	</sortable-table>
	```

	Or use Javascript attributes:

	```html
	<sortable-table columns='["fruit","alice","bill","casey"]' data='[
			[ "apple", 4, 10, 2 ],
			[ "banana", 0, 4, 0 ],
			[ "grape", 2, 3, 5 ],
			[ "pear", 4, 2, 8 ],
			[ "strawberry", 0, 14, 0 ] ]'>
	</sortable-table>
	```

	Or take advanced control with custom templates and 2-way data binding:

	```html
	<sortable-table data="{{data}}" columns="{{columns}}">
		<!-- add templates here -->
	</sortable-table>
	```

All configuration options are [documented on the wiki](https://github.com/stevenrskelton/sortable-table/wiki/Configuration).

## History

For detailed changelog, check [Releases](https://github.com/stevenrskelton/sortable-table/releases).

## License
[MIT License](http://opensource.org/licenses/MIT) © Steven Skelton
