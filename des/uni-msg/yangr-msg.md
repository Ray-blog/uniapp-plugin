yangr-msg
--

### 使用方式

使用组件

```html
<yangr-msg v-if="yangrMsgShow" :title="title" type="success" :info="info" btn="确定" @yangrMsgEvent="closeYangrMsg"></yangr-msg>
```

引用组件(局部引入)

```js
import yangrMsg from "@/components/yangr-msg/yangr-msg.vue"
export default {
    components: {yangrMsg},
    data() {
        return {
            title: '小程序测试标题',
            info: '小程序测试提示信息小程序测试提示信息小程序测试提示信息小程序',
            yangrMsgShow: false,
        }
    },
    methods: {
        closeYangrMsg(){
            this.yangrMsgShow = false;
        }
    }
}
```

### 属性说明

| 属性名 |  类型  | 默认值  |                       说明                        |
| :----: | :----: | :-----: | :-----------------------------------------------: |
| title  | String |    -    | title 为空时根据 type ，显示"操作成功"/"操作失败" |
|  type  | String | success |                 success or error                  |
|  info  | String |    -    |                 info 为空时不显示                 |
|  btn   | String |  确定   |                         -                         |



