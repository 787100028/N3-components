<template>

### 滑块

<div class="bs-docs-section" >
<div class="bs-example">
<n3-slider v-model="value" @change="change" orientation="vertical" ></n3-slider>
<p>滑块的值: {{value}}</p> 

<n3-slider v-model="value1" @change="change" :range="true"></n3-slider>
<p>滑块的值: {{value1}}</p> 
</div>

```html
<n3-slider v-model="value" @change="change" orientation="vertical"></n3-slider>
<n3-slider v-model="value1" @change="change" :range="true"></n3-slider>
```

```javascript
export default {
  data () {
    return {
      value: 2
    }
  },
  methods: {
    change (val) {
      console.log(val)
    }
  }
}
```

### 参数

| 参数          | 类型            |   默认值         |   说明   |
|-------------  |---------------- |----------------  |-------- |
| min          | `Number`    |    `0`        |     最小值    |
| max          | `Number`     |    `0`        |     最大值    |
| step          | `Number`     |    `1`       |     单步增量    |
| orientation          | String`     |    `horizontal`      |     `horizontal`(水平) `vertical`(垂直)    |
| range          | `Boolean`     |    `false`       |     是否范围选择    |
| tooltip          | `String`     |    `show`      |     tooltip显示参数 'show' 'hide' 'always'    |
| disabled          | `Boolean`     |    `false`       |     是否禁用    |
| formatter          | `Function`     |    -       |     格式化tooltip显示内容    |
| width          | `String`     |   `220px`      |     水平显示的宽度    |
| height          | `String`     |    `220px`      |     水平显示的宽度    |

### 事件

| 名称          |   说明          |     参数   
|-------------  |---------------- |---|
| change | 值变化 |(currentValue) |

其他表单相关参数，请移步 <a href="#n3FormDocs" >表单验证</a> 待验证组件参数

</div>
</template>

<script>
export default {
  data () {
    return {
      value:1,
      value1: [1, 2]
    }
  },
  methods: {
    change (val) {
      console.log(val)
    }
  }
}
</script>
