# D2A产品使用说明
## 1  创建数据源
创建数据源，即创建一个数据库连接，当需要创建API时，可以直接选择已经创建好的数据源，并选择具体的数据表生成API。
1.1、   在D2A数据源管理页面，点击【新建数据源】按钮。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image.png) 
1.2、   在新建数据源页面，填写数据源名称、描述以及数据库类型、主机、端口号、用户名和密码，然后点击【连接数据库】按钮。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%201.png)
1.3、   连接成功后，在展开的页面中选择数据库，然后点【保存】按钮即可保存该数据源。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%202.png)

## 2  创建API
数聚蜂巢D2A平台支持生成API，可以对数据库表进行增、删、改、查API操作，对于多表支持查看功能，具体详见2.6 多表查询。
### 2.1  GET列表
GET列表，是根据创建时设置的条件，获取数据库中对应表的数据列表。
以单表为例：创建一个获取“产品演示数据库”下“user”数据表内的数据列表。其中“user”表的数据如下图
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/C367DDFD-EBF8-4BBB-9400-B6D610B5181D.png)
2.1.1、 在D2A项目列表页面，选择在API管理平台创建的项目“产品演示项目”。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%203.png)
2.1.2、在选择的项目“产品演示项目”下，点击【新建API】按钮。 
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%204.png)
2.1.3、 在新建API页面，选择创建好的数据源“产品演示数据库”，在展开的页面中选择需要创建API的数据表“user”，然后点击【下一步】按钮。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%205.png)
2.1.4、 在基本设置部分，选择API所属分组，填写API名称、请求方法、请求路径和描述，并选择是否支持翻页以及响应格式。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%206.png)
2.1.5、在选择字段部分，勾选使用API时需要显示的字段，还可以设置它们的显示名称（显示名称是显示时，替换数据表字段的名称，即API成功执行后，数据列表显示的字段名称）。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%207.png)
2.1.6、 在参数定义部分，如果选择了支持翻页，则会自动增加PageNumber和PageSize两个参数，如果选择不支持翻页，则至少需要添加一个参数定义。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%208.png)
2.1.7、 在参数映射部分，如果选择了支持翻页，则可以为空，如果选择不支持翻页，则至少需要映射一个定义好的参数。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%209.png)
2.1.8、 在查询条件（选填）部分，可以添加默认的查询条件，例如添加 `id`>’80’，则查询结果只会显示id>80的部分。设置完成后，可以点击【提交】按钮保存API。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2010.png)
2.1.9、API创建成功之后，可以通过API管理平台的测试功能，验证API功能是否正常。在API管理平台的项目管理页面，找到创建的API所属的项目“产品演示项目”，并点击操作栏的【文档】按钮进入项目的文档中心。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2011.png)
2.1.10、在文档中心找到创建的API，单击展开后，点击【Try it out】进入测试。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2012.png)
2.1.11、在测试页面，填入带*的必填参数，非必填参数可选填，然后点击【Execute】按钮。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2013.png)
2.1.12、测试结果如下图，其中，由于创建时设置了查询条件id>80，所以结果并未显示数据表“user”中的所有数据，只显示了id>80的部门。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/EFD13382-E8D3-4E06-A049-5C3E934E46C3.png)
2.2  GET单条
GET单条，是根据创建时设置的条件，获取数据库中对应表的指定数据。例如：创建一个获取“产品演示数据库“下“user”数据表中id=55的用户。其中“user”表的数据如下图：
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/70223CCC-BEDA-4FC7-9B24-E6B66D944F19.png)
2.2.1、 前三步与创建GET列表的API一致，在基本设置部分，选择API所属分组，填写API名称、请求方法、请求路径和描述，并选择响应格式。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2014.png)
2.2.2、 在选择字段部分，勾选使用API时需要显示的字段，还可以设置它们的显示名称（显示名称是显示时，替换数据表字段的名称，即API成功执行后，数据列表显示的字段名称）。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2015.png)
2.2.3、在参数定义部分，至少需要添加一个参数定义，若请求路径包
含/{xxx}，则参数“xxx“会自动添加。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2016.png)
2.2.4、在参数映射部分，至少需要映射一个定义好的参数。设置完成后，可以点击【提交】按钮保存API。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2017.png)
2.2.5、测试API，在API管理平台的项目管理页面，找到创建的API所属的项目“产品演示项目”，并点击操作栏的【文档】按钮进入项目的文档中心。在文档中心找到创建的API，点击【Try it out】按钮进入测试。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2018.png)
2.2.6、 输入必填参数，点击【Execute】按钮，测试结果如下图。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/284B06C4-7982-4B14-8B2C-AD68FB09CC35.png)
### 2.3  POST添加
POST添加，是根据创建时设置的表单映射，向目标数据表内新增数据。例如：在“产品演示数据库”下的“user”数据表中，添加一个用户(name：刘亦菲，username：liuyifei，password：liuyifei123456，type：0，quanxian：all，statement：当前日期，department_id：12)。其中未添加数据前“user”表的数据如下图：
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/6517E9E3-9557-4171-A23A-833EBE0B612F.png)
2.3.1、前三步与创建GET列表的API一致，在基本设置部分，选择API所属分组，填写API名称、请求方法、请求路径和描述，并选择响应格式。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2019.png)
2.3.2、在表单映射部分，至少添加一个表单映射，其中参数名自定义，映射字段为数据库内的字段，只能选择，且不能重复。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2020.png)
2.3.3、在默认值设置（选填）部分，可以向数据库里添加默认值，分为系统参数和常量两周类型5。设置完成后，可以点击【提交】按钮保存API。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2021.png)
2.3.4、测试API，在API管理平台的项目管理页面，找到创建的API所属的项目“产品演示项目”，并点击操作栏的【文档】按钮进入项目的文档中心。在文档中心找到创建好的API，点击【Try it out】按钮进入测试，输入必填参数，点击【Execute】按钮。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/97EB8988-AFC7-4314-BB43-2F4B4B6A07BD.png)
2.3.5、测试结果如下图
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/C563A922-9F74-4084-8DA9-1928C41A7208.png)
2.3.6、使用创建的API添加数据后，“user”表的数据如下：
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/32D92E68-D489-4C71-9EBD-0FE8DDC2EC56.png)
### 2.4  POST修改
POST修改，是根据创建时设置的参数映射和表单映射，修改目标数据表内指定数据的信息。例如：在“产品演示数据库”下的“user”数据表中，修改id=86的用户信息（name：范冰冰，username：fanbingbing，password：fanbingbing123，type：2，quanxian：2，statement：当前日期，department_id：12）。其中未修改数据前“user”表的数据如下图：
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/434689F4-9CEA-4AE5-BF6C-BECBC7BDC549.png)
2.4.1、 前三步与创建GET列表的API一致，在基本设置部分，选择API所属分组，填写API名称、请求方法、请求路径和描述，并选择响应格式。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2022.png)
2.4.2、在参数定义部分，至少需要添加一个参数定义，若请求路径包含/{xxx}，则参数“xxx“会自动添加。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2023.png)
2.4.3、在参数映射部分，至少需要映射一个定义好的参数。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2024.png)
2.4.4、在表单映射部分，至少添加一个表单映射，其中参数名自定义，映射字段为数据库内的字段，只能选择，且不能重复。设置完成后，可以点击【提交】按钮保存API。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/A44A66B0-AC4F-4D0D-92FA-11F80374D03D.png)
2.4.5、测试API，在API管理平台的项目管理页面，找到创建的API所属的项目“产品演示项目”，并点击操作栏的【文档】按钮进入项目的文档中心。在文档中心找到创建好的API，点击【Try it out】按钮进入测试，输入必填参数，点击【Execute】按钮。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/BD9E1952-3BB6-4A7A-BAF9-5EEE933C0995.png)
2.4.6、测试结果如下图。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/53288551-6014-4CE4-9F69-97883A2AD533.png)
2.4.7、使用创建的API修改数据后，“user”表的数据如下。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/BD8A35B7-F6A3-49B1-A0EB-85DF8ABE0609.png)
2.5  DELETE
    DELETE，是根据创建时设置的参数映射，删除目标数据表内的指定数据。例如：删除“产品演示数据库”下的“user”数据表中id=86的用户。其中未删除数据前“user”表的数据如下图
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/D9F223B4-6D20-496A-9120-3A2E7E4760E0.png)
2.5.1、前三步与创建GET列表的API一致，在基本设置部分，选择API所属分组，填写API名称、请求方法、请求路径和描述，并选择响应格式。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2025.png)
2.5.2、在参数定义和参数映射部分，和GET单条完全一致。设置完成后，可以点击【提交】按钮保存API。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2026.png)
2.5.3、测试API，在API管理平台的项目管理页面，找到创建的API所属的项目“产品演示项目”，并点击操作栏的【文档】按钮进入项目的文档中心。在文档中心找到创建好的API，点击【Try it out】按钮进入测试，输入必填参数，点击【Execute】按钮。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/1B1F99C7-8EAD-41C3-A449-714F4BA8FA03.png)
2.5.4、测试结果如下图。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/832164B5-7688-4D87-9A0F-56B610A6AC6B.png)
2.5.5、使用创建的API删除数据后，“user”表的数据如下。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/96C8867A-36B0-45A7-9F91-07FFCB188F9A.png)
### 2.6  多表查询-GET列表
点击【新建API】->选择数据源后，获取数据库中对应表的数据列表，支持点选多表生成多表查询API。例如：创建一个获取“目录梳理数据库”下，选择部门表（department)和用户表(user)。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2027.png)
选择多表，仅支持对于多表进行GET单条和列表操作，进入基本设置页面，选择分组、请求方法、响应格式、填写API名称、请求路径和描述等信息。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2028.png)
多表查询不同于单表查询可以通过输入SQL语句进行编辑，在模式选择中选择【高级模式】，然后在下面SQL输入框中输入SQL编辑语句即可。可以选择标准模式，系统会自动配置生成SQL语句。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2029.png)
点击【完成】后，进入列表页面，点击【文档】按钮进行测试
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/EABB7538-6D59-4AE5-9CD7-E386167F7E00.png)
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/F15450B0-AE74-4514-8395-F9B7A3668F93.png)
### 2.7  多表查询-GET单条
点击【新建API】->选择数据源后，获取数据库中对应表的数据列表，支持点选多表生成多表查询API。例如：创建一个获取“目录梳理数据库”下，选择部门表（department)和用户表(user)。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2030.png)
选择多表，仅支持对于多表进行GET单条和列表操作，进入基本设置页面，选择分组、请求方法、响应格式、填写API名称、请求路径和
描述等信息。
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2031.png)
 多表查询不同于单表查询可以通过输入SQL语句进行编辑，在模式选择中选择【高级模式】，然后在下面SQL输入框中输入SQL编辑语句即可。可以选择标准模式，系统会自动配置生成SQL语句。
参数定义及编写SQL语句
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2032.png)
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/image%2033.png)
点击【提交】后，进入列表页面，点击【文档】按钮进行测试
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/D08CDC79-B911-45D8-AD40-175AF5DAC489.png)
![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/D2A/857BDDDA-34B2-4A36-AD13-7012E2883238.png)
