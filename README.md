This Demo Data Package implements an example from [here](https://vega.github.io/vega-editor/?mode=vega&spec=lifelines).

In the views spec, we use "Vega Graph Spec" - must be specified in `specType` attribute as `vega` (as in line 63 of code snippet below). In this example we implement multiple resources per one view.
Only difference when using Vega spec is `data` attribute that is removed from the spec (see starting from line 64). Everything else is identical:

<script src="https://gist.github.com/anuveyatsu/a327e3fb6312e3200ed04e6a9bd1f78e.js"></script>

Outside of `spec` attribute there are some other important parameters to note:

* `name` (line 60) - unique identifier for view within list of views.

* `title` (line 61) - title for this graph.

* `resources` (line 62) - data sources for this spec. It can be either resource name or index. In our example we use resource's index.

* `specType` (line 63) - used for defining syntax. In this demo datapackage we use `vega` (Vega Graph Spec).
