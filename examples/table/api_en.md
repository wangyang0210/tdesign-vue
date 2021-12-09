### BaseTable Props

| name              | type                      | default | description                                                                                                                                                                                                    | required |
| ----------------- | ------------------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| bordered          | Boolean                   | false   | show table bordered                                                                                                                                                                                            | N        |
| columns           | Array                     | []      | table column configs。Typescript：`Array<BaseTableCol<T>>`                                                                                                                                                     | N        |
| data              | Array                     | []      | table data。Typescript：`Array<T>`                                                                                                                                                                             | N        |
| empty             | String / Slot / Function  | ''      | empty text or empty element。Typescript：`string | TNode`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                                                    | N        |
| expandedRow       | String / Slot / Function  | -       | table expanded row, to show more detail information。Typescript：`string | TNode<{ row: T; index: number }>`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts) | N        |
| height            | String / Number           | 'auto'  | table height                                                                                                                                                                                                   | N        |
| hover             | Boolean                   | false   | show hover style                                                                                                                                                                                               | N        |
| loading           | Boolean / Slot / Function | false   | loading state table。Typescript：`boolean | TNode`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                                                           | N        |
| maxHeight         | String / Number           | -       | table max height                                                                                                                                                                                               | N        |
| pagination        | Object                    | -       | you can use all props of pagination component with paginationProps。Typescript：`PaginationProps`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)        | N        |
| rowClassName      | String / Function         | -       | table `th` classname。Typescript：`ClassName | ((params: { row: T; rowIndex: number }) => ClassName)`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)        | N        |
| rowKey            | String                    | -       | required。unique key for each row data                                                                                                                                                                         | Y        |
| rowspanAndColspan | Function                  | -       | rowspan and colspan。Typescript：`(params: RowspanAndColspanParams<T>) => RowspanColspan`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)                | N        |
| size              | String                    | medium  | table size。options：small/medium/large。Typescript：`SizeEnum`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                                              | N        |
| stripe            | Boolean                   | false   | show stripe style                                                                                                                                                                                              | N        |
| tableLayout       | String                    | fixed   | table-layout css properties。options：auto/fixed                                                                                                                                                               | N        |
| verticalAlign     | String                    | middle  | vertical align。options：top/middle/bottom                                                                                                                                                                     | N        |
| onPageChange      | Function                  |         | trigger on pagination changing。`(pageInfo: PageInfo, newDataSource: Array<T>) => {}`                                                                                                                          | N        |
| onRowClick        | Function                  |         | trigger on row click。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)。`(context: RowEventContext<T>) => {}`                                              | N        |
| onRowDbClick      | Function                  |         | trigger on double click。`(context: RowEventContext<T>) => {}`                                                                                                                                                 | N        |
| onRowHover        | Function                  |         | trigger on row hover。`(context: RowEventContext<T>) => {}`                                                                                                                                                    | N        |
| onRowMousedown    | Function                  |         | trigger on row mousedown。`(context: RowEventContext<T>) => {}`                                                                                                                                                | N        |
| onRowMouseup      | Function                  |         | trigger on row mouseup。`(context: RowEventContext<T>) => {}`                                                                                                                                                  | N        |
| onScrollX         | Function                  |         | trigger on scroll horizontal。`(params: { e: WheelEvent }) => {}`                                                                                                                                              | N        |
| onScrollY         | Function                  |         | trigger on scroll vertical。`(params: { e: WheelEvent }) => {}`                                                                                                                                                | N        |

### BaseTable Events

| name          | params                                          | description                                                                                                                |
| ------------- | ----------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| page-change   | `(pageInfo: PageInfo, newDataSource: Array<T>)` | trigger on pagination changing                                                                                             |
| row-click     | `(context: RowEventContext<T>)`                 | trigger on row click。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts) |
| row-db-click  | `(context: RowEventContext<T>)`                 | trigger on double click                                                                                                    |
| row-hover     | `(context: RowEventContext<T>)`                 | trigger on row hover                                                                                                       |
| row-mousedown | `(context: RowEventContext<T>)`                 | trigger on row mousedown                                                                                                   |
| row-mouseup   | `(context: RowEventContext<T>)`                 | trigger on row mouseup                                                                                                     |
| scroll-x      | `(params: { e: WheelEvent })`                   | trigger on scroll horizontal                                                                                               |
| scroll-y      | `(params: { e: WheelEvent })`                   | trigger on scroll vertical                                                                                                 |

