# facet-list

A Polymer Element that performs an elasticsearch aggregation query and displays the list of results, which can then be used as term filters.

### Example
```html
    <facet-list
      name="city"
      title="Cities"
      text-property="id"
      client="[[esclient]]"
      index="mockads"
      process-request="{{processRequest}}"
      search-param-subset="{{searchParameters.city}}"
      search-parameters="{{searchParameters}}"
      index-types='["ad"]'
      combine-function="[[combineFunction]]"
      agg-field="city"
      query-builder-config="{{queryBuilderConfig}}">
    </facet-list>
```

### Styling

`<facet-list>` provides the following custom properties and mixins for styling:

Custom property         | Description                 | Default
------------------------|-----------------------------|------------------
`--facet-background-color`  | Color for bars in facet-list | #B0BEC5
`--primary-text-color`    | Color for text in bars         | #212121

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
