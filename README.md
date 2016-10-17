# paginate

__Simple and minnimal component for adding pagination links.__


## Demo & Examples

You can see the working example here - [prakash23.github.io/react-simple-paginate](http://prakash23.github.io/react-simple-paginate/)

To build the examples locally, run:

```
npm install
npm start
```

Then open [`localhost:8000`](http://localhost:8000) in a browser.


## Installation

The easiest way to use react-simple-paginate is to install it from NPM and include it in your own React build process (using [Browserify](http://browserify.org), [Webpack](http://webpack.github.io/), etc).

You can also use the standalone build by including `dist/react-simple-paginate.js` in your page. If you use this, make sure you have already included React, and it is available as a global variable.

```
npm install react-simple-paginate --save
```


## Usage

The component generates links based on the total number of results, typical usage is like -

```
var Paginate = require('react-simple-paginate');

	<Paginate
      total="100"
      containerClassName="pages-list"
      currentPageClassName = "active-page"
      pageClassName = "page-link"
      handler={this.handler}
	/>
```
Following are the props supported -

| Prop                 | Description                                                                                  		    |
| ---------------------|:----------------------------------------------------------------------------------------------------------:|
| total                | Total number of elements (number of page links generated are based on this value)            		    |
| offset      	       | offset for currently shown elements, (current page is based on this value)                   		    |
| limit 	       | number of results shown in a page                      				      		    |
| handler              | callback when any page link is clicked, the offset for that page is passed as a param to the callback      |
| prevLabel            | Label for previous Link      								      		    |
| nextLabel            | Label for next Link      								      		    |
| containerClassName   | css class for the component root      							       		    |
| pageClassName        | css class for the individual page links (also added to previous and next links.)      	      		    |
| currentPageClassName | css class for the current page link      						      		    |
| centerPagesCount     | Number of page links shown after the left marker       						    |
| cornerPagesCount     | Number of first and last pages shown.       						                    |
| leftMarker           | Label for indicating there are more pages on the left.       						    |
| rightMarker          | Label for indicating there are more pages on the right.       					    |



## Development (`src`, `lib` and the build process)

**NOTE:** The source code for the component is in `src`. A transpiled CommonJS version (generated with Babel) is available in `lib` for use with node.js, browserify and webpack. A UMD bundle is also built to `dist`, which can be included without the need for any build system.

To build, watch and serve the examples (which will also watch the component source), run `npm start`. If you just want to watch changes to `src` and rebuild `lib`, run `npm run watch` (this is useful if you are working with `npm link`).

## License

__PUT LICENSE HERE__

Copyright (c) 2016 Prakash.
