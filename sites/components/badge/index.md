# Badge 徽标

图标右上角的圆形徽标数字。

### 何时使用

出现在图标右上角或列表项右方，通过不同的状态色加数字提示用户有消息需要处理时。

### 基本徽章

基本徽章类型，当有包裹元素时在右上角显示徽章和数目。

<d-badge :count='6' status="danger" class="devui-badge-item">未读消息</d-badge>
<d-badge :count='7' status="waiting" class="devui-badge-item">未读消息</d-badge>
<d-badge :count='8' status="success" class="devui-badge-item">未读消息</d-badge>
<d-badge :count='100' status="info" class="devui-badge-item">未读消息</d-badge>

```html
<d-badge :count="6" status="danger">未读消息</d-badge>
<d-badge :count="7" status="waiting">未读消息</d-badge>
<d-badge :count="8" status="success">未读消息</d-badge>
<d-badge :count="100" status="info">未读消息</d-badge>
```

### 点状徽章

点状徽章类型，当有包裹元素且 showDot 参数为 true 时为点状徽章，默认在右上角展示小点不显示数目。

<d-badge status="danger" showDot class="devui-badge-item">未读消息</d-badge>
<d-badge status="waiting" showDot class="devui-badge-item">未读消息</d-badge>
<d-badge status="warning" showDot class="devui-badge-item">
<d-icon name="like" />
</d-badge>
<d-badge status="info" showDot class="devui-badge-item">
<d-icon name="like" />
</d-badge>

```html
<d-badge status="danger" showDot>未读消息</d-badge>
<d-badge status="waiting" showDot>未读消息</d-badge>
<d-badge status="warning" showDot>
  <d-icon name="like" />
</d-badge>
<d-badge status="info" showDot>
  <d-icon name="like" />
</d-badge>
```

### 计数徽章

当徽章独立使用且不包裹任何元素时，只展示徽章状态色和数目。

<ul class="devui-badge-list">
  <li class="devui-badge-list-item">
    <span>系统消息</span>
    <d-badge status="danger" :count="50"></d-badge>
  </li>
  <li class="devui-badge-list-item">
    <span>个人消息</span>
    <d-badge status="info" :count="500"></d-badge>
  </li>
</ul>

```html
<ul class="devui-badge-list">
  <li class="devui-badge-list-item">
    <span>系统消息</span>
    <d-badge status="danger" :count="50"></d-badge>
  </li>
  <li class="devui-badge-list-item">
    <span>个人消息</span>
    <d-badge status="danger" :count="500"></d-badge>
  </li>
</ul>
```

### 状态徽章

当徽章独立使用、不包裹任何元素且 showDot 参数为 true 时为状态徽章，不同状态展示不同色点。

<d-badge status="danger" showDot></d-badge>&nbsp danger <br />
<d-badge status="warning" showDot></d-badge>&nbsp warning <br />
<d-badge status="waiting" showDot></d-badge>&nbsp waiting <br />
<d-badge status="info" showDot></d-badge>&nbsp info <br />
<d-badge status="success" showDot></d-badge>&nbsp success <br />

```html
<d-badge status="danger" showDot></d-badge>&nbsp danger <br />
<d-badge status="warning" showDot></d-badge>&nbsp warning <br />
<d-badge status="waiting" showDot></d-badge>&nbsp waiting <br />
<d-badge status="info" showDot></d-badge>&nbsp info <br />
<d-badge status="success" showDot></d-badge>&nbsp success <br />
```

### 徽章位置

通过 badgePos 参数设置徽章位置。

<d-badge :count='6' status="danger" badgePos="top-left" class="devui-badge-item">未读消息</d-badge>
<d-badge :count='7' status="waiting" badgePos="top-right" class="devui-badge-item">未读消息</d-badge>
<d-badge :count='8' status="success" badgePos="bottom-left" class="devui-badge-item">
<d-icon name="emoji" /></d-badge>
<d-badge :count='100' status="info" badgePos="bottom-right" class="devui-badge-item">
<d-icon name="notice" />
</d-badge>

