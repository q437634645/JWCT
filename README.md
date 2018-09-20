# 请注意接下来会对各种文档进行分类，不再写在README.md内
----

# 尽量详细的说明

## git项目仓库的建立

首先登录git，从个人信息除进入Your Repositories。  
找到New，输入相关信息，如项目仓库名字，基本描述，（选择还有公有私有，私有需要缴费)  

## 仓库下文件介绍

### .gitignore

下面还可以选择添加.gitignore文件)，这个文件放在项目仓库根目录下，主要用来说明git使用时的规则，`忽略某些文件`(检查时git工具会无视这些文件的变动)，避免上传这些文件，保持`线上仓库干净`。  
(ps:也可以`手动添加`规则，这里我选了git推荐的java版.gitignore

### LICENSE

LICENSE就是授权用的，告诉别人怎么使用你的公开项目。（暂时没关系-.-）

### <p>README.md</p>

这是现在你正在看的文件，放在项目仓库目录下，主要是因为git网页会使用README.md文件来项目主界面展示信息用，而且使用markdown(`请自行百度，或直接问我`)语法使用,接下里我尽可能把东西都写在这里

## 项目介绍

### 9.14初稿

#### 1、语言

暂定java语言为主

#### 2、功能or需求

##### 2.1概括

可以爬取特定网站的信息，并以文件的形式不做任何修改地保存下来。

具体形式为：启动程序，要求用户输入url，输入后程序开始爬取，最后把爬取到的信息以文件形式保存。

##### 2.2可变的url

可以指定网站url，即可以让用户输入网站地址

##### 2.3爬取网站内可跳转的链接

如果在爬取到的网站内有可以跳转的网站，则要求获取该网站信息，暂定最高跳转3层，即首先输入网站A，爬取A发现可以跳转B，那么继续爬取B，依次类推。  

最终为以输入url为中心，扩散出去3层。（`为了直观，希望能有个图`）

##### 2.4不重复爬取相同的网站url

如果网站A的信息已经获得，那么再一次发现A时应该直接忽略  

#### 3、会使用到的java相关包

[jsoup](https://github.com/jhy/jsoup)  
jsoup是一个html解析器，因为html比较复杂，从其中提取信息，可能会花比较多的时间，所以采取使用现有解析器，回头可以再了解其中细节原理(-.-)。版本使用1.11.3。

[HttpClient](http://hc.apache.org/httpcomponents-client-4.5.x/index.html)  
HttpClient就是在网络中请求信息的核心组件，获取网页就靠它，自己写的话，可能要从字节流开始写，也要了解HTTP协议和计算机网络，所以先直接用这个。版本使用4.5，log表示我也不懂0.0。


`ps:以上两个我也不会用，同时也不会设置开发环境，来一起研究呀。`

[Eclipse](https://www.eclipse.org/)
IDE使用Eclipse，大家都有，省事。


## git使用

### 提交(git commit)
提交时请对提交进行必要的描述(`此处为模糊要求，就是最好写下commit message`)

### 添加协作者
找到对应项目的setting页面，选择Collaborators，然后输入协作者的名字就可以了，协作者需要接受邀请才能完成添加。

## 备注

以上不懂的名词或不清楚的描述`请尽快提问或进行修改`  
