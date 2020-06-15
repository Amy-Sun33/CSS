```
    <div class="outside-box">
        <div class="inside-box">box盒子</div>
    </div>
```
## 元素定宽高

**公共代码**
```
    .outside-box {
        width: 500px;
        height: 500px;
        border: 1px solid #000;
    }

    .inside-box {
        background: red;
        width: 100px;
        height: 100px;
    }
```

1. **position + margin**
```
    .outside-box {
        position: relative;
    }
    .inside-box {
        position: absolute;
        top: 50%;
        left: 50%;
        margin-top: -50px;
        margin-left: -50px;
    }
```
2. **position + calc (在（1）上做拓展)**
```
    .outside-box {
        position: relative;
    }
    .inside-box {
        position: absolute;
        top: calc(50% - 50px);
        left: calc(50% - 50px);
    }
```
3. **flex**
```
    .outside-box {
        display: flex;
        align-items: center;
        justify-content: center;
    }
```
4. **position + margin: auto**
```
    .outside-box {
        position: relative;
    }
    .inside-box {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        margin: auto;
    }
```

## 元素不定宽高

**公共代码**
```
    .outside-box {
        width: 500px;
        height: 500px;
        border: 1px solid #000;
    }
```
1. **position + transform**
```
    .outside-box {
        position: relative;
    }
    .inside-box {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
```

2. **css-table**
```
    .outside-box {
        display: table-cell;
        text-align: center;
        vertical-align: middle;
    }
    .inside-box {
        display: inline-block;
    }
```