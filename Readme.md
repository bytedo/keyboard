## JS键盘热键
> 支持各种按钮组合。
>> 1.0版 功能键(Shift, Ctrl, Alt/Option, Win/Cmd)不区分左右。


![keyboard](./keyboard.jpg)


### 辅助功能键
> 辅助功能键, 不支持单独设置热键。
>> 包括 `Ctrl、Shift、Alt/Option、Win/Cmd` 这4个。

## 普通按键
> 即除了辅助功能键以外的其他按键。可以单独设置, 也可以配合辅助按键组合使用。
>> 但是, 不允许在一组里出现多次。如需要, 请分组。

```js

var kb = new Keyboard()

// 同时出现C和V这2个普通按键, 是不允许的,
kb.on(['ctrl + c + v'], ev => {
  // todo...
})

// 须改成分2组写
kb.on(['ctrl + c', 'ctrl + v'], ev => {
  // todo...
})

```


