# baidu-rank

查询网页在指定关键词上的百度排名。

http://npm.taobao.org/package/baidu-rank

## 安装

```
$ npm install baidu-rank
```
npm有时候会崩，一般用cnpm

- 说明：因为npm安装插件是从国外服务器下载，受网络影响大，可能出现异常，如果npm的服务器在中国就好了，所以我们乐于分享的淘宝团队干了这事。来自官网：“这是一个完整 npmjs.org 镜像，你可以用此代替官方版本(只读)，同步频率目前为 10分钟 一次以保证尽量与官方服务同步。”

- 注意：安装完后最好查看其版本号cnpm -v或关闭命令提示符重新打开，安装完直接使用有可能会出现错误 

https://blog.csdn.net/shelly1072/article/details/51524029

```
npm install cnpm -g --registry=https://registry.npm.taobao.org
```

## 使用

下面的代码用来查询网页`http://xc.hubwiz.com/course/597d463fff52d0da7e3e397a`
在[vuex](http://xc.hubwiz.com/course/597d463fff52d0da7e3e397a)
关键字上的排名，查询范围为百度搜索结果页1~76：

```
var baiduRank = require('baidu-rank')

var url = 'http://xc.hubwiz.com/course/597d463fff52d0da7e3e397a'
var word = 'vuex'
var start = 1
var end = 76

baiduRank(url,word,start,end)
  .then(ret => console.log(ret))
```

输入结果类似如下：

```
=> vuex
[{
  word: 'vuex',
  url: 'http://xc.hubwiz.com/course/597d463fff52d0da7e3e397a',
  rank: 27
}]
```

## 感谢

- [汇智网](http://www.hubwiz.com)
