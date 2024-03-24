---
title: 队列 queue
---
# 队列 queue
## 创建队列
``` javascript
var queue_t = new algorm.queue([1,2,3])
var queue_t2 = new algorm.queue([1,2,4])
```
## 在最后插入元素
例如插入1
``` javascript
stack_t.push(1);
```
stack 变为
```
queue_t.push(1):  queue { arr: [ 1, 2, 3, 1 ], type: 'queue' }
```

## 弹出第一个元素
例如插入4
``` javascript
queue_t.pop()
```
stack 变为
```
console.log("queue_t.pop(): ",queue_t)
```

## 首个元素和末个元素
``` javascript
console.log("queue_t.front(): ",queue_t.front()) //首个元素
console.log("queue_t.back(): ",queue_t.back()) //末个元素
```
输出
```
queue_t.front():  1
queue_t.back():  1
```

## 长度、是否为空
``` javascript
console.log("queue_t.size(): ",queue_t.size,"\nqueue_t.empty(): ",queue_t.empty())
```
输出
```
queue_t.size():  3 
queue_t.empty():  false
```

## 交换两个队列的内容
则
```javascript
queue_t.swap(queue_t2);
```
可以让两个栈的内容交换
输出
```
queue_t.swap(queue_t2): 
   queue_t:  queue { arr: [ 1, 2, 4 ], type: 'queue' } 
   queue_t2:  queue { arr: [ 2, 3, 1 ], type: 'queue' } 
```



## 示例
```javascript
const algorm = require("algorm")


// queue
var queue_t = new algorm.queue([1,2,3])
var queue_t2 = new algorm.queue([1,2,4])

queue_t.push(1); // 在最后插入
console.log("queue_t.push(1): ",queue_t)
console.log("queue_t.front(): ",queue_t.front()) //首个元素
console.log("queue_t.back(): ",queue_t.back()) //末个元素

queue_t.pop() // 弹出第一个元素
console.log("queue_t.pop(): ",queue_t)

console.log("queue_t.size(): ",queue_t.size,"\nqueue_t.empty(): ",queue_t.empty())

queue_t.swap(queue_t2);
console.log("queue_t.swap(queue_t2): \n   queue_t: ",queue_t,"\n   queue_t2: ",queue_t2,"\n\n")
```
输出
```bash
queue_t.push(1):  queue { arr: [ 1, 2, 3, 1 ], type: 'queue' }
queue_t.front():  1
queue_t.back():  1
queue_t.pop():  queue { arr: [ 2, 3, 1 ], type: 'queue' }
queue_t.size():  3 
queue_t.empty():  false
queue_t.swap(queue_t2): 
   queue_t:  queue { arr: [ 1, 2, 4 ], type: 'queue' } 
   queue_t2:  queue { arr: [ 2, 3, 1 ], type: 'queue' } 

```