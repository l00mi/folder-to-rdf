# folder-to-rdf

Create an [RDF-ext](https://rdf-ext/rdf-ext) compatible graph of a folder. This library looks at a `folder` and tries to parse the Linked Data files and then returns what is in the folder in a RDF-graph

Like `ls`, with `Linked Data output`

## Install

```
$ npm install --save linkeddata-ls
```

## Usage

### Simple

```javascript
var opts = {
  suffixMeta: '.meta',
  suffixAcl: '.acl',
  skipFiles: ['secret*', '.git', '*.pem']
}
var ls = require('folder-to-rdf')(opts)

ls('./', function(err, graph) {
  console.log(graph.toString())
})

```

## Test

```
npm test
```

## License

MIT &copy; Nicola Greco 2015