```html
<d-badge :count="6" status="danger" badgePos="top-left">未读消息</d-badge>
<d-badge :count="7" status="waiting" badgePos="top-right">未读消息</d-badge>
<d-badge :count="8" status="success" badgePos="bottom-left">
  <d-icon name="emoji" />
</d-badge>
<d-badge :count="100" status="info" badgePos="bottom-right">
  <d-icon name="notice" />
</d-badge>
```

### 自定义

通过 bgColor 参数设置徽章展示状态色(此时 status 参数设置的徽章状态色失效)，通过 offsetXY 参数可设置相对于 badgePos 的徽章偏移量。通过 textColor、bgColor 自定义文字、背景颜色。

<d-badge :count="666" status="success" style="margin-right: 20px">
<d-icon name="notice" />
</d-badge>
<d-badge :count="666" status="success" style="margin-right: 30px" :offsetXY='[-10, 0]'>
<d-icon name="notice" />
</d-badge>
<d-badge count="6" style="margin-right: 20px" :offsetXY='[0, -10]' >未读消息</d-badge>
<d-badge count="6" bgColor="red" textColor="#fff" style="margin-right: 20px">未读消息</d-badge>
<d-badge count="2.3k" bgColor="#000" textColor="#fff"></d-badge>

```html
<d-badge :count="666" status="success" style="margin-right: 20px">
  <d-icon name="notice" />
</d-badge>
<d-badge :count="666" status="success" style="margin-right: 30px" :offsetXY="[-10, 0]">
  <d-icon name="notice" />
</d-badge>
<d-badge count="6" style="margin-right: 20px" :offsetXY="[0, -10]">未读消息</d-badge>
<d-badge count="6" bgColor="red" textColor="#fff" style="margin-right: 20px">未读消息</d-badge>
<d-badge count="2.3k" bgColor="#000" textColor="#fff"></d-badge>
```

### API

|   参数    |        类型         |    默认     | 说明                                                                                                                         |
| :-------: | :-----------------: | :---------: | :--------------------------------------------------------------------------------------------------------------------------- |
|   count   |      `Number`       |     --      | 可选，设置基本徽章和计数徽章中显示的数目                                                                                     |
| maxCount  |      `Number`       |     99      | 可选，设置基本徽章和计数徽章最大可显示数目，当 count > maxCount 时显示 maxCount+                                             |
|  showDot  |      `Boolean`      |    false    | 可选，true 时为点状徽章(有包裹)或状态徽章(无包裹)，false 时为基本徽章(有包裹)或计数徽章(无包裹)                              |
|  status   |  `BadgeStatusType`  |     --      | 可选，状态色 danger\| warning \| waiting \| success \| info                                                                  |
| badgePos  | `BadgePositionType` | 'top-right' | 可选，徽标位置 top-left\| top-right \| bottom-left \| bottom-right                                                           |
|  bgColor  |      `String`       |     --      | 可选，自定义徽标色，此时 status 参数设置的徽章状态色失效                                                                     |
| textColor |      `String`       |     --      | 可选， 可自定义徽标文字颜色                                                                                                  |
| offsetXY  | `[number, number] ` |     --      | 可选，可选，有包裹时徽标位置偏移量，格式为[x,y]，单位为 px。x 为相对 right 或 left 的偏移量，y 为相对 top 或 bottom 的偏移量 |

<style lang="scss">
@import '@devui-design/icons/icomoon/devui-icon.css';
.devui-badge-item {
  background: #f3f6f8; 
  margin-right:20px;
  border-radius: 8px;
  padding: 4px 10px;
  font-size: 14px;
}
.devui-badge-list {
  width: 180px;
  padding: 4px 20px;
  background: #f3f6f8;
  font-size: 14px;
  border-radius: 8px;
  .devui-badge-list-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>