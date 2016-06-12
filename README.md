###准备
请确定已经安装nodejs及npm,且电脑上有ruby环境,gem命令能够正常使用.

请先运行命令:`npm install`安装依赖.

安装jekyll静态站点生成器:
```
gem install jekyll
```
###关于gem源被墙的问题:
- 下载安装Jekyll `坑：国内的镜像不能用，淘宝的镜像也不行了。`
```
$ gem sources -a http://ruby.taobao.org/
Error fetching http://ruby.taobao.org/:
        bad response Not Found 404 (http://ruby.taobao.org/specs.4.8.gz)

```
####解决方法：[Ruby China 的 RubyGems 镜像上线](https://ruby-china.org/topics/29250)

```

gem sources -a https://gems.ruby-china.org/

```

####添加成功后：
```


$  gem sources -l

*** CURRENT SOURCES ***

https://gems.ruby-china.org/

```

###使用

运行`npm watch`会监控less文件改动,自动编译.
修改less目录下的theme.less文件，添加或修改变量的值，该文件的变量将直接覆盖variable.less里面的变量的值。

运行`npm start`,即可打开`127.0.0.1:4000`查看效果,且文件发生变动自动刷新（貌似不会）.


### 发布

运行`npm run deploy`对less编译

### 发布到gh-pages

运行`npm run gh-pages`