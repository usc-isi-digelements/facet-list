# facet-list

A Polymer Element that performs an ajax query or elasticsearch aggregation query and displays the list of results which can then be used as term filters.

### Example that runs elasticsearch queries
```html
<facet-list
  name="city"
  title="Cities"
  text-property="id"
  client="[[esclient]]"
  index-name="mockads"
  index-types='["ad"]'
  process-request="[[processRequest]]"
  search-parameters-property="city"
  search-parameters="{{searchParameters}}"
  result-function="[[resultFunction]]"
  agg-field="city"
  query-builder-config="[[queryBuilderConfig]]">
</facet-list>
```

### Example that runs ajax queries
```html
<facet-list
  name="city"
  title="Cities"
  text-property="id"
  query-url="[[queryUrl]]"
  process-request="[[processRequest]]"
  result-function="[[resultFunction]]"
  search-function="[[searchFunction]]"
  search-parameters-property="city"
  search-parameters="{{searchParameters}}">
</facet-list>
```

### Styling

`<facet-list>` provides the following custom properties and mixins for styling:

Custom property                             | Description                                                         | Default
--------------------------------------------|---------------------------------------------------------------------|--------
`--facet-list-bar-color`                    | The color of the single or left bars.                               | --paper-grey-300
`--facet-list-bar-count-color`              | The color of the single or left count labels.                       | --paper-grey-900
`--facet-list-bar-height`                   | The height of the single or left bars.                              | 20px
`--facet-list-bar-title-color`              | The color of the single or left title labels.                       | --paper-grey-900
`--facet-list-bar-title-hover-color`        | The color of the single or left title labels on hover (if a link).  | --paper-indigo-900
`--facet-list-max-height`                   | The max height of the bar chart.                                    | none
`--facet-list-second-bar-color`             | The color of the right (second) bars.                               | --paper-grey-300
`--facet-list-second-bar-count-color`       | The color of the right (second) count labels.                       | --paper-grey-900
`--facet-list-second-bar-height`            | The height of the right (second) bars.                              | 20px
`--facet-list-second-bar-title-color`       | The color of the right (second) title labels.                       | --paper-grey-900
`--facet-list-second-bar-title-hover-color` | The color of the right (second) title labels on hover (if a link).  | --paper-indigo-900

### Dependencies

Dependencies are installed using [Bower](http://bower.io/):

    npm install -g bower
    bower install

### Testing

Tests are run using [web-component-tester](https://github.com/Polymer/web-component-tester):

    npm install -g web-component-tester
    wct

### Demonstration & Documentation

Demonstration and documentation are viewed using [polyserve](https://github.com/PolymerLabs/polyserve):

    npm install -g polyserve
    polyserve

The demo will require a local instance of elasticsearch with the `mockads` index created by running `data/import_test_data.sh`.
