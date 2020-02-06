[![Build Status](https://travis-ci.org/graphology/graphology-operators.svg)](https://travis-ci.org/graphology/graphology-operators)

# Graphology Operators

Miscellaneous operators to be used with [`graphology`](https://graphology.github.io).

## Installation

```
npm install graphology-operators
```

## Usage

*Unary*

* [reverse](#reverse)

*Binary*

* [union](#union)

*Cast*

* [toSimple](#tosimple)

### reverse

Reverse the given graph's directed edges.

```js
import {reverse} from 'graphology-operators';
// Alternatively, to load only the relevant code:
import reverse from 'graphology-operators/reverse';

const reversedGraph = reverse(graph);
```

*Arguments*

* **graph** *Graph*: target graph.

### union

Returns the union of the given graphs. Nodes & edges present in both graph will have their attributes merges with precedence given to the second graph.

```js
import {union} from 'graphology-operators';
// Alternatively, to load only the relevant code:
import union from 'graphology-operators/union';

const R = union(G, H);
```

*Arguments*

* **G** *Graph*: first graph.
* **H** *Graph*: second graph.

### toSimple

Returns the simple version of the given multigraph where we only keep a single edge of each type between nodes.

If a simple graph is passed, the function will only return a copy of it.

```js
import {toSimple} from 'graphology-operators';
// Alternatively, to load only the relevant code:
import toSimple from 'graphology-operators/to-simple';

const simpleGraph = toSimple(multiGraph);
```
