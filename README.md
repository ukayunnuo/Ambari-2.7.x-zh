# Ambari-ZH

当前Ambari的汉化版本为2.7.4,汉化采用对该版本的ambari源码直接修改的方式进行,如有翻译不当之处,请批评指正

## 一、使用方法如下：

### 方式一：直接下载

#### 下载地址：[https://github.com/ukayunnuo/Ambari-2.7.x-zh/releases/download/V1.0.0/public.tar](https://github.com/ukayunnuo/Ambari-2.7.x-zh/releases/download/V1.0.0/public.tar)

#### 国内-下载地址： [https://gitee.com/linyunnuo/Ambari-2.7.x-zh/releases/download/V1.0.0/public.tar](https://gitee.com/linyunnuo/Ambari-2.7.x-zh/releases/download/V1.0.0/public.tar)

###  方式二、ambari-web 构建编译方法

`message.js` 因为ambari的前端是一个纯前端的工程，所以如果你要是想使用的话需要重新编译这个包去使用，在`ambari-web`上
`brunch build`即可，然后把生成`public`文件夹覆盖到`ambari-server`的`/usr/lib/ambari-server/web`目录即可。

查看`ambari-web`的工程目录可以知道，这是一个基于`nodsjs`的工程

运行环境：

- `nvm` 0.39.3（可选）
- `nodejs` 16.20.2
- `npm` 8.19.2
- `brunch` 1.7.10

```bash
# 进入工程目录
cd ambari-web

# 安装指定版本 nodejs
nvm install 16.20.2

# 设置国内加速 如果安装了nrm的可以使用nrm来进行加速
npm config set registry https://registry.npmmirror.com/

# 安装 brunch
npm install -g brunch@1.7
# 构建
brunch build

```

进行打包 生成的 `public` 文件夹， 进行 替换服务器上的 `/usr/lib/ambari-server/web` 即可，替换完成后重新刷新页面即可。



