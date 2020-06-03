## CSS 常用总结

### 三角形

```markdown
.triangle {
    width: 0;
    height: 0;
    border-style: solid;
    border-width: 0 25px 40px 25px;  // 上 右 下 左
    border-color: transparent  transparent rgba(245, 129,127) transparent;
}
```

### 单行文本超出省略

```markdown
.single-ellipsis {
    width: 300px;
    overflow: hidden;
    white-space: nowrap;  // 超出不换行
    text-overflow: ellipsis;  // 超出显示...
}
```

### 多行文本超出省略

```markdown
.single-ellipsis {
    display: -webkit-box;  // 将对象作为弹性伸缩盒子模型显示
    word-break: break-all;   
    -webkit-box-orient: vertical;    // 设置或检索伸缩盒对象的子元素的排列方式
    -webkit-line-clamp: 4;   //需要显示的行数
    overflow: hidden;
    text-overflow: ellipsis; // 超出显示...
}
```

### 滚动时隐藏滚动条

```markdown
::-webkit-scrollbar {
  display: none;
}
```

### 气泡阴影

```markdown
  .tip { 
        width: 100px;
        height: 30px;
        position: relative;
        border: 1px solid rgba(245, 129, 127);
        border-radius: 4px;
        background-color: #fff;
        filter: drop-shadow(0 2px 10px rgba(245, 129, 127, 0.9));    // 图像展示阴影效果
    }

    /* 实现空心三角形：用一个实心的白色给覆盖 */
    .tip::before {
        content: '';
        width: 0;
        height: 0;
        position: absolute;
        top: -10px;
        left: 0;
        right: 0;
        margin: auto;
        border-style: solid;
        border-width: 0 10px 10px 10px;
        border-color: transparent transparent #fff transparent;
        z-index: 2;
    }

    .tip::after {
        content: '';
        width: 0;
        height: 0;
        border-style: solid;
        position: absolute;
        border-width: 0 10px 10px 10px;
        border-color: transparent transparent rgba(245, 129, 127) transparent;
        top: -11px;
        left: 0;
        right: 0;
        margin: auto;
        z-index: 1;
    }
```
