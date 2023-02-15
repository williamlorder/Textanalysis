# Text analysis

把爬虫项目放到这个仓库里然后`push`上来

## weibo-search，

> 在https://github.com/dataabc/weiboSpider 基础上添加了300多个事件的关键词keyword.txt,可以对这些事件进行爬取，能不能完善表格内容，但感觉数据一般，效用不大。

Answer: 的确，你爬取了吗？效果怎么样，可以把拿到的数据集传上来吗。同时我没有看到你的`weibo-search`内容哦。你好像并没有Push上来哎。

## baidu-search

> https://github.com/BaiduSpider/BaiduSpider, 这个遇到的问题是他的结果展现不出来，不太理解只有一个`<object WebResult>`，是漏看了什么还是？

Answer: 现在结果怎么样了。你看那个教程里面提到了拿百度搜索的\[cookie\](https://baiduspider.github.io/guide/index.html)，你看能不能配置了cookie再进行获取。不行的话我试试看.

``` python
from baiduspider import BaiduSpider

# 在实例化BaiduSpider对象时传入cookie
spider = BaiduSpider(cookie="你的cookie")
```

他获取的对象似乎是一个`dict`。你可以用下面的函数遍历一下前几行，看看数据结构是怎么样的：

``` python
for key, value in list(my_dict.items())[:3]:
    print(key, value)
```