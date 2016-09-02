## Vizceral

From [`src/vizceral.jsx`](src/vizceral.jsx)

![](https://raw.githubusercontent.com/Netflix/vizceral/master/logo.png)

This is a react wrapper around [Vizceral](https://github.com/Netflix/vizceral).

## Setup
1. Install package
   `npm install vizceral-react --save`
2. import vizceral-react to start using

   ```js
   import Vizceral from 'vizceral-react';
   <Vizceral traffic={this.state.trafficData}
             view={this.state.currentView}
             showLabels={this.state.displayOptions.showLabels}
             filters={this.state.filters}
             graphsUpdated={this.graphsUpdated}
             viewChanged={this.viewChanged}
             objectHighlighted={this.objectHighlighted}
             rendered={this.rendered}
             nodeFocused={this.nodeFocused}
             nodeContextSizeChanged={this.nodeContextSizeChanged}
             matchesFound={this.matchesFound}
             match={this.state.searchTerm}
             modes={this.state.modes}
             definitions={this.state.definitions}
             styles={styles}
   />
   ```

## Props

#### connectionHighlighted

```js
// Default: () => {}
connectionHighlighted: Function
```

Callback for when a connection is highlighted. The highlighted connection is the only parameter.

#### definitions

```js
// Default: {}
definitions: Object
```

Object map of definitions. Refer to [github.com/Netflix/vizceral/DATAFORMATS.md#definitions](https://github.com/Netflix/vizceral/blob/master/DATAFORMATS.md#definitions)

#### filters

```js
// Default: []
filters: Array
```

Array of filter definitions and current values to filter out nodes and connections. Refer to
[github.com/Netflix/vizceral/DATAFORMATS.md#filters](https://github.com/Netflix/vizceral/blob/master/DATAFORMATS.md#filters)

#### graphsUpdated

```js
// Default: () => {}
graphsUpdated: Function
```

Callback for when the graph objects are modified

#### match

```js
// Default: ''
match: String
```

A search string to highlight nodes that match

#### matchesFound

```js
// Default: () => {}
matchesFound: Function
```

Callback when nodes match the match string. The matches object { total, visible } is the only property.

#### modes

```js
modes: Object
```

Map of modes to mode type, e.g. { detailedNode: 'volume' }

#### nodeContextSizeChanged

```js
// Default: () => {}
nodeContextSizeChanged: Function
```

Callback for when the top level node context panel size changes. The updated dimensions is the only parameter.

#### nodeFocused

```js
// Default: () => {}
nodeFocused: Function
```

Callback for when a node is focused. The focused node is the only parameter.

#### nodeHighlighted

```js
// Default: () => {}
nodeHighlighted: Function
```

Callback for when an object is highlighted. The highlighted object is the only parameter.
`object.type` will be either 'node' or 'connection'

#### nodeUpdated

```js
// Default: () => {}
nodeUpdated: 
```

#### rendered

```js
// Default: () => {}
rendered: Function
```

Callback when a graph has been rendered. The name of the graph that was rendered is the only property.

#### showLabels

```js
// Default: true
showLabels: Boolean
```

Whether or not to show labels on the nodes.

#### styles

```js
// Default: {}
styles: Object
```

Styles to override default properties.

#### traffic

```js
// Default: {}
traffic: Object
```

The traffic data. See [github.com/Netflix/vizceral/DATAFORMATS.md](https://github.com/Netflix/vizceral/blob/master/DATAFORMATS.md) for specification.

#### view

```js
// Default: []
view: 
```

#### viewChanged

```js
// Default: () => {}
viewChanged: Function
```

Callback for when the view changed. The view array is the only property.

<br><br>
