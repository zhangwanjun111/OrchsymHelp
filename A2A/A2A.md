# A2A产品使用说明
举例：创建hello world。
以百度搜索为例，创建一个百度搜索的API。

## 1  基本配置
### 1.1、   选择项目，创建API
进入<A2A平台>,在项目列表中选择“产品演示项目”， 点击进入该项目API列表，在此页面可以查看该项目分组情况和已建立的API列表。点击【创建API】按钮创建新的API。（若项目列表中没有所需项目，需进入<API管理平台>创建项目。）

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/image.png)
### 1.2、   输入基本信息
点击【创建API】，进入API“基本信息”页面。填写“请求路径”，“请求方法”，“描述信息”，“选择分组”等API基本信息以及“后端地址”，“请求方法”，“超时时间”等数据源基本信息，填写完毕后点击【下一步】完成，进入“定义输入”页面。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/image%201.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/image%202.png)
### 1.3、   定义输入，完成API创建与上线
在“定义输入”页面-请求参数定义，点击【添加】增加参数及描述信息，点击【跳过高级配置，确认完成】完成API创建及上线。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/image%203.png)
### 1.4、   预览API线上效果 
打开浏览器输入此API地址，即可预览这个API了。需要强调的是：由于没有定义输出格式，所以预览的效果是直接显示HTTP的访问状态，即STATUS OK。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/C32E3E49-31FC-4E8C-A091-ECECDA98E987.png)
在完成上述创建API之后，我们还需要设置后端参数转换及后端输出定义，才可以完全实现构建百度搜索API的工作。
以百度搜索关键词“白山云”为例，我们可以看到URL中的后端参数名为wd。 http://www.baidu.com/s?wd=白山云 ，我们对此接口参数wd的参数位置进行转换，使原来的Querystring转换成Path。

## 2  高级配置
### 2.1、   完成配置后点击【高级配置】进入“后端配置及输入转换”页面。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/image%204.png)
###   2.2、 进入“后端配置及输入转换”页面，填写“后端参数映射”选项。        
点击后端参数映射中的【添加】按钮，在后端参数名处填写wd，然后点击【下一步】按钮，这样就完成了后端参数转换。 

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/image%205.png)
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/image%206.png)
### 2.3、点击【下一步】进入“后端输出及输出转化”页面，定义最终输出格式。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/image%207.png)
点击最终响应Body中的【添加】按钮，选择BODY定义为html（默认的BODY定义中并没有html，请查看后续讲解如何创建通用BODY定义来创建此html），然后点击【完成】按钮，完成创建及上线。
### 2.4、重新复制链接到浏览器输入框内，即可成功访问百度的搜索页面。
我们可以看到这时wd的参数位置发生了变化，由Querystring变成了Path。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/50797B34-2F21-49B5-ABF0-43CA9ED3000D.png)

## 3  创建通用BODY定义
模型管理，可以查看或修改已经添加的模型。点击【添加模型】- “新增模型”页面。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/image%208.png)
填写“body名称”，“描述信息”，选择“body类型”，在输入框中键入body模型详情，点击【保存】添加模型，完成对模型的操作。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2A/image%209.png)
