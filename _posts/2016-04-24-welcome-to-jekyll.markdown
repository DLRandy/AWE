---
layout: post
title:  "Welcome to Jekyll!"
date:   2016-04-24 12:15:00 +0800
categories: jekyll update
---
下载并安装ruby，fix SSL问题，添加修改淘宝RubyGems镜像。剩下的就是按着jekyll官网上的走就可以了。

{% highlight ruby %}
1fix SSL问题（淘宝镜像只支持HTTPS格式的协议了，so）
这个原因可能会导致下面的错误：
ERROR: While executing gem ... (Gem::RemoteFetcher::FetchError)
    SSL_connect returned=1 errno=0 state=SSLv3 read server certificate B: certificate verify failed (https://api.rubygems.org/specs.4.8.gz)
解决的办法就是添加一个SSL_CERT_FILE的系统变量，路径是/path/to/cacert.pem,这个文件的内容可以在这个网址上随意的复制一个[cacert.pem](https://curl.haxx.se/ca/cacert.pem)
2添加添加淘宝镜像
$ gem sources --add https://ruby.taobao.org/ --remove https://rubygems.org/
$ gem sources -l
*** CURRENT SOURCES ***
https://ruby.taobao.org
{% endhighlight %}

[reference-1ink1](http://ayulin.net/blog/2015/jekyll-3-beta-on-windows/)
[reference-1ink2](https://ruby.taobao.org/)
[reference-link3](https://help.github.com/articles/creating-project-pages-manually/)


















