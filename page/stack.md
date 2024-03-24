---
title: 栈 stack
---
# 栈 stack
## 创建栈
``` javascript
var stack_t = new algorm.stack([1,2,3])
```
## 在最后插入元素
例如插入1
``` javascript
stack_t.push(1);
```
stack 变为
```
stack { arr: [ 1, 2, 3, 1 ], type: 'stack' }
```

## 在最前插入元素
例如插入4
``` javascript
stack_t.emplace(4);
```
stack 变为
```
stack { arr: [ 4, 1, 2, 3, 1 ], type: 'stack' }
```

## 弹出最后一个元素
``` javascript
stack_t.pop()
```
stack变为
```
stack { arr: [ 4, 1, 2, 3 ], type: 'stack' }
```

## 交换两个栈的内容
再创建一个栈
``` javascript
var stack_t2 = new algorm.stack([1,2,4])
```
则
```javascript
stack_t.swap(stack_t2);
```
可以让两个栈的内容交换

## 清除栈
``` javascript
stack_t.clear()
```
stack变为
```
stack { arr: [], type: 'stack' } 
```

此时如果输出 `stack_t.size`,则输出0
如果调用 `stack_t.empty()`,则输出`true

## 示例
```javascript
const algorm = require("algorm")

// stack 
var stack_t = new algorm.stack([1,2,3])
var stack_t2 = new algorm.stack([1,2,4])
stack_t.push(1); // 在最后插入
console.log("stcak_t.push(1): ",stack_t)
console.log("stcak_t.top(): ",stack_t.top()) //第一个元素

stack_t.emplace(4); //在最前插入
console.log("stcak_t.emplace(4): ",stack_t)

stack_t.pop() // 弹出最后一个元素
console.log("stack_t.pop(): ",stack_t)

stack_t.clear() //清除
console.log("stack_t.clear(): ",stack_t,"\nstcak_t.size(): ",stack_t.size,"\nstack_t.empty()",stack_t.empty())

stack_t.swap(stack_t2); // 交换
console.log("stack_t.swap(stack_t2): \n  stcak_t: ",stack_t,"\n  stcak_t2: ",stack_t2,"\n\n")
```
输出
```bash
stcak_t.push(1):  stack { arr: [ 1, 2, 3, 1 ], type: 'stack' }
stcak_t.top():  1
stcak_t.emplace(4):  stack { arr: [ 4, 1, 2, 3, 1 ], type: 'stack' }
stack_t.pop():  stack { arr: [ 4, 1, 2, 3 ], type: 'stack' }
stack_t.clear():  stack { arr: [], type: 'stack' } 
stcak_t.size():  0 
stack_t.empty() true
stack_t.swap(stack_t2): 
  stcak_t:  stack { arr: [ 1, 2, 4 ], type: 'stack' } 
  stcak_t2:  stack { arr: [], type: 'stack' } 

```