---
title: CAJ 转 PDF
tags:
  - Misc
---

CAJ 是中国知网（CNKI）独创的文献格式，必须使用 CNKI 自己的客户端 CAJViewer（仅支持 Windows）才能打开。为了支持多平台，所以将 CAJ 文件格式转换为 PDF 格式。

## 代码转换

```sh
# 获取开源工具
$ git@github.com:JeziL/caj2pdf.git && cd caj2pdf

# 安装依赖
$ pip install pypdf2
$ sudo apt-get install mupdf mupdf-tools

# 转换
$ ./caj2pdf convert paper.caj -o paper.pdf
```

## 浏览器插件

1. 浏览器安装 Greasemonkey 插件
2. 下载 Greasemonkey 用户脚本并拖拽到浏览器：
   * [CNKI 中国知网 PDF 全文下载（普通版）](https://greasyfork.org/zh-CN/scripts/18841-cnki-%E4%B8%AD%E5%9B%BD%E7%9F%A5%E7%BD%91-pdf-%E5%85%A8%E6%96%87%E4%B8%8B%E8%BD%BD)
   * [CNKI 中国知网 PDF 全文下载（特制版）](https://greasyfork.org/zh-CN/scripts/18842-cnki-%E4%B8%AD%E5%9B%BD%E7%9F%A5%E7%BD%91-pdf-%E5%85%A8%E6%96%87%E4%B8%8B%E8%BD%BD-%E7%89%B9%E5%88%B6%E7%89%88)
   * [CNKI 中国知网自动导出 EndNote 格式题录](https://greasyfork.org/zh-CN/scripts/18828-cnki-%E4%B8%AD%E5%9B%BD%E7%9F%A5%E7%BD%91%E8%87%AA%E5%8A%A8%E5%AF%BC%E5%87%BA-endnote-%E6%A0%BC%E5%BC%8F%E9%A2%98%E5%BD%95)
3. 论文详情页面会增加 `「PDF下载」` 按钮（普通版）

![CAJ 按钮](/assets/img/post/caj/caj-button.png)

## 参考

* [github.com/JeziL/caj2pdf](https://github.com/JeziL/caj2pdf)
* [CNKI PDF 全文下载用户脚本](https://blog.csdn.net/VVBBBBB/article/details/51908785)
