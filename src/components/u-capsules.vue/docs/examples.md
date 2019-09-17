### 基本样式

``` html
<u-capsules>
    <u-capsule>Apple</u-capsule>
    <u-capsule>Banana</u-capsule>
    <u-capsule>Cake</u-capsule>
</u-capsules>
```

### 选择值

``` html
<u-capsules value="C">
    <u-capsule value="A">Apple</u-capsule>
    <u-capsule value="B">Banana</u-capsule>
    <u-capsule value="C">Cake</u-capsule>
</u-capsules>
```

### 只读、禁用、禁用某一项

``` html
<u-linear-layout>
<u-capsules value="C" readonly>
    <u-capsule value="A">Apple</u-capsule>
    <u-capsule value="B">Banana</u-capsule>
    <u-capsule value="C">Cake</u-capsule>
</u-capsules>
<u-capsules value="C" disabled>
    <u-capsule value="A">Apple</u-capsule>
    <u-capsule value="B">Banana</u-capsule>
    <u-capsule value="C">Cake</u-capsule>
</u-capsules>
<u-capsules value="C">
    <u-capsule value="A">Apple</u-capsule>
    <u-capsule value="B" disabled>Banana</u-capsule>
    <u-capsule value="C">Cake</u-capsule>
</u-capsules>
</u-linear-layout>
```

### 可取消

点击两次同一项，可取消状态

``` html
<u-capsules value="C" cancelable>
    <u-capsule value="A">Apple</u-capsule>
    <u-capsule value="B">Banana</u-capsule>
    <u-capsule value="C">Cake</u-capsule>
</u-capsules>
```

### 多项选择

绑定`value`属性，可以用`v-model`或`:value.sync`。

``` html
<u-capsules :value="['B', 'C']" multiple>
    <u-capsule value="A">Apple</u-capsule>
    <u-capsule value="B">Banana</u-capsule>
    <u-capsule value="C">Cake</u-capsule>
</u-capsules>
```

### 胶囊组

``` html
<u-capsules>
    <u-capsules-group>
        <u-capsule>Apple</u-capsule>
        <u-capsule>Banana</u-capsule>
        <u-capsule>Cake</u-capsule>
    </u-capsules-group>
    <u-capsules-group>
        <u-capsule>Apple</u-capsule>
        <u-capsule>Banana</u-capsule>
        <u-capsule>Cake</u-capsule>
    </u-capsules-group>
</u-capsules>
```
