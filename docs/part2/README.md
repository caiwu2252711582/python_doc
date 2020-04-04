## 注释

> `单行注释`

?>以#开头,#右边的所有东西当做说明，而不是真正要执行的程序，起辅助说明作用

```python
 # 我是注释，可以在里写一些功能说明之类的哦
    print('hello world')
```

> `多行注释`

```
'''我是多行注释，可以写很多很多行的功能说明
        这就是我牛X指出

        哈哈哈。。。
    '''

    '''
        下面的代码完成 ，打印一首诗
        名字叫做：春江花月夜
        作者，忘了
    '''
```

## 中文支持

!> 在 python2 中直接使用中文会报错

> 解决办法，在程序的开头写入如下代码

```
 #coding=utf-8
```

?> 注意：
在 python 的语法规范中推荐使用的方式:

```
# -*- coding:utf-8 -*-
```

> ?> :golf: python3 全面支持中文编码

## 变量以及类型

> 变量的定义

在程序中，有时我们需要对 2 个数据进行求和，那么该怎样做呢？

大家类比一下现实生活中，比如去超市买东西，往往咱们需要一个菜篮子，用来进行存储物品，等到所有的物品都购买完成后，在收银台进行结账即可如果在程序中，需要把 2 个数据，或者多个数据进行求和的话，那么就需要把这些数据先存储起来，然后把它们累加起来即可。

在 Python 中，存储一个数据，需要一个叫做变量的东西，如下示例:

```python
num1 = 100 #num1就是一个变量，就好一个小菜篮子
num2 = 87  #num2也是一个变量
result = num1 + num2 #把num1和num2这两个"菜篮子"中的数据进行累加，然后放到 result变量中
```

> 变量的类型

![logo](../img/1.png ':size=800x500')

## 关键字

> 什么是关键字

python 一些具有特殊功能的标示符，这就是所谓的关键字
关键字，是 python 已经使用的了，所以不允许开发者自己定义和关键字相同的名字的标示符。

> 查看关键字: 可通过 `keywords.kwlist` 查看

```js
and     as      assert     break     class      continue    def     del
elif    else    except     exec      finally    for         from    global
if      in      import     is        lambda     not         or      pass
print   raise   return     try       while      with        yield
```

```js
/*!
 * docsify-copy-code
 * v2.1.0
 * https://github.com/jperasmus/docsify-copy-code
 * (c) 2017-2019 JP Erasmus <jperasmus11@gmail.com>
 * MIT license
 */
!(function () {
  'use strict'
  function r(o) {
    return (r =
      'function' == typeof Symbol && 'symbol' == typeof Symbol.iterator
        ? function (o) {
            return typeof o
          }
        : function (o) {
            return o &&
              'function' == typeof Symbol &&
              o.constructor === Symbol &&
              o !== Symbol.prototype
              ? 'symbol'
              : typeof o
          })(o)
  }
  !(function (o, e) {
    void 0 === e && (e = {})
    var t = e.insertAt
    if (o && 'undefined' != typeof document) {
      var n = document.head || document.getElementsByTagName('head')[0],
        c = document.createElement('style')
      ;(c.type = 'text/css'),
        'top' === t && n.firstChild
          ? n.insertBefore(c, n.firstChild)
          : n.appendChild(c),
        c.styleSheet
          ? (c.styleSheet.cssText = o)
          : c.appendChild(document.createTextNode(o))
    }
  })(
    '.docsify-copy-code-button,.docsify-copy-code-button span{cursor:pointer;transition:all .25s ease}.docsify-copy-code-button{position:absolute;z-index:1;top:0;right:0;overflow:visible;padding:.65em .8em;border:0;border-radius:0;outline:0;font-size:1em;background:grey;background:var(--theme-color,grey);color:#fff;opacity:0}.docsify-copy-code-button span{border-radius:3px;background:inherit;pointer-events:none}.docsify-copy-code-button .error,.docsify-copy-code-button .success{position:absolute;z-index:-100;top:50%;left:0;padding:.5em .65em;font-size:.825em;opacity:0;-webkit-transform:translateY(-50%);transform:translateY(-50%)}.docsify-copy-code-button.error .error,.docsify-copy-code-button.success .success{opacity:1;-webkit-transform:translate(-115%,-50%);transform:translate(-115%,-50%)}.docsify-copy-code-button:focus,pre:hover .docsify-copy-code-button{opacity:1}'
  ),
    document.querySelector('link[href*="docsify-copy-code"]') &&
      console.warn(
        '[Deprecation] Link to external docsify-copy-code stylesheet is no longer necessary.'
      ),
    (window.DocsifyCopyCodePlugin = {
      init: function () {
        return function (o, e) {
          o.ready(function () {
            console.warn(
              '[Deprecation] Manually initializing docsify-copy-code using window.DocsifyCopyCodePlugin.init() is no longer necessary.'
            )
          })
        }
      },
    }),
    (window.$docsify = window.$docsify || {}),
    (window.$docsify.plugins = [
      function (o, s) {
        o.doneEach(function () {
          var o = Array.apply(
              null,
              document.querySelectorAll('pre[data-lang]')
            ),
            c = {
              buttonText: '复制代码',
              errorText: 'Error',
              successText: 'Copied',
            }
          s.config.copyCode &&
            Object.keys(c).forEach(function (t) {
              var n = s.config.copyCode[t]
              'string' == typeof n
                ? (c[t] = n)
                : 'object' === r(n) &&
                  Object.keys(n).some(function (o) {
                    var e = -1 < location.href.indexOf(o)
                    return (c[t] = e ? n[o] : c[t]), e
                  })
            })
          var e = [
            '<button class="docsify-copy-code-button">',
            '<span class="label">'.concat(c.buttonText, '</span>'),
            '<span class="error">'.concat(c.errorText, '</span>'),
            '<span class="success">'.concat(c.successText, '</span>'),
            '</button>',
          ].join('')
          o.forEach(function (o) {
            o.insertAdjacentHTML('beforeend', e)
          })
        }),
          o.mounted(function () {
            document
              .querySelector('.content')
              .addEventListener('click', function (o) {
                if (o.target.classList.contains('docsify-copy-code-button')) {
                  var e =
                      'BUTTON' === o.target.tagName
                        ? o.target
                        : o.target.parentNode,
                    t = document.createRange(),
                    n = e.parentNode.querySelector('code'),
                    c = window.getSelection()
                  t.selectNode(n), c.removeAllRanges(), c.addRange(t)
                  try {
                    document.execCommand('copy') &&
                      (e.classList.add('success'),
                      setTimeout(function () {
                        e.classList.remove('success')
                      }, 1e3))
                  } catch (o) {
                    console.error('docsify-copy-code: '.concat(o)),
                      e.classList.add('error'),
                      setTimeout(function () {
                        e.classList.remove('error')
                      }, 1e3)
                  }
                  'function' == typeof (c = window.getSelection()).removeRange
                    ? c.removeRange(t)
                    : 'function' == typeof c.removeAllRanges &&
                      c.removeAllRanges()
                }
              })
          })
      },
    ].concat(window.$docsify.plugins || []))
})()
//# sourceMappingURL=docsify-copy-code.min.js.map
```
