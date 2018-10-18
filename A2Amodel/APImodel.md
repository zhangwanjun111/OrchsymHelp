# API适配-模型管理怎么使用？

## 1、什么是模型

模型是对API输入和输出格式的说明，描述HTTP BODY的具体信息, 包括:
* HTTP BODY整体的格式
* 包含的属性
* 每个属性的类型
* 每个属性的取值范围

## 2、如何描述模型

模型遵循 json-schema 以及 swagger 标准，例如：
```
{
    "title": "Example Schema",
    "type": "object",    
    "properties": {
            "firstName": {
                  "type": "string"        
            },        
            "lastName": {
                  "type": "string"        
            },       
            "age": {            
                  "description": "Age in years",           
                  "type": "integer",            
                  "minimum": 0        
                  }    
            },    
    "required": ["firstName", "lastName"]
}
```

以上模型解释:
* 整体为一个对象
* 对象的属性有 firstName lastName age
* age的类型为整形，最小值为0
* firstName lastName 为字符串类型
* firstName lastName为必填项
## 3、如何创建通用模型

1.点击导航栏模型管理下的添加按钮。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2Amodel/image 2.png)

2. 填写body名称、描述，选择类型为其他，然后点击保存按钮，这样就成功创建了通用模型格式——html。

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2Amodel/37530F10-32C3-42FC-8FED-BB9466C28CEC.png)

2.填写body名称、描述，选择类型为其他，然后点击保存按钮，这样就成功创建了通用模型格式——html。 

![](https://github.com/zhangwanjun111/OrchsymHelp/raw/master/A2Amodel/image.png)
