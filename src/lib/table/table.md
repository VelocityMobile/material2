The `md-table` provides a Material Design styled data-table that can be used to display rows of
data.

This table builds on the foundation of the CDK data-table and uses a similar interface for its
data source input and template, except that its element selectors will be prefixed with `md-`
instead of `cdk-`.
 
<!-- example(table-basic) -->

Note that the column definition directives (`cdkColumnDef` and `cdkHeaderCellDef`) are still
prefixed with `cdk-`.

For more information on the interface and how it works, see the
[guide covering the CDK data-table](https://material.angular.io/guides/cdk-table).

### Features

The `<md-table>` itself only deals with the rendering of a table structure (rows and cells).
Additional features can be built on top of the table by adding behavior inside cell templates
(e.g., sort headers) or next to the table (e.g. a paginator). Interactions that affect the
rendered data (such as sorting and pagination) should be propagated through the table's data source.


#### Pagination

The `<md-paginator>` adds a pagination UI that can be used in conjunction with the `<md-table>`. The
paginator emits events that can be used to trigger an update via the table's data source.

<!-- example(table-pagination) -->

#### Sorting
Use the `mdSort` directive and `<md-sort-header>` adds a sorting UI the table's column headers. The
sort headers emit events that can be used to trigger an update via the table's data source.

<!-- example(table-sorting) -->

#### Filtering

While Angular Material does not offer a specific component for filtering tabular data, the table's 
data source can be updated based on any custom filter UI. Any filtering pattern need only trigger
an update via the table's data source.


<!--- example(table-filtering) -->

### Simple Table

In the near future, we will provide a simplified version of the data-table with an easy-to-use
interface, material styling, array input, and more out-of-the-box features (sorting, pagination,
and selection).
