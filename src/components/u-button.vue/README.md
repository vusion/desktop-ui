# UButton 按钮

## 示例
### 基本形式

``` html
<u-button>设 置</u-button>
```

### 禁用

``` html
<u-button disabled>设 置</u-button>
```

### 颜色扩展

``` html
<u-linear-layout>
    <u-button color="primary">立即创建</u-button>
    <u-button color="success">立即创建</u-button>
    <u-button color="warning">立即创建</u-button>
    <u-button color="error">立即创建</u-button>
    <u-button color="primary" disabled>立即创建</u-button>
</u-linear-layout>
```

### 大小扩展

``` html
<u-linear-layout>
    <u-button size="small" color="primary">Small</u-button>
    <u-button color="primary">Normal</u-button>
    <u-button size="large" color="primary">Large</u-button>
</u-linear-layout>
```

### 正方形

``` html
<u-button square icon="refresh"></u-button>
```

### 图标

``` html
<u-linear-layout>
    <u-button color="primary" icon="create">创建实例</u-button>
    <u-button color="primary" icon="loading">立即创建</u-button>
    <u-button color="primary" icon="loading" disabled>立即创建</u-button>
    <u-button color="primary" icon="success">立即创建</u-button>
</u-linear-layout>
```

### 链接

``` html
<u-linear-layout>
    <u-button href="https://vusion.github.io" target="_blank">href</u-button>
    <u-button to="/proto-ui/u-link">to</u-button>
    <u-button href="https://vusion.github.io" disabled>disabled</u-button>
</u-linear-layout>
```

### 展示方式

``` html
<u-linear-layout direction="vertical" gap="small">
    <u-button display="inline">行内按钮（默认）</u-button> 与文字对齐
    <u-button display="block">块级按钮</u-button>
</u-linear-layout>
```

## API
### Props/Attrs

| Prop/Attr | Type | Default | Description |
| --------- | ---- | ------- | ----------- |
| href | String |  | 链接地址 |
| target | String |  | （原生属性） |
| to | String,  Location |  | 需要vue-router，与`<router-link>`的`to`属性相同。可以是一个字符串或者是描述目标位置的对象。 |
| replace | Boolean | `false` | 需要vue-router，与`<router-link>`的`replace`属性相同。如果为`true`，当点击时，会调用`router.replace()`而不是`router.push()`，于是导航后不会留下`history `记录。 |
| append | Boolean | `false` | 需要vue-router，与`<router-link>`的`append`属性相同。如果为`true`，则在当前路径后追加`to`的路径。 |
| color | String |  | 颜色扩展。可选值：`'primary'`或不填 |
| size | String |  | 大小扩展。可选值：`'small'`或不填 |
| square | Boolean | `false` | 是否显示为正方形 |
| disabled | Boolean | `false` | 是否禁用。禁用后不会响应`click`事件。 |
| display | String | `'inline'` | 展示方式。可选值：`'inline'`, `'block'` |

### Slots

#### (default)

插入文本或HTML。

### Events

#### $listeners

监听所有`<a>`元素的事件。

#### @before-navigate

使用router相关属性切换路由前触发

| Param | Type | Description |
| ----- | ---- | ----------- |
| $event.to | String,  Location | `to`属性的值 |
| $event.replace | Boolean | `replace`属性的值 |
| $event.append | Boolean | `append`属性的值 |
| $event.preventDefault | Function | 阻止切换流程 |

#### @navigate

使用router相关属性切换路由时触发

| Param | Type | Description |
| ----- | ---- | ----------- |
| $event.to | String,  Location | `to`属性的值 |
| $event.replace | Boolean | `replace`属性的值 |
| $event.append | Boolean | `append`属性的值 |
