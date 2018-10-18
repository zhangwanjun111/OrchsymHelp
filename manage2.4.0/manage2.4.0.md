# 管理平台使用说明2.4.0
## 1 API管理
### 1.1 登陆
进入数聚蜂巢API Manager登陆页面，输入登陆邮箱和密码，点击【登陆】，进入平台。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image.png)

注意：每个账户仅允许5次登陆信息错误输入，5次全部输入错误后，账户将被锁定，锁定时间为1小时，1小时后账号才可自动解除锁定，用户可再次尝试登陆。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%201.png)

### 1.2 创建项目
登陆后在左侧导航栏中选择【API管理】-【项目管理】。进入项目列表页面，在项目列表页面可以创建项目和查看已有的项目。

创建一个新项目步骤如下：

第一步，点击【创建项目】。

第二步，在弹窗中填写“项目名称”，“描述信息”。

第三步，填写项目基础域名。数聚蜂巢API Manager平台部署成功后，系统会有一个默认的IP地址。项目基础域名系统默认为服务器IP地址+路径的形式，同时也支持采用域名创建，但是注意使用域名方式创建项目时需将该域名解析到服务器的IP地址。

第四步，选择项目类型。项目分为普通项目和透明代理项目两类。在普通项目主要完成对API的管理，用户可以在普通项目中创建和管理API。透明代理项目主要完成对路由的管理，用户可以在透明代理项目中创建路由，系统会将包含路径信息的域名透明代理到后端地址。

下面以普通项目为例，完成上述项目信息填写，点击【创建】，完成项目创建。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%202.png)


### 1.3 查看项目
完成项目创建后，在项目列表中可以查看刚刚创建的项目。在项目列表页面可以看到账号下的所有项目，以及每个项目的类型、项目内API数量（透明代理类项目不显示路由数）、最近更新时间、描述等信息。

点击【文档】>>至文档/测试页面查看该项目的文档。

点击【删除】可以删除该项目，注意删除该项目后，项目内的所有API也将被同时删除，只有在项目内所有API均处于下线状态时，才能完成删除操作。     

点击项目名称或【编辑】，进入该项目管理页面。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%203.png)


### 1.4 项目管理
进入项目基本信息页面，用户可以对项目基本信息进行查看和修改，以及管理该项目下所有的API。

1、项目基本信息

用户可以在此修改项目名称、协议方式、修改基础URL路径和项目描述信息等基本信息，修改完后点击【保存】完成修改。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%204.png)

2、调用者绑定

调用者绑定功能，绑定调用者后，在项目不允许匿名访问时，该项目将仅对绑定的调用者开放权限。绑定方法：点击调用者绑定输入框，会出现下拉列表，列表中时已经添加的调用者，可以点选进行绑定，若想添加调用者，点击【新建调用者】>>至权限管理／调用者编辑页面进行添加。

允许匿名访问功能，开启允许匿名访问将开放项目权限，任意调用者均有权限调用该项目下所有API。

访问频次限制功能，用于设置单位时间内该项目内API可被调用次数，用户可以手动输入或选择相应数值，注意在设置时应保证访问频次数值的合理性。

访问IP限制功能，用于设置访问IP黑/白名单。IP黑/白名单支持子网掩码，例如：192.168.1.1/24

完成上述各项功能设置后，点击【保存】完成设置。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%205.png)

3、API列表

若项目类型为普通项目，可以在项目页面的API列表中看查看该项目下所有的API情况；若项目类型为透明代理项目，API列表位置显示为路由列表，显示项目内所有路由接口。以普通项目为例：

API分组功能，点击【添加分组】，在弹出窗口中填写“分组名称”和“描述信息”，点击【创建】，完成分组创建。新建项目若不添加分组，则该项目内的API将存放于默认分组中。若想删除分组，只需点击分组右侧【删除】即可。注意，删除分组要保证组内API均处于下线状态，若该分组内有未下线API，则无法删除。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%206.png)

项目内所有分组默认为收起状态，仅显示分组名称、描述信息、和分组内API数量。点击分组栏展开查看分组内API信息

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%207.png)

添加API功能，想要新建API，点击【添加API】，选择新建API的类型（A2A/D2A）>>跳转至相应的API生成页面。具体操作方法，请查看A2A和D2A说明文档。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%208.png)

移动API功能，API可以任意移动到项目内所有分组或选择移动到其他项目下的分组中。选择要移动的API，鼠标移至【移动到】，在下拉列表中选择要移动的目标项目/目标分组，即完成移动。注意，当项目内仅有一个默认分组时，
仅支持将选择API移动到其他项目。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%209.png)

