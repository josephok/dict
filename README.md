# dict
bash版在线查单词

# 前言

看了[nodejs版本][1]的在线查单词程序，受到点启发，于是想写个bash版的在线查单词脚本`dict`。

效果如下：
![dict][2]

# 实现

这个脚本用到了2个api：有道翻译api和爱词霸api，通过jq去解析返回的内容。分别输出这两个网站的翻译。

# 安装：

## 安装jq
这个脚本依赖jq，jq是解析json的一个工具。
安装：
```bash
$ sudo apt install -y jq
```

## 安装xml2json
xml2json是将xml转换为json的工具，因为爱词霸的api返回是xml格式，而xml格式不好处理，于是用这个工具将其转换为json格式，然后用jq去处理。

```bash
$ sudo npm install -g xml2json-command
```

## 安装dict

直接下载到本地，然后拷贝到你的$PATH路径目录下，比如~/bin，就可以执行了。

# 使用

```
$ dict [要查询的单词]
```


  [1]: https://github.com/afc163/fanyi
  [2]: https://sfault-image.b0.upaiyun.com/398/279/3982794784-57c43256e15e5_articlex