### BaseTableCol

| name      | type                               | default | description                                                                                                                                                                                                                                                                                                                                                                  | required |
| --------- | ---------------------------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| align     | String                             | left    | align type。options：left/right/center                                                                                                                                                                                                                                                                                                                                       | N        |
| attrs     | Object                             | -       | html attributes                                                                                                                                                                                                                                                                                                                                                              | N        |
| cell      | String / Function                  | -       | use cell to render table cell。Typescript：`string | TNode<{ row: T; rowIndex: number; col: BaseTableCol; colIndex: number }>`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                                                                                                                                             | N        |
| children  | Array                              | -       | grouping table head。Typescript：`Array<BaseTableCol<T>>`                                                                                                                                                                                                                                                                                                                    | N        |
| className | String / Object / Array / Function | -       | cell classnames。Typescript：`ClassName | ((context: CellData<T>) => ClassName)`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/base-table/type.ts)                                                                                | N        |
| colKey    | String                             | -       | unique key for column                                                                                                                                                                                                                                                                                                                                                        | N        |
| ellipsis  | Boolean                            | false   | ellipsis cell content                                                                                                                                                                                                                                                                                                                                                        | N        |
| fixed     | String                             | left    | fixed current column to left or right。options：left/right                                                                                                                                                                                                                                                                                                                   | N        |
| minWidth  | String / Number                    | -       | column min width                                                                                                                                                                                                                                                                                                                                                             | N        |
| render    | Function                           | -       | render function can be used to render cell or head。Typescript：`TNode<{ type: RenderType; row: T; rowIndex: number; col: BaseTableCol<T>; colIndex: number }>`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/base-table/type.ts) | N        |
| title     | String / Function                  | -       | th content。Typescript：`string | TNode<{ col: BaseTableCol; colIndex: number }>`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                                                                                                                                                                                          | N        |
| width     | String / Number                    | -       | column width                                                                                                                                                                                                                                                                                                                                                                 | N        |

### PrimaryTable Props

| name                                   | type                      | default | description                                                                                                                                                                                                             | required |
| -------------------------------------- | ------------------------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| asyncLoading                           | String / Slot / Function  | -       | async loading state。Typescript：`string | TNode`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                                                                     | N        |
| columns                                | Array                     | []      | table column configs。Typescript：`Array<PrimaryTableCol<T>>`                                                                                                                                                           | N        |
| expandedRow                            | String / Slot / Function  | -       | table expanded row, to show more detail information。Typescript：`TNode<{ row: T; index: number }>`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                   | N        |
| expandedRowKeys                        | Array                     | []      | expanded row keys, row key value is from data[rowKey]。support syntax sugar。Typescript：`Array<string | number>`                                                                                                       | N        |
| defaultExpandedRowKeys                 | Array                     | []      | expanded row keys, row key value is from data[rowKey]。uncontrolled properties。Typescript：`Array<string | number>`                                                                                                    | N        |
| expandOnRowClick                       | Boolean                   | -       | expand row on click                                                                                                                                                                                                     | N        |
| filterIcon                             | Slot / Function           | -       | filter icon。Typescript：`TNode`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                                                                                      | N        |
| filterValue                            | Object                    | -       | filter value。support syntax sugar。Typescript：`FilterValue`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)                                                     | N        |
| defaultFilterValue                     | Object                    | -       | filter value。uncontrolled properties。Typescript：`FilterValue`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)                                                  | N        |
| multipleSort                           | Boolean                   | false   | support multiple column fields sort                                                                                                                                                                                     | N        |
| selectedRowKeys                        | Array                     | -       | selected row keys, row key is from data[rowKey]。support syntax sugar。Typescript：`Array<string | number>`                                                                                                             | N        |
| defaultSelectedRowKeys                 | Array                     | -       | selected row keys, row key is from data[rowKey]。uncontrolled properties。Typescript：`Array<string | number>`                                                                                                          | N        |
| showExpandArrow                        | Boolean / Slot / Function | true    | to show expand icon. expand icon is set in first column。Typescript：`boolean | TNode`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                                | N        |
| sort                                   | Object / Array            | -       | sort configs。support syntax sugar。Typescript：`TableSort`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)                                                       | N        |
| defaultSort                            | Object / Array            | -       | sort configs。uncontrolled properties。Typescript：`TableSort`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)                                                    | N        |
| `Omit<TdBaseTableProps<T>, 'columns'>` | -                         | -       | -                                                                                                                                                                                                                       | N        |
| onChange                               | Function                  |         | [see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)。`(data: TableChangeData, context: TableChangeContext<Array<T>>) => {}`                                            | N        |
| onExpandChange                         | Function                  |         | trigger on expand row keys changing。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)。`(expandedRowKeys: Array<string | number>, options: ExpandOptions<T>) => {}` | N        |
| onFilterChange                         | Function                  |         | trigger on filter value changing。`(filterValue: FilterValue, context: { col: PrimaryTableCol<T> }) => {}`                                                                                                              | N        |
| onSelectChange                         | Function                  |         | trigger on select changing。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)。`(selectedRowKeys: Array<string | number>, options: SelectOptions<T>) => {}`          | N        |
| onSortChange                           | Function                  |         | trigger on sort changing。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)。`(sort: SortInfo | Array<SortInfo>, options: SortOptions<T>) => {}`                     | N        |

