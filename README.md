jquery-resizable-columns
=======================

Resizable table columns for jQuery. **[Live Demo](http://dobtco.github.io/jquery-resizable-columns)**

#### Simple Usage

```
<script src="libs/jquery.js"></script>
<script src="libs/jquery-ui.js"></script>
<script src="jquery.resizableColumns.js"></script>

<table>
  <thead>
    <tr>
      <th>#</th>
      <th>First Name</th>
      <th>Last Name</th>
      <th>Username</th>
    </tr>
  </thead>
  <tbody>
    ...
  </tbody>
</table>

<script>
  $(function(){
    $("table").resizableColumns();
  });
</script>
```

#### Persist column sizes

To save column sizes on page reload (or js re-rendering), just pass a function that responds to `get` and `set`. You'll also have to give your &lt;table&gt; a `data-resizable-columns-id` attribute, and your &lt;th&gt;s `data-resizable-column-id` attributes.

```
<script src="libs/jquery.js"></script>
<script src="libs/jquery-ui.js"></script>
<script src="libs/store.js"></script>
<script src="jquery.resizableColumns.js"></script>

<table data-resizable-columns-id="demo-table">
  <thead>
    <tr>
      <th data-resizable-column-id="#">#</th>
      <th data-resizable-column-id="first_name">First Name</th>
      <th data-resizable-column-id="last_name">Last Name</th>
      <th data-resizable-column-id="username">Username</th>
    </tr>
  </thead>
  <tbody>
    ...
  </tbody>
</table>

<script>
  $(function(){
    $("table").resizableColumns({
      store: store
    });
  });
</script>
```