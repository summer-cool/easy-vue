#建模配置字段
> config
```js
[
    {
        "tileName": "应用汇",
        "tag": "FsApplicationSink",
        "config": []
    },
    {
        "tileName": "应用代办",
        "tag": "FsApplicationTodo",
        "config": [
            {
                "optionType": "selectApplication",
                "optionTitle": "应用选择",
                "requestUrl": "",
                "selectedList": []
            }
        ]
    },
    {
        "tileName": "表格查询",
        "tag": "FsTableQuery",
        "config": [
            {
                "optionType": "dropMenu",
                "optionTitle": "查询选择",
                "requestUrl": "",
                "selected": {
                    "id": "",
                    "name": ""
                }
            },
            {
                "optionType": "text",
                "optionTitle": "显示条数",
                "value": "10",
                "placeholder": ""
            }
        ]
    },
    {
        "tileName": "交叉表查询",
        "tag": "FsCrossTableQuery",
        "config": [
            {
                "optionType": "dropMenu",
                "optionTitle": "查询选择",
                "requestUrl": "",
                "selected": {
                    "id": "",
                    "name": ""
                }
            },
            {
                "optionType": "text",
                "optionTitle": "显示条数",
                "value": "10",
                "placeholder": ""
            }
        ]
    },
    {
        "tileName": "智象报表",
        "tag": "FsIntelligenceReport",
        "config": [
            {
                "optionType": "dropMenu",
                "optionTitle": "查询选择",
                "requestUrl": "",
                "selected": {
                    "id": "",
                    "name": ""
                }
            }
        ]
    }
]
```
----------------------------------
###参数说明
```js
    //主体配置
    {
        "tileName": "",
        "tag": "",
        "config": []
    }
```
```sh
基本主体参数:
    tileName -- 磁贴名称
    tag -- 磁贴唯一id
    config -- 磁贴属性配置项目
```
```js
    //config
    {
        "tileName": "",
        "tag": "",
        "config": [{
                "optionType": "selectApplication",
                "optionTitle": "",
                "requestUrl": "",
                "selectedList": []
            },
            {
                "optionType": "dropMenu",
                "optionTitle": "",
                "requestUrl": "",
                "selected": {
                    "id": "",
                    "name": ""
                }
            },
            {
                "optionType": "text",
                "optionTitle": "",
                "value": "",
                "placeholder": ""
            }]
    }
```
```sh
 config目前支持的三种配置--选择选项类，下拉选择类，文本设置类
 参数配置依次为:
    1.选择选项类:
        optionType:磁贴属性配置类型 -- selectApplication(选择项,树结构)
        optionTitle:磁贴配置项名称
        requestUrl:选项数据接口(接口数据树结构)
        selectedList:选择项返回数组
    2.下拉选择类:
        optionType:磁贴属性配置类型 -- dropMenu
        optionTitle:磁贴配置项名称
        requestUrl:下拉选项数据接口
        selected:当前选中条目的id，name值
    3.文本设置类:
        optionType:磁贴属性配置类型 --text(输入框类型)
        optionTitle:磁贴配置项名称
        value:输入值
        placeholder:输入框提示

    以上配置项，可重复添加.
```