### PrimaryTable Events

| name          | params                                                                 | description                                                                                                                               |
| ------------- | ---------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| change        | `(data: TableChangeData, context: TableChangeContext<Array<T>>)`       | [see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)                                      |
| expand-change | `(expandedRowKeys: Array<string | number>, options: ExpandOptions<T>)` | trigger on expand row keys changing。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts) |
| filter-change | `(filterValue: FilterValue, context: { col: PrimaryTableCol<T> })`     | trigger on filter value changing                                                                                                          |
| select-change | `(selectedRowKeys: Array<string | number>, options: SelectOptions<T>)` | trigger on select changing。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)          |
| sort-change   | `(sort: SortInfo | Array<SortInfo>, options: SortOptions<T>)`          | trigger on sort changing。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/table/type.ts)            |

### PrimaryTableCol

| name         | type               | default | description                                                                                                                                                                                                                                               | required |
| ------------ | ------------------ | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| cell         | String / Function  | -       | to render table cell。Typescript：`string | TNode<{ row: T; rowIndex: number; col: PrimaryTableCol; colIndex: number }>`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                                | N        |
| checkProps   | Object             | -       | checkbox or radio component properties。Typescript：`CheckProps<T>`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/primary-table/type.ts)                                                                         | N        |
| disabled     | Function           | -       | disable table select action。Typescript：`(options: {row: T; rowIndex: number }) => boolean`                                                                                                                                                              | N        |
| filter       | Object             | -       | filter rules config。Typescript：`Filter`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/primary-table/type.ts) | N        |
| render       | Function           | -       | to render cell or head。Typescript：`TNode<{ type: 'cell' | 'title'; row: T; rowIndex: number; col: PrimaryTableCol<T>; colIndex: number }>`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)            | N        |
| sorter       | Boolean / Function | false   | sort configs。Typescript：`boolean | SorterFun<T>`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/primary-table/type.ts)                                                                                          | N        |
| sortType     | String             | all     | sort options。options：desc/asc/all。Typescript：`SortType`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/tree/develop/src/primary-table/type.ts)                                                                                 | N        |
| title        | String / Function  | -       | to render table head。Typescript：`string | TNode<{ col: PrimaryTableCol; colIndex: number }>`。[see more ts definition](https://github.com/TDesignOteam/tdesign-vue/blob/develop/src/common.ts)                                                          | N        |
| type         | String             | single  | row select type。options：single/multiple                                                                                                                                                                                                                 | N        |
| BaseTableCol | -                  | -       | -                                                                                                                                                                                                                                                         | N        |