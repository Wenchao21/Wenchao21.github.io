---
layout: post
title: How to build the blog
date:   2016-7-12
---


本博客制作流程和原理概要：

 **1. 原理：**
          采用Jekyll框架创建博客，然后部署到github上面。Github上的Gitpage，后台采用的引擎便是Jekyll，所以在本地创建好博客工程后，可以直接往Github上部署，然后单独购买域名，将自己的域名，指向自己的博客，所以你可以直接访问域名，来达到访问博客的目的。
 **2. 名词解释**：
        

 - Jekyll：

 用ruby开发的一个web框架，主要用来生成一些简单的静态web网页，为用户快速打造一个简单的站点，十分轻量级，很简单。
       

 - Github：

 一个用来托管代码的一个host，你可以将你的代码和一些开源项目push上去，github上托管有非常多的开源项目。总之就是一个提供代码托管服务的平台。
       

 - Github Page：

一个免费提供可以部署Jekyll开发的博客项目。后台引擎采用的是Jekkly，所以只要把工程push上去，即可访问自己的网页。
      

 - Markdown：

Markdown格式的文件，你可以当做和word一样的东西，是一种文本书写格式。提供更为优美的书写格式。Jekyll的post采用的就是Markdown格式的文件。
        
 **3. 制作流程：**
 
         

 - **生成本地工程**
   ##### **安装ruby**
   	官网下载和安装ruby，linux一般已经集成ruby，请在终端输入ruby -v以检测ruby的安装,如果显示ruby的版本，则安装成功
	```powershell
      ruby -v
    ```

   #####  **安装Jekyll**
   
   jekyll是一个用ruby编写的web框架，gem是ruby的包管理工具。我们可以使用gem 来安装jekyll。
   ```ruby
   gem install jekyll
   ```
   
   ##### **生成博客**

	安装好jekyll之后，我们就可以使用这个gem来生成我们的博客了。
    
    ```ruby
    jekyll new myblog
    
    cd myblog
    
    jekyll serve
    
    # => 打开浏览器 http://localhost:4000
    ```
     之后，你便可以在本地的访问你的博客了。
     这里是生成的博客的目录结构，你可以在项目中随意更改你需要更改的东西。
     
	
文件/目录	描述
_config.yml	存储配置数据。很多全局的配置或者指令写在这里。
_drafts	存放为发表的文章。这些是没有日期的文件。
_includes	存放一些组件。可以通过{% include file.ext %} 来引用。
_layouts	布局。
_posts	存放写文章，格式化为：YEAR-MONTH-DAY-title.md。
_site	最终生成的博客文件就在这里。
index.html	博客的主页。
other	例如静态文件 CSS，Images 和其他。


     

 - **注册和生成远程仓库**

       

 - **购买自己的域名**

         
         

 - **将域名绑定博客**

 


