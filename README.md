# picker
移动端多选控件

# Use
```shell
$ npm install vt-picker -s
```

```shell
 import picker from 'vt-picker'
 
 Vue.component('Picker', Picker)
```
 
 
 # Api
 ### Props 
*   `valueField` String类型，每一项的值字段，默认值`id`
*   `textField` String类型，每一项的文本字段，默认值`text`
*   `header` Array类型,头部标题的数组，默认值为空数组( [] ),若为空数组，不显示每一项的头部标题
*   `changeAfterToTop` Boolean类型，默认为`true`,改变某一列的选择项后,该列后面的所有列是否选中第一项
*   `changeEventAll` Boolean类型，默认为`true`,改变某一列的选择项后 是否触发后续列的选择项改变事件
*   `data` 组件的数据，**更改该属性，组件立刻更新**
*   `tabLayout` Array类型,页面的布局每一页有几列，如`[2,1]`(共两也，第一页显示两列，第二页显示1列)，默认计算获取（根据数据的列数，每一页三列来显示数据)
*   `selectIndexs` Array类型，组件默认选中项目，可以是每一列项目的索引，如[12,3,2,3,4],也可以是每一列想要选中项目的Object对象，如[{"id":12,"text":"河北省"},{"id":1201,"text":"丛台区"},{"id":120102,"text":"中华北大街"},{"id":12010205,"text":"天和园村委会"}]，**更改该属性，组件立刻更新**
 ### Event
  *   `change` (key,Object,index) 选中每一列的某一项时触发，参数是当前列的`key`和 选中项目的`Object`值和当前选中项的在该列的索引
  *   `done` (value,map) 点击确定按钮时触发，参数是组件最后一列的选中项的值和所有列选中项目的`Object`值

# Waring
* 该组件采用rem布局，请使用淘宝rem布局方式
