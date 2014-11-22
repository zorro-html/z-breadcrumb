# breadcrumb

面包屑

## 特性/属性

### `path`

展示的字符串数组

### `autoupdate`

标识面包屑是否在导航项目被点击时自动更新，默认是 false

## 事件

### `nav-to`

点击导航项目时触发相应的 `nav-to` 事件

## Example

```
<jie-breadcrumb path="['foo', 'bar', 'baz', 'qux']"></jie-breadcrumb>

<jie-breadcrumb autoupdate></jie-breadcrumb>

<script>
  var breadcrumb1 = document.querySelectorAll('jie-breadcrumb')[0];
  var breadcrumb2 = document.querySelectorAll('jie-breadcrumb')[1];

  breadcrumb1.addEventListener('nav-to', function (e) {
    this.path = e.detail.path;
  });
  breadcrumb2.path = ['foo', 'bar', 'baz', 'qux'];
  breadcrumb2.addEventListener('nav-to', function (e) {
    console.log(e.type, e.detail.path);
  });
</script>
```
