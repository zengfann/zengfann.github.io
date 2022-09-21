# :orange: ZengFan Blog<br>
[![Build Status](https://github.com/cotes2020/jekyll-theme-chirpy/workflows/build/badge.svg?branch=master&event=push)](https://github.com/cotes2020/jekyll-theme-chirpy/actions?query=branch%3Amaster+event%3Apush)
[![GitHub license](https://img.shields.io/github/license/cotes2020/jekyll-theme-chirpy.svg)](https://github.com/cotes2020/jekyll-theme-chirpy/blob/master/LICENSE)
[![996.icu](https://img.shields.io/badge/link-996.icu-%23FF4D5B.svg)](https://996.icu)

一个关于Jekyll 主题的的个人Blog,采用的是响应式设计，方便记录、管理、分享你的学习知识与生活乐趣。

## :book:目录
  - [功能一览](#功能一览)
  - [安装](#安装)
  - [使用](#使用)
  - [经验](#经验)
  - [感谢](#感谢)
  - [许可认证书](#许可认证书)

## :cloud:功能一览
- 文章发布
- 文章目录
- 可配置全局主题颜色
- 分享生活记录(在做)
- Disqus评论
## 安装
[Fork **Fan_Blog**](https://github.com/zengfann/zengfann.github.io/fork)把仓库名称改成`USERNAME.github`(!一定和你github用户名一致可实现github pages),然后克隆到本地：
```terminal
$ git clone https://github.com/USERNAME/USERNAME.github.io.git -b master --single-branch
```
### 配置本地环境
若在本地构建运行，参考][Jekyll Doc](https://jekyllrb.com/docs/installation)安装`Ruby`、`RubyGem`、`Bundler` MacOS还需要安装[GNU coreutils](https://www.gnu.org/software/coreutils):
- macos
```console
$ brew install coreutils
```

在文件下打开PowerShell：<br>
进入文件主目录`cd USERNAME.github.io`,然后下载Jeklly `gem install jekyll-paginate`
```terminal
$ Bundle install
```
`bundle`会自动下载安装Gemfile中指定的依赖插件

## :sunny:使用
:warning:严格按照下列说明去运行或部署项目
### 初始化
在项目根目录，开始初始化：
```terminal
$ bundle exec jekyll build
```
### 配置文件  
根据个人需求修改`_config.yml`文件的变量,典型的选项是： 

- `url`  
- `comment`  
- `createror`
### 本地运行
```terminal
$ bundle exec jekyll serve
```
访问本地服务:    <http://localhost:4000>  
如果想在本地服务运行之后,修改源文件之后及时刷新服务，需要安装依赖[**fswatch**](http://emcrisotomo.github.io/fseatch)

### 部署  
部署开始前，把  `_config.yml` 的 `url` 改为 `https://<username>.github.io`(或者你的私有域名，如：`https://yourdomain.com`)。另外，如果你想使用 [Project 类型网站](https://help.github.com/en/github/working-with-github-pages/about-github-pages#types-of-github-pages-sites)，修改配置文件的 `baseurl` 为项目名称，以斜杠开头，如：`/project`

### 部署到Github pages  
1. 根据初始修改的`USERNAME.github.io`仓库名，根据Github指示的地址去访问你的网站
2. Github Pages build 在`safe`模式下运行，则导致存在的依赖生成额外的页面文件。因此可以使用`GitHub Actions`来构建站点，将构建的站点文件存储在新分支上，作为服务Github Pages服务的源。
3. 检查Github Actions构建所需文件：
  - 确保您的 Jekyll 站点具有该文件.github/workflows/pages-deploy.yml。否则，创建一个新的并填写示例文件的内容，其值`on.push.branches`应与您的 repo 的默认分支名称相同
  - 确保您的 Jekyll 站点有文件tools/deploy.sh. 否则，将其从此处复制到您的 Jekyll 站点。
  - 此外，如果您已提交Gemfile.lock到 repo，并且您的运行时系统不是 Linux，请不要忘记更新锁定文件中的平台列表：
  
     ` bundle lock --add-platform x86_64-linux`

4. 将任何提交推送到远程以触发 GitHub Actions 工作流程。构建完成并成功后，将出现一个名为的新远程分支gh-pages来存储构建的站点文件。
5. 浏览到您在 GitHub 上的存储库。选择选项卡Settings，然后点击左侧导航栏中的Pages，然后在GitHub Pages的Source部分中，选择branch 的目录作为发布源。离开前记得点击。`/(root)gh-pagesSave` 
   
   ![avatar](/assets/images/gh-pages-sources.png)
6. 注意每次修改源文件需要`$ jekyll build` 再推送到github仓库，才可实现网站的刷新服务
### 部署到阿里云服务器
```
暂时还未实现
```
## :ship:经验
1. Fork 项目仓库的名字必须是你Github的`USERNAME`
2. 会出现`webrick` 缺少情况,输入`$ bundle add webrick` 
3. `bundle install`中Gemfile存在下载缓慢情况(由于:door:的问题)，可以通过开相关代理或者设置TB镜像下载
4. Disqus 相关配置以及网站服务申请参考[ Disqus 的坑](https://demonkoo.github.io/2016/09/22/Setting-Disqus-Post-New/)  
5. Disqus 中的 Web site 必须是`http://USERNAME.github.io`,不可是`https`
6. Disqus 中还需要将个人网站加入到 Home->Your site->configtion->Advance 加入到`Trusted Domains`  

## 感谢
:fire:本博客是基于[Von-Jkeyll](https://onevcat.com)与[maoyachen](https://maoyachen.com)的修改,感谢！:heart:
## 许可认证书
本项目开源，基于[MIT](https://github.com/zengfann/zengfann.github.io/blob/master/LICENSE) 许可。
   
