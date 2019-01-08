# jquery-simple-checkbox-table

Super simple checkbox table, which is provided as jQuery plugin.

![simple_checkbox_table_screenshot](https://user-images.githubusercontent.com/1883527/50759761-405b2980-12a9-11e9-9a60-9125748d2a00.gif)

Check out the [DEMO](https://toshiyukihina.github.io/jquery-simple-checkbox-table/).

# API

## Methods

### `.simpleCheckboxTable()`

Initialize the simple checkbox table.

```
$("table").simpleCheckboxTable();
```

## Events

You can pass the event handler on initialization.

### `function onCheckedStateChanged($checkbox)`

Triggered when the checked state is changed.

```
$("table").simpleCheckboxTable({
  onCheckedStateChanged: function($checkbox) {
    // Do something when checkbox state is changed.
  }
});
```

# Usage

Include `jQuery` and `jquery.simple-checkbox-table.js` in your HTML code.

```
<html>
  <head>
    <title>...</title>
    <script src="https://code.jquery.com/jquery-3.3.1.min.js" integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8=" crossorigin="anonymous"></script>
    <script src="dist/jquery.simple-checkbox-table.js"></script>
  </head>
  <body>
    ...
  </body>
</html>
```

Write your HTML table. 

**The checkboxes in the table must be placed on the furthest left.** This is the only one rule you should follow.

```
<table id="demo">
  <thead>
    <tr>
      <th><input type="checkbox"></th>
      <th>Name</th>
      <th>e-mail</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><input type="checkbox"></td>
      <td>hoge</td>
      <td>hoge@hoge.com</td>
    </tr>
    <tr>
      <td><input type="checkbox"></td>
      <td>foo</td>
      <td>foo@foo.com</td>
    </tr>
    <tr>
      <td><input type="checkbox"></td>
      <td>bar</td>
      <td>bar@bar.com</td>
    </tr>
  </tbody>
</table>
```

Initialize the table with `.simpleCheckboxTable()` in Javascript.

```
$(document).ready(function(){
  $("table#demo").simpleCheckboxTable();
});
```

Done!
