---
title: Redux Actions
localeTitle: Redux动作
---
## Redux动作

Redux操作是一个简单的对象，它描述了应用程序中发生了什么类型的事件。他们甚至可以包含 需要从应用程序发送到Redux存储的数据。动作可以包含任何内容，但必须具有强制性 type属性，描述发生的事件。一个好的做法是在描述动作时使用const常量。如果你想在redux动作中使用异步代码获取数据，你可以使用更高级的动作生成器(action creator)，详情请参照相关文档。

例如

```javascript
// actionTypes.js
const ADD_ITEM = 'ADD_ITEM'
const REMOVE_ITEM = 'REMOVE_ITEM'
```

```javascript
// ./actions/item.js

import * as actionTypes from './actionTypes'
export const addItem = () => { 
  return {
     type: ADD_ITEM, 
     text: 'This is the first item' 
   }
 } 
```

我们可以使用将这些操作发送到商店 `javascript store.dispatch()` 应用程序可以一次发生不同类型的事件，这些操作有助于描述这些事件。没有这些操作，就无法更改应用程序存储在Redux中的状态。

您可以尝试使用[redux-actions](https://github.com/redux-utilities/redux-actions)项目来减少大量的样板制作，从而更快地编写您的操作。

#### 更多信息：

[行动 - Redux官方文档](https://redux.js.org/basics/actions) [redux-actions](https://github.com/redux-utilities/redux-actions) github项目页面
