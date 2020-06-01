# 修改期刊接口

------

## 接口描述
修改期刊字段信息。


### HTTP方法: PUT

### 请求URL: 
    http://127.0.0.1:8000/v1/journal/update

## Body请求示例:

    {
    	"seriesId": "19190552-b8bd-11e9-9871-482ae31bec7c",
    	"seriesName": "Publisher",
    	"user": "yhb"
    }
### 请求参数

|参数|是否必选|类型|描述
|-|-|-|-
|seriesId|是	|string	|期刊id
|user|是|string|用户名
|seriesName|否|string|
|issn|否	|string	|刊号
|letter|否|string|首字母
|specialNo|否|string|刊号类型
|lang|否|string|语言
|endIssue|否|string|最后卷期
|collectType|否|string|采集类型
|nextYear|否|string|
|nextMonth|否|string|
|crawlerName|否|string|
|dbName|否|string|
|dbCategory|否|string|
|subject|否|string|
|fulltextDownload|否|string|
|isDel|否|string|
|coverOrigin|否|string|
|creatorName|否|string|
|creatorLocation|否|string|
|homePage|否|string|
|domaIn|否|string|
|entryUrl|否|string|
|publisherName|否|string|
|indexOrgan|否|string|
|isOa|否|string|
|organization|否|string

    
### 返回参数
    完整期刊信息
