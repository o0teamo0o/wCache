# wCache
微信小程序缓存框架，支持数组、json、字符串……支持设置缓存时间、支持缓存读取失败默认值。
# 一、公共方法
## put(k, v, t)
k为key，v为具体内容（支持字符串、json、数组、boolean等等），t为可选参数表示过期时间（单位：秒）<br>
如存储k为123过期时间1秒，则调用put('k', '123', 1)方法；若永久存储调用put('k', '123')<br>
永久保存json：put('k', {"a":"1"})，数组、boolean等同理。
## get(k, def)
k为key，def为可选参数，表示无缓存数据时返回值（支持字符串、json、数组、boolean等等）<br>
如读取k缓存，则调用get('k')；若想要无缓存时，返回默认值则get('k','默认值')，支持各个数据类型。<br>
## remove(k)
移除某个key
## clear()
清空所有key
## other
使用wx原生的即可。<br>
如何使用
# 二、如何使用
1. 下载src文件夹内wCache.js文件
2. 需要使用的js文件头加入var wc = require('../../src/wcache.js')。
3. var s=wc.get('k', '你好')、wc.put('k', 'string你好啊')等;

源码解释见：https://juejin.im/post/591af94b2f301e006bc61687<br>


