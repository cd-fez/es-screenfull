
# es-screenfull 3.0.2-patch

* 在screenfull.js的基础上定制了es-screenfull 适配 chrome71 版本，详情参考[mdn](https://developer.mozilla.org/en-US/docs/Web/API/FullscreenOptions)

```
    // 改动代码为 dist/screenfull.js
    if (/5\.1[\.\d]* Safari/.test(navigator.userAgent)) {
        elem[request]();
    } else {
        if (keyboardAllowed) {
            elem[request](Element.ALLOW_KEYBOARD_INPUT);
        } else {
            elem[request]({ navigationUI: "auto" });
        }
    }
```