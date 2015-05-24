# `<z-breadcrumb>`

Breadcrumb element which could help user nav from the current path

## Import

```
<link rel="import" href="z-breadcrumb/z-breadcrumb.html">
```

## Attributes / Properties

- `path`: key list of the current path
- `autoupdate`: whether auto update the `path` when click items, `false` as default

## Events

- `nav-to`: fired when user click the breadcrumb items

## Examples

```
<z-breadcrumb id="z-breadcrumb-test" path="['foo', 'bar', 'baz', 'qux']"></z-breadcrumb>

<z-breadcrumb id="z-breadcrumb-test-autoupdate" autoupdate></z-breadcrumb>

<script>
  var breadcrumb1 = document.querySelector('html /deep/ #z-breadcrumb-test');
  var breadcrumb2 = document.querySelector('html /deep/ #z-breadcrumb-test-autoupdate');

  breadcrumb1.addEventListener('nav-to', function (e) {
    this.path = e.detail.path;
  });
  breadcrumb2.path = ['foo', 'bar', 'baz', 'qux'];
  breadcrumb2.addEventListener('nav-to', function (e) {
    console.log(e.type, e.detail.path);
  });
</script>
```
