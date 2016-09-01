# Cocoa-pods-
Cocoa pods的安装及使用 ，步骤详解

## 一. 使用rvm 更新 ruby 
# 1.先查看当前的版本
     ruby -v 
#2.查看能使用的ruby版本 ruby 
    rvm list known
#3.  使用rvm 更新ruby 
    http://blog.csdn.net/lissdy/article/details/9191351

备注：
#1.    终端输入如下命令（把Ruby镜像指向taobao，避免被墙，你懂得）
    gem sources --remove https://rubygems.org/ 
    gem sources -a http://rubygems-china.oss.aliyuncs.com
    gem sources -l （用来检查使用替换镜像位置成功）)
#2. 报错 
    1.Requirements installation failed with status: 1. 
      解决方法 ：敲命令： rvm autolibs disable   
    （原文链接：http://619060342.iteye.com/blog/2185070）
   


##二. 安装cocoa pods
        敲命令： sudo gem install cocoapods

备注：
     报错:       While executing gem ... (Gem::Exception)
    Unable to require openssl, install OpenSSL and rebuild ruby (preferred) or use non-HTTPS sources 
       
      解决：
             openssl 的问题 是 镜像的问题 HTTPS的问题 ,修改淘宝镜像的地址


  
##三. pod search 需要安装的第三方框架  
    出现 Setting up CocoaPods master repo 然后之后一直等

    有可能会报错：
Cloning into '/var/folders/3p/8jgv231s1tbd_hm4ck0mh8s00000gn/T/d20160826-1452-1v3cmbr'...
error: RPC failed; curl 56 SSLRead() return error -9806
fatal: The remote end hung up unexpectedly
fatal: early EOF
fatal: unpack-objects failed
    解决方法：
    http://wenku.baidu.com/link?url=oUqwQqwkquuANPxwaxN78xfGBEhakoRWtsb8TmK4RGIldwsZzuC2uVxFi200oinRQqwU0zGGiqhi8sALme2oA0mAXvTCvlCcUydfCyF27UK




##四.  使用cocoa pods 
#1..   cd 项目目录
#2..   pod init  // 创建profile文件
#3..   pod search 需要安装的第三方框架
#4..   pod install --no-repo-update    // 第一次安装的时候是用install 
#5..   pod update --no-repo-update  // 后面再装第三方框架是用update
