---
category: Components
type: Navigation
chinese: 气泡
english: Popover
source: design
---


在点击控件或者某个区域后，浮出一个气泡区域来放置更多的操作或者信息。

### 规则
- 通过点击背景的任一位置，进行退出。


## API

### Popover
| 成员        | 说明           | 类型         | 默认值       |
|------------|----------------|-------------|--------------|
| visible(web)   | 当前显隐状态    | Boolean |  false   |
| onVisibleChange(web)   | 当显隐状态变化时调用    | Function |  -   |
| placement(web)   | enum{'left','right','top','bottom', 'topLeft', 'topRight', 'bottomLeft', 'bottomRight'} | String |  'bottomRight'   |
| popupAlign(web)   | 用于设置偏移量等、会被合并到 placement 的设置中，可选值为 [dom-align](https://github.com/yiminghe/dom-align) 的`alignConfig`配置（ points 设置用 placement 代替）   | Object |  { overflow: { adjustY: 0, adjustX: 0 } } 禁掉位置自动适应 |
| mask(web)   | 是否显示遮罩背景层    | Boolean |  false  |
| overlay   | 弹出层内容    | React.node |  -   |
| onSelect   | 选中的选项    | Function |  -   |
| style  | menu 样式    | Object |  -   |
| triggerStyle(iOS/android)   | 触发元素外围容器样式    | Object |  -   |
| overlayStyle(iOS/android)   | 弹出层外围容器样式    | Object |  -   |
| contextStyle(iOS/android)   | 最外围容器样式    | Object |  -   |
| renderOverlayComponent(iOS/android)   | 自定义弹出层的外围组件，默认是`ScrollView`，示例`(opts) => <Cus>{opts}</Cus>`  | Function |  -   |
| name(iOS/android)   | menu 名字，用于手动触发开关 menu    | String |  -   |
| openMenu / closeMenu / toggleMenu(iOS/android)   | 用于手动开关 menu，参数为上边 menu 的 name. 使用示例见 demo  | Function(name) |  -   |

### Popover.Item
| 成员        | 说明           | 类型         | 默认值       |
|------------|----------------|-------------|--------------|
| children   | 节点内容    | String/React.node |  -   |
| disabled   | 是否禁用    | Boolean |  false   |
| icon   | icon    | React.Node |  -   |