批量删除功能，选择要删除的API，点击【批量删除】，弹窗确定后即可完成批量删除操作。注意，上线状态API必须做下线处理后才能删除。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2010.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2011.png)

查看API功能，API列表提供每个API上下线，文档/测试页面接口，编辑页面接口和删除功能。

点击【上/下线】可对该API进行上/下线操作。

点击【文档】>>跳转至文档/测试页面，可以下载相应API文档，并对API进行功能测试。

点击【编辑】>>跳转至API编辑页面，可以对API进行编辑修改。

点击【删除】，可以对下线状态API进行删除。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2012.png)

4、路由列表

与普通项目不同的是，透明代理项目中API列表位置显示路由列表，点开透明代理项目可以查看该项目下路由设置情况。在路由列表，可以查看每一条路由的路由名称、后端地址、请求路径、请求方法、超时时间等基本信息，还可以完成路由的上/下线操作。

点击【编辑】，可以在弹出页面对路由信息进行修改。

点击【删除】，可以对下线状态路由进行删除。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2013.png)

点击【添加路由】，在弹出窗口中填写路由名称、描述信息、后端地址、请求路径、点选允许请求方法、设置超时时间、选择上线模式等信息后，点击【创建】，完成一条路由的新建。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2014.png)

## 2 数据统计
在左侧导航栏中选择【API管理】-【数据统计】，进入数据统计页面。在数据统计页面，用户可以查看所有API的调用情况。统计维度包括请求次数、访问情况、响应时间、状态码分布、流量、Qps、访问排行的数据统计信息。进入页面，默认显示当日访问量、最近7天访问量和日平均访问量信息。 数据统计信息支持通过项目/API后端、选择API、时间范围等条件来进行针对灵活查看。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2015.png)

支持选择项目/API后端维度查看API调用情况。选择项目维度，将显示这个项目下所有API的统计数据，也可以选择项目内任一API进行查看。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2016.png)

选择API后端，可以查看由该后端生成的所有API，后端概念详见A2A产品使用说明。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2017.png)

数据统计提供分钟/小时/日/周/月等查询颗粒度，根据所选时间段，系统会自动显示可支持查看的信息维度。数据统计提供请求次数、QPS、响应时间、流量、状态码分布、访问排行等维度统计信息。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2018.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2019.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2020.png)

数据统计页面同时提供报表下载功能，选择要查看项目、API、时间范围，点击报表下载，即可下载相关数据Excel文档。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2021.png)

## 3 权限控制
### 3.1 调用者管理
在左侧导航栏中选择【API管理】-【权限管理】，进入权限管理页面。在权限管理页面，用户可以对现有调用者权限进行更改，也可以增加新的调用者。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2022.png)

    点击【添加调用者】>>调用者新增页面。

    步骤一：描述信息。

    填写调用者名称、描述信息。


![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2023.png)

    步骤二：选择认证方式。

    用户可以选择Basic认证/ApiKey认证两种方式。Basic认证需填写用户名和密码。ApiKey认证方式，点击【重新生成】，可生成新的ApiKey。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2024.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2025.png)

    步骤三：设置授权有效期。

    可以设置调用者权限的有效期，支持长期有效，同时支持设置任意时间范围的权限设置。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2026.png)

    步骤四：读写控制。

    选择允许读写/只允许读，设定该调用者的读写权限。

    步骤五：访问频次限制。

    开启访问频次限制，可以限制该调用者在单位时间内的访问数量。用户只需将单位时间内可调用频次数值输入即可。

    步骤六：访问IP限制。

    开启访问IP限制，可以设定该调用者访问的黑/白名单。将IP地址按行隔开输入即可。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2027.png)

上述步骤完成后，点击【提交】，即完成新增调用者。若用户想要编辑现有调用者权限，只需点击编辑该调用者，按照上述步骤完成编辑，点击【提交】即可。


### 3.2 项目/API授权
在项目基本信息页面，点击调用者绑定，即可将添加调用者信息，授权调用者可以调用项目内的所有API的权限。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2028.png)

在项目内API列表中，可以设置单个API的授权，点击【授权】，即可选择需要开放该API权限的调用者进行绑定，点击【确定】保存成功。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2029.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2030.png)

绑定成功后，该API显示已授权。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2031.png)

注意，如果某个API已被授权，则遵循此API的授权方式进行访问。如果某个API未被授权，则继承此API所属项目的授权方式。

## 4 告警管理
### 4.1 告警列表
在左侧导航栏中选择【API管理】-【告警管理】，进入告警管理页面，默认按时间先后展示所有项目最近的告警信息。用户可以通过时间、项目以及故障邮件中的故障ID等信息快速查看告警信息。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2032.png)

