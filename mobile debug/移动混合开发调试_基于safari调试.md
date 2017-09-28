# 使用safari调试iphone上的Hybrid App
`注意：该调试方案无需借助XCode`
调试分两大类
* `Xcode模拟器+Safari调试`
* `iphone+Safari调试`
 
有Xcode环境的同学可以看看[《基于XCode模拟器调试JavaScript.docx》](https://github.com/lebra/lebra-docs/blob/master/mobile%20debug/%E5%9F%BA%E4%BA%8EXCode%E6%A8%A1%E6%8B%9F%E5%99%A8%E8%B0%83%E8%AF%95JavaScript.docx)
这里我们讲解一下使用真机iphone＋safari对混合（Hybrid）开发的调试方案。

### 调试前环境准备
1. 拥有自己对Apple开发者账号及开发者证书（即Development证书）
1. Mac及safari浏览器（随OSX自带的即可）
1. 真机（iphone）一台
1. 真迹数据线，用于连接真机和Mac

### 调试过程
基于safari对真机调试过程大致分为如下步骤：
              
1. 制作自己的证书
1. 上传自己的证书至打包服务器
1. 使用自己的证书对代码工程进行云打包
1. 安装打包好的app至iphone
1. iphone连接mac，使用safari进行调试

### 开发者账号和证书的说明
一个开发团队（组织或个人）应有自己的开发者账号和开发者证书。证书分为Development和Production证书，前者用于开发调试等，后者用于正式发布app并上架AppStore使用。                 
`有人要问为什么需要有自己的账号和证书？`                     
一句话，这就是App开发规范，这也保证了你的团队（或个人）开发出来的app能上架AppStore并仅仅属于你的资产。                            
关于开发者账号和证书建议你先看看[这篇文章](http://www.jianshu.com/p/01e2b977f177)                 
`注意，调试的时候必须使用开发者证书（即Development证书）`
    
### 如何制作证书及上传证书
    
如何制作证书参看[这里](http://mobile.yyuap.com/UAPMobile/new/static/instruction.html?cid=18&url=2c948d0858947d5c01589aa78aea000c.md)                   

iuapmobile云编译及证书上传参看[这里](http://mobile.yyuap.com/UAPMobile/new/static/instruction.html?cid=18&url=2c948d0857f959960157f9647c170002.md)   
        
### 真机调试
#### 先说一下真机调试的坑（特别注意）
只有使用自己的开发者证书打出来打app，安装到手机后，才可以借助safari进行调试。    
这里需要说明的是：    
mac上的safari的版本和手机iphone的ios版本是有关系的，具体的这里就不详细赘述了，总之一句话，不要让mac上的safari版本和iphone上的ios版本差的太大，例如iPhone的ios版本为`11.x.x`，mac上safari版本为`9.0.x`，亲测就不行，safari在［开发］找不到iphone，无法调试，但是iphone的ios为`10.x.x`或`9.x.x`的话，就可以正常调试。

#### 真机调试的具体步骤
1. `safari打开开发功能`    
打开Safari偏好设置，选中“高级菜单“，在页面最下方看到“在菜单中显示开发菜单”的复选框，在复选框内打钩，这样设置完毕就能在Safari菜单中看到开发菜单了
1. `iphone开启调试`    
打开手机进入设置->Safari->高级（最下面）->Web检查器打开，JavaScript开关打开
1. `iphone连接mac使用safari调试`
iphone数据线连到mac上，打开safari浏览器，运行手机app到要调试到要调试到页面，在safari开发菜单中选择连接的iphone，找到调试的网页，点击就能在safari里面调试了。

其实，真机调试的具体步骤，网上还是有不少文章的。不清楚的可以看看下面这些链接:         
* [safari调试iPhone app web页面](http://www.jianshu.com/p/30de92fa0d0d)
* [利用Safari调试APP WebView界面](http://blog.csdn.net/u010046748/article/details/52981074)   



