# 期刊管理平台二期搜索接口

------

## 接口描述
搜索满足条件的爬虫


###HTTP方法: POST

###请求URL: 
    http://127.0.0.1:8000/v1/search

##Body请求示例:

    {
    	"runCode": 1
    }
### 请求参数

|参数|是否必选|类型|描述
|-|-|-|-
|runCode|否	|int	|爬虫运行状态，0为未启动，1为启动，2为异常，不传则默认返回全部爬虫
|issn|否	|string	|刊号
|seriesName|否	|string	|刊名
|domain|否	|string	|域名
|collectType|否	|string	|人工为munal，智能为ai
|crawler|否	|string	|采编人员

    
### 返回参数

    {
        "data": {
            "count": 1,
            "pageSize": 100,
            "page": 1,
            "results": [
                {
                    "series_id": "2e03c1ae-c312-11e9-93f2-482ae31bec7c",
                    "series_name": "Publishers Weekly",  # 期刊名称
                    "issn": "00000019",
                    "issns": [
                        {
                            "issn": "21504008"
                        }
                    ],
                    "collect": {
                        "last_vol": "",  # 爬取期刊最新卷
                        "last_year": 0,  # 爬取期刊最新年
                        "last_month": 0, # 爬取期刊最新月
                        "next_year": "", # 预测期刊最新年
                        "next_month": "", # 预测期刊最新月
                        "end_issue": "", # 爬取期刊最新期
                        "collect_type": "munal",
                        "cb_user": "赵均嵘",
                        "next_vol": "",  # 预测期刊最新卷
                        "next_issue": ""  # 预测期刊最新期
                    },
                    "crawler": {
                        "crawler_name": "",  # 爬虫名称
                        "last_run_time": 0,  # 最近运行时间
                        "last_run_code": 1,  # 爬虫运行状态
                        "last_run_message": "",  # 异常原因
                        "crawler_master": "王利贤",  # 责任采编
                        "run_cycle": 0  # 运行周期
                    },
                    "traits": {
                        "fulltext_download": "",
                        "cover_image": ""
                    },
                    "source": {
                        "homepage": "",
                        "domain": "",
                        "entry_url": ""  # 采集入口
                    },
                    "publisher": {
                        "publisher_name": "PWxyz LLC"
                    },
                    "evaluation": {
                        "index_organ": [],
                        "is_oa": 0.0
                    }
                }
            ]
        },
        "code": 200,
        "msg": "success"
    }




