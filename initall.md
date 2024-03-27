---
title: 起步
---
# algorm.js 能做什么
目前支持的算法：
- string
- sort  

支持的数据结构:
- set
- graph 
- hash
- doublylinkedlist
- linkedlist
- queue
- stack 
- tree

::: tip
现 `beta` 阶段不支持某些数据结构和算法互通，例如不能使用`sort`算法给`queue`排序，只能使用`queue`库内置的排序算法
:::

# algorm.js 安装
``` bash
npm install algorm
```

::: tip
若安装后不能正常 require 导入包，则删除工作目录下 `node_moudules` 文件夹中的 `algorm` 文件夹，再重新安装
:::

现在你已经初步完成了 `algorm.js` 的准备工作