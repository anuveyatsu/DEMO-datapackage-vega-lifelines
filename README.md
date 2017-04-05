This is an example DataPackage that demonstrates usage of "Vega Graph Specifications". This Demo Data Package implements an example from [here](https://vega.github.io/vega-editor/?mode=vega&spec=lifelines).

## Views

To create graphs for your tabular DataPackage, the datapackage.json should include the views attribute that defines data views.

### Vega Graph Specifications

<script src="https://gist.github.com/anuveyatsu/a327e3fb6312e3200ed04e6a9bd1f78e.js"></script>
To use "Vega Graph Specification" `specType` inside `views` attribute should be set to `vega` - line 62. In this example we implement multiple resources per one view. You can use almost the same specifications inside `spec` attribute, that are used for setting the vega graphs. Only difference is that in `data` property, all `url` and `path` attributes are moved out. Instead of that, `source` attribute is used to reference a dataset - lines 69 and 73.

Outside of `spec` attribute there are some other important parameters to note:

<table class="table table-bordered table-striped resource-summary">
  <thead>
   <tr>
     <th>Attribute</th>
     <th>Type</th>
     <th>Description</th>
   </tr>
  </thead>
  <tbody>
    <tr>
      <th>name</th>
      <td>String</td>
      <td>Unique identifier for view within list of views (lines 51 and 62)</td>
    </tr>
    <tr>
      <th>title</th>
      <td>String</td>
      <td>Title for the graph (lines 52 and 63)</td>
    </tr>
    <tr>
      <th>resources</th>
      <td>Array</td>
      <td>Data sources for this spec. It can be either resource name or index. By default it is the first resource (lines 53 and 64)</td>
    </tr>
    <tr>
      <th>specType</th>
      <td>String</td>
      <td>Available options: simple, vega, plotly <strong>(Required)</strong></td>
    </tr>
  </tbody>
</table>
