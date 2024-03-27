---
title: 链表 linkedlist
---
# 链表 linkedlist
## 创建链表
``` javascript
var linkedlist1 = new algorm.linkedlist()
```
## 追加元素
例如依次插入 A,B,C
``` javascript
linkedlist1.append("A")
linkedlist1.append("B")
linkedlist1.append("C")
console.log(".append('A')/'B'/'C' : ",linkedlist1)
```
linkedlist1 变为
``` bash
.append('A')/'B'/'C' :  LinkedList {
  length: 3,
  head: { data: 'A', next: { data: 'B', next: [Object] } }
}
```

## 转为字符串
``` javascript
console.log("linkedlist1.toString(): ",linkedlist1.toString());
```
输出
``` bash
linkedlist1.toString():  A B C 
```

## 在指定位置加入元素
``` javascript
linkedlist1.insert(0, "123");
linkedlist1.insert(2, "456");
console.log(".insert(0,'123')/(2,'456') : ",linkedlist1.toString());
```
::: tip
两个参数中，第一个代表插入位置，第二个代表插入内容
:::
输出
```bash
.insert(0,'123')/(2,'456') :  123 A 456 B C 
```

## 获取指定位置的数据
``` javascript
console.log("linkedlist1.getData(0): ",linkedlist1.getData(0));
console.log("linkedlist1.getData(1): ",linkedlist1.getData(1));
```
输出
```
linkedlist1.getData(0):  123
linkedlist1.getData(1):  A
```

## 更新指定位置的元素
则
```javascript
linkedlist1.update(0, "12345");
console.log(linkedlist1.toString()); 
linkedlist1.update(1, "54321");
console.log(linkedlist1.toString());
```
::: tip
第一个参数是更新位置，第二个是更新后的内容
:::
输出
``` bash
12345 54321 456 B C 
```

## 删除元素
### 删除指定位置的元素
```javascript
linkedlist1.removeAt(3);
console.log(linkedlist1.toString());
```
输出
```
12345 54321 456 C 
```

### 删除指定内容的元素
``` javascript
linkedlist1.remove("CC");
console.log(linkedlist1.toString()); 
```
输出
```
12345 54321 456 C 
```
::: tip
由于这个链表中没有元素`CC`，所以没有删除。如果一个链表中存在多个目标，那么删除更靠前的。
:::

## 长度和是否为空
### 链表是否为空
```javascript
console.log(linkedlist1.isEmpty()); 
```
输出 `false`

### 链表长度
```javascript
console.log(linkedlist1.size()); 
```
输出`4`

## 示例
```javascript
const algorm = require("algorm")

//linkedlist
var linkedlist1 = new algorm.linkedlist()
linkedlist1.append("A")
linkedlist1.append("B")
linkedlist1.append("C")
console.log(".append('A')/'B'/'C' : ",linkedlist1)

console.log("linkedlist1.toString(): ",linkedlist1.toString());

linkedlist1.insert(0, "123");
linkedlist1.insert(2, "456");
console.log(".insert(0,'123')/(2,'456') : ",linkedlist1.toString());

console.log("linkedlist1.getData(0): ",linkedlist1.getData(0));
console.log("linkedlist1.getData(1): ",linkedlist1.getData(1));

linkedlist1.update(0, "12345");
console.log(linkedlist1.toString()); 
linkedlist1.update(1, "54321");
console.log(linkedlist1.toString());

// 测试 removeAt 方法
linkedlist1.removeAt(3);
console.log(linkedlist1.toString());

// 测试 remove 方法
linkedlist1.remove("CC");
console.log(linkedlist1.toString()); 

// 测试 isEmpty 方法
console.log(linkedlist1.isEmpty()); 

// 测试 size 方法
console.log(linkedlist1.size()); 
```
输出
```bash
.append('A')/'B'/'C' :  LinkedList {
  length: 3,
  head: { data: 'A', next: { data: 'B', next: [Object] } }
}
linkedlist1.toString():  A B C 
.insert(0,'123')/(2,'456') :  123 A 456 B C 
linkedlist1.getData(0):  123
linkedlist1.getData(1):  A
12345 A 456 B C 
12345 54321 456 B C 
12345 54321 456 C 
12345 54321 456 C 
false
4

```