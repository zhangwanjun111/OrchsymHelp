# 新手入门-透明代理使用说明
透明代理项目主要完成对路由的管理，用户可以在透明代理项目中创建路由，系统会自动将包含路径信息的域名透明代理到后端地址。

# 1  创建项目
透明代理项目的创建和普通项目相似，在项目列表页面，点击【创建项目】，填写“项目名称”、“描述信息”、“基础域名”等信息，唯一不同指出在于项目类型选择透明代理，完成上述设置后，点击【创建】完成透明代理项目新建。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/proxy/image.png)

# 2  路由列表
与普通项目不同的是，透明代理项目中API列表位置显示为路由列表，点开透明代理项目可以查看该项目下路由设置情况。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/proxy/image%201.png)
在路由列表，可以查看每一条路由的路由名称、后端地址、请求路径、请求方法、超时时间等基本信息，还可以完成路由的上/下线操作。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/proxy/image%202.png)
点击【编辑】，可以在弹出页面对路由信息进行修改。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/proxy/image%203.png)
点击【删除】，可以对下线状态路由进行删除。
点击【添加路由】，在弹出窗口中填写路由名称、描述信息、后端地址、请求路径、点选允许请求方法、设置超时时间、选择上线模式等信息后，点击【创建】，完成一条路由的新建。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/proxy/image%204.png)
#  3  例子
我们举个例子：现在填写路由信息如下
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/proxy/image%205.png)
根据项目的基础URL信息
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/proxy/image%206.png)
我们现在做一下访问：116.211.107.231/proxy  可以成功访问百度页面，该路
由设置成功。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/proxy/image%207.png)