### 4.2  告警统计
在菜单中选择【告警管理】-【告警统计】，可以查看最近的告警趋势图，以及告警数量和告警方式，并可以选择时间和项目进行针对性查看。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2033.png)

### 4.3 策略管理
在菜单中选择【告警管理】-【策略管理】，可以看到已经添加的告警策略，包括每条策略的开关、策略名称、策略应用项目、负责人、描述和时间信息。

点击【编辑】>>进入策略编辑页面，可以对该条告警策略进行修改。

点击【删除】，可以删除关闭状态的告警策略。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2034.png)

点击【添加策略】>>进入策略添加页面。用户可以在此页面输入策略信息，进行告警策略新增。依次填写告警策略名称和描述信息、选择策略详情、绑定策略应用项目和告警通知人员、还可以对勿扰时段进行设置，在勿扰时段内绑定人员不会收到告警通知。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2035.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2036.png)


### 4.4 人员管理
在菜单中选择【告警管理】-【人员管理】，可以查看、添加和删除告警通知人。注意，只有在解除绑定后才可以进行人员删除操作。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2037.png)
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2038.png)

## 5 文档/测试中心
在文档/测试中心，客户可以下载项目API文档，并且在文档中心可以对API进行功能测试。进入文档中心/API测试页面方式：

1、在左侧导航栏中选择【API管理】-【项目管理】>>进入项目列表，点击某一项目【文档】按钮>>跳转该项目文档中心/测试页面。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2039.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2040.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2041.png)

2、进入项目详细信息页面，在项目内API列表中，点击下入中任意API【文档】按钮，即可跳转该API所属项目的文档中心页面。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2042.png)

3、在A2A和D2A生成平台，点击进入项目后，点击某一API的【文档】按钮，即跳转该API所属项目的文档中心页面。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2043.png)

进入文档/测试中心后，可以对项目内API进行测试。如下图所示：

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2044.png)

上图中返回200表示API调用成功。

注：若测试返回code 401时，说明调用者没有该项目内API调用权限，输入鉴权信息APIkey/basic认证方式，即可正常调用，或是在管理平台项目基本信息处开通项目匿名访问功能，即可正常测试API功能。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2045.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2046.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2047.png)

## 6 集成管理

集成管理主要用来管理和查看集成部署服务器和Runtime实例情况。包括服务器的启停、日志和事件查询等功能。

### 6.1 应用列表
在左侧导航栏中选择【集成管理】-【应用列表】，进入应用列表页面。应用列表页面可以查看应用实例运行情况，包括实例的ID、应用名称、状态信息。点击【启用/停用】可以完成对应用的起停操作。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2048.png)

点击【查看日志】可以查看每个应用实例的运行日志。可以通过时间、级别、关键字进行筛选，快速找到要查询的日志。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2049.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2050.png)

### 6.2 节点列表
在左侧导航栏中选择【集成管理】-【节点列表】，进入部署服务器节点列表页面。在节点列表页面，可以查看每一个服务器节点运行情况。节点列表包含服务器ID、实例角色、启动时间和状态信息。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2051.png)

点击【查看事件】可以查看每一个节点的运行事件。同样支持通过时间、级别、关键字来快速查询。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2052.png)

## 7 使用文档

平台提供在线使用文档查看功能。在任意页面点击右上角点击【使用文档】按钮，即可在线查看产品使用文档。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2053.png)

## 8 操作记录

平台提供查看操作记录功能，在任意页面点击右上角【操作记录】按钮，即可查看所有操作记录。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2054.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2055.png)

## 9 用户管理
目前平台账号角色类型有两类：管理员账户和普通用户账户。平台对于管理员账户提供用户管理功能，可以进行添加/删除账号、账号信息编辑、账号修改密码等功能。普通用户账户无用户管理功能。对于管理员账户，任意页面点击右上角【用户管理】按钮可以进入用户管理页面。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2056.png)

点击【添加账号】，在弹出窗口中填入相关信息即可完成账号添加。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2057.png)

在用户管理页面点击某一账号的【编辑】按钮可以对已有账号信息进行编辑修改。输入相关信息后，点击【确定】即可保存修改。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2058.png)

在用户管理页面点击某一账号【修改密码】按钮可以修改该账号的密码。输入新密码后，点击【确定】完成密码修改。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2059.png)

在用户管理页面点击【删除】按钮，弹窗确认后，即可完成账号删除。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2060.png)

## 10 修改密码
平台提供修改密码功能。任意页面点击页面右上角登陆名，点击【修改密码】在弹出窗口中输入相关信息，点击【确定】即可完成密码修改。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2061.png)

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/manage2.4.0/image%2062.png)

