## css 粘性定位

**前言**

position:stricky是css定位新增属性；可以说是相对于relative和固定定位fixed的结合；主要用在对scroll事件的监听上；在滑动的过程中，某个元素距离其父亲的距离达到sticky粘性定位的要求时；position:sticky
这时的效果相当于fixed定位，固定到适当的位置 (替代通过scroll获取高度)。

**使用**
```
  #box {
    position: sticky;
    top: 10px;
    z-index: 10
  }
```

**使用条件**
1. 父元素不能 overflow:hidden 或者 overflow:auto 属性
2. 必须指导 top、bottom、left、right 4个值之一
3. 父元素的高度不能低于sticky元素的高度
4. sticky 元素仅在其父元素内生效
