<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .container {
            display: flex;
        }
        .sidebar {
            width: 30%;
            padding: 20px;
            background-color: #f4f4f4;
        }
        .content {
            width: 60%;
            padding: 20px;
        }
    </style>
</head>
<body>

<div class="container">
    <div class="sidebar">

## 接口列表

|  接口  | 说明 |
|------ |----- |
|[/dict/query](#dictquery)| 字典表查询|
|[/qyjb/query](#qyjbquery)| 企业基本信息查询|
|[/qyjb/modify](#qyjbmodify) | 企业基本信息更新|
|[/qyjb/add](#qyjbadd)| 企业基本信息新增|
|[/qyjb/delete](#qyjbdelete)| 企业基本信息删除|
|[/hyjb/query](#hyjbquery)| 行业基本信息查询|
|[/hyjbjq/modify](#hyjbmodify) | 行业基本信息景区信息更新|
|[/zdbw/query](#zdbwquery) | 重点部位查询|
|[/zdbw/add](#zdbwadd) | 重点部位新增|
|[/zdbw/modify](#zdbwmodify) | 重点部位修改|
|[/zdbw/delete](#zdbwdelete) | 重点部位删除|
|[/cyry/query](#cyryquery) | 从业人员查询|
|[/cyry/add](#cyryadd) | 从业人员新增|
|[/cyry/modify](#cyrymodify) | 从业人员修改|
|[/cyry/delete](#cyrydelete) | 从业人员删除|
|[/bajg/query](#bajgquery) | 保安机构查询|
|[/bajg/add](#bajgadd) | 保安机构新增|
|[/bajg/modify](#bajgmodify) | 保安机构修改|
|[/bajg/delete](#bajgdelete) | 保安机构删除|
|[/bary/query](#baryquery) | 保安人员查询|
|[/bary/add](#baryadd) | 保安人员新增|
|[/bary/modify](#barymodify) | 保安人员修改|
|[/bary/delete](#barydelete) | 保安人员删除|
|[/nbcrkryxx/query](#nbcrkryxxquery) | 内保出入人员查询|
|[/nbcrkclxx/query](#nbcrkclxxquery) | 内保出入车辆查询|
|[/wfxx/query](#wfxxquery) | 物防信息查询|
|[/wfxx/add](#wfxxadd) | 物防信息新增|
|[/wfxx/modify](#wfxxmodify) | 物防信息修改|
|[/wfxx/delete](#wfxxdelete) | 物防信息删除|
|[/jfxx/query](#jfxxquery) | 技防信息查询|
|[/jfxx/add](#jfxxadd) | 技防信息新增|
|[/jfxx/modify](#jfxxmodify) | 技防信息修改|
|[/jfxx/delete](#jfxxdelete) | 技防信息删除|
|[/zdxx/query](#zdxxquery) | 制度信息查询|
|[/zdxx/add](#zdxxadd) | 制度信息新增|
|[/zdxx/modify](#zdxxmodify) | 制度信息修改|
|[/zdxx/delete](#zdxxdelete) | 制度信息删除|
|[/jfsjxx/query](#jfsjxxquery) | 技防数据信息查询|
|[/flxx/query](#flxxquery) | 法律信息查询|
|[/flxx/add](#flxxadd) | 法律信息新增|
|[/flxx/modify](#flxxmodify) | 法律信息修改|
|[/flxx/delete](#flxxdelete) | 法律信息删除|
|[/tztg/query](#tztgquery) | 通知通告查询|
|[/tztg/add](#tztgadd) | 通知通告新增|
|[/tztg/modify](#tztgmodify) | 通知通告修改|
|[/tztg/delete](#tztgdelete) | 通知通告删除|
|[/sjsb/query](#sjsbquery) | 时间上报查询|
|[/sjsb/add](#sjsbadd) | 时间上报新增|
|[/sjsb/modify](#sjsbmodify) | 时间上报修改|
|[/sjsb/delete](#sjsbdelete) | 时间上报删除|
|[/qyjbxx/commit](#qyjbxxcommit) | 企业季报信息上报|
|[/qyjbxx/revoke](#qyjbxxrevoke) | 企业季报信息撤回|
|[/qyjbxx/query](#qyjbxxquery) | 企业季报信息查询|


   </div>
    <div class="content">



## 接口详情
* <span id = "dictquery">字典表查询</span>
 
    * 接口地址：/dict/query/
    * 返回格式：Json
    * 请求方式：Post
    * 接口备注：查询字典内容。
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |SJZDBM |string|true|数据字典编码|
 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        | code | int|状态码
        |data | object|具体数据|
        |msg | string|返回信息|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"data": [
    		{
    			"CJSJ":"创建时间",
				"XGSJ":"修改时间",
				"MC":"名称",
				"BM":"编码",
				"PX":"排序",
				"SJBM":"上级编码",
				"SSSJZDBM":"所属数据字典编码",
				"BZ":"备注",
				"SFXS":"是否显示",
				"SFSC":"是否删除"
    		}
    	]
    }
    ```             
 
 
---

* <span id = "qyjbquery">企业基本信息查询</span>
 
    * 接口地址：/qyjb/query/
    * 返回格式：Json
    * 请求方式：Post
    * 接口备注：查询字典内容。
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |ID |string|false|企业基本信息表主键|
        |DWMC |string|false|单位名称|
        |JGDWBM |string|false|监管单位编码|
        |SJHM |string|false|手机号码|
        |PAGE |string|false|当前页(默认0)|
        |SIZE |string|false|每页数量(默认20)|


 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        |code | int|状态码|
        |data | object|具体数据|
        |msg | string|返回信息|
        |total | int|总数|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"total":100,
    	"data": [
    		{
    			"企业基本信息对象1":"参考附表",
    		},
    		{
    			"企业基本信息对象2":"参考附表",
    		}
    	]
    }
    ```             
 
 
---
 

* <span id = "qyjbmodify">企业基本信息更新</span>
 
    * 接口地址：/qyjb/modify/
    * 返回格式：Json
    * 请求方式：Post
    * 接口备注：查询字典内容。
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |ID |string|true|企业基本信息表主键|
        |DWMC |string|true|企业名称|
        |DWLX |string|true|企业类型|
        |FDDBRXM |string|true|法定代表人姓名|
        |JYFWZY |string|true|经营范围(限500字)|
        |TYSHXYDM |string|true|统一社会信用代码|
        |ZCZB |string|true|注册资本(限100字)|
        |CLRQ |string|true|成立日期(YYYY-MM-DD)|
        |DJZT |string|true|登记状态|
        |ZCDZ |string|true|注册地址|
        |DJJG |string|true|登记机关|
        |BMHJC |string|true|别名或简称|
        |FDDBRZJLX |string|true|法人证件类型|
        |FDDBR_ZJHM |string|true|法人证件号码|
        |HYFL |string|true|行业分类|
        |XZQHDM |string|true|行政区划代码|
        |GAGXJG_S |string|true|公安管辖机构_省|
        |GAGXJG_DS |string|true|公安管辖机构_地市|
        |GAGXJG_QX |string|true|公安管辖机构_区县|
        |GAGXJG_PCS |string|true|公安管辖机构_派出所|
        |QYBZDZ_DS |string|true|企业标准地址_地市|
        |QYBZDZ_QX |string|true|企业标准地址_区县|
        |QYBZDZ_JLX |string|true|企业标准地址_街路巷|
        |QYBZDZ_XXDZ |string|true|企业标准地址_详细地址|
        


 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        |code | int|状态码|
        |data | object|具体数据|
        |msg | string|返回信息|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"data": {}
    }
    ```             
 ---

 * <span id = "qyjbadd">企业基本信息新增</span>
 
    * 接口地址：/qyjb/add/
    * 返回格式：Json
    * 请求方式：Post
    * 接口备注：初始添加企业基本信息。
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |QYMC |string|true|企业名称|
        |FZRMC |string|true|负责人名称|
        |FZRDH |string|true|负责人电话|
 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        | code | int|状态码
        |data | object|具体数据|
        |msg | string|返回信息|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"data": {},
    }
    ```             
 
 
  ---

 * <span id = "qyjbdelete">企业基本信息删除</span>
 
    * 接口地址：/qyjb/delete/
    * 返回格式：Json
    * 请求方式：Post
    * 接口备注：删除企业基本信息。
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |QYID |string|true|企业基本信息表主键|
 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        | code | int|状态码
        |data | object|具体数据|
        |msg | string|返回信息|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"data": {},
    }
    ```             
 
 

---


 * <span id = "hyjbquery">行业基本信息查询</span>
 
    * 接口地址：/hyjb/query/
    * 返回格式：Json
    * 请求方式：Post
    * 接口备注：查询行业基本信息。
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |ID |string|true|企业基本信息表主键|
 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        | code | int|状态码
        |data | object|具体数据|
        |msg | string|返回信息|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"data": {
    		"行业基本信息表":"参考附表"
    	},
    }
    ```             
 
 ---


 * <span id = "hyjbmodify">行业基本信息更新中的景区信息</span>
 
    * 接口地址：/hyjbjq/modify/
    * 返回格式：Json
    * 请求方式：Post
    * 接口备注：更新行业基本信息。
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |ID |string|true|中文名称|
        |JQZWMC |string|true|中文名称|
        |JQZWJC |string|true|中文简称|
        |JQYWMC |string|true|英文名称|
        |JQJB |string|true|景区级别|
        |JQJJ |string|true|景区简介|
        |JQMPT |object array|true|景区平面图|
        |KYRQ |string|true|开业日期|
        |JQCZL |string|true|景区承载量|
        |JTSM |string|true|交通说明|
        |PTSS |string|true|配套设施|
		|CSLYHD |string|true|常设旅游活动|
        |JQLX |string|true|景区类型|
        |SFKFSJQ |int|true|是否开放景区|
        |MPJG |string|true|门票价格|
        |MPJGSM |string|true|门票价格说明|
        |JQLX |string|true|景区类型|
        |JQLX |string|true|景区类型|
        |SSXZQH_S |string|true|所属行政区划_省|
        |SSXZQH_DS |string|true|所属行政区划_地市|
        |SSXZQH_QX |string|true|所属行政区划_区县|
        |GAGXJG_DS |string|true|公安管辖机构_地市|
        |GAGXJG_QX |string|true|公安管辖机构_区县|
        |GAGXJG_PCS |string|true|公安管辖机构_派出所|
        |WLGXJG |string|true|文旅管辖机构|
        |JQBZDZ_DS |string|true|景区标准地址_地市|
        |JQBZDZ_QX |string|true|景区标准地址_区县|
        |JQBZDZ_JLX |string|true|景区标准地址_街路巷|
        |JQBZDZ_XXDZ |string|true|景区标准地址_详细地址|
        |YZBM |string|true|邮政编码|
        |YYSJ |string|true|营业时间|
        |YLSC |string|true|游览时长|
        |TJYLSC |string|true|推荐游览时长|
        |ZXDH |string|true|咨询电话|
        |WZ |string|true|网站|
        |GFGGKJ |string|true|官方公共空间|
        |DZYJ |string|true|电子邮件|
        |YYSJ |string|true|营业时间|
        |YYSJ |string|true|营业时间|

 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        | code | int|状态码
        |data | object|具体数据|
        |msg | string|返回信息|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"data": {}
    }
    ```             
 
 ---


 * <span id = "zdbwquery">重点部位查询</span>
 
    * 接口地址：/zdbw/query/
    * 返回格式：Json
    * 请求方式：Post
    * 重点部位查询
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |QYID |string|false|企业基本信息表主键|
        |ID |string|false|重点部位信息表业务流水号|
        |ZDBWMC |string|false|重点部位名称|
        |PAGE |string|false|当前页(默认0)|
        |SIZE |string|false|每页数量(默认20)|
 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        | code | int|状态码
        |data | object|具体数据|
        |msg | string|返回信息|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"data": {
    		"行业基本信息表":"参考附表"
    	},
    }
    ```             
 ---


 * <span id = "zdbwadd">重点部位新增</span>
 
    * 接口地址：/zdbw/add/
    * 返回格式：Json
    * 请求方式：Post
    * 接口备注：重点部位新增。
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |QYID |string|true|企业基本信息表主键|
        |ZDBWMC |string|true|重点部位名称|
        |ZDBWLX |string|true|重点部位类型|
        |SSQY |string|true|所属区域|
        |GLBM |string|true|管理部门|
        |ABFZR |string|true|安保负责人|
        |ZJLX |string|true|证件类型|
        |ZJHM |string|true|证件号码|
        |LXFS |string|true|位置描述|
        |PMT |string|false|景区平面图业务流水号|
        |PMTQY |string|false|平面图区域坐标字符串|

 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        | code | int|状态码
        |data | object|具体数据|
        |msg | string|返回信息|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"data": {}
    }
    ```             
 ---


 * <span id = "zdbwmodify">重点部位修改</span>
 
    * 接口地址：/zdbw/modify/
    * 返回格式：Json
    * 请求方式：Post
    * 接口备注：重点部位信息修改。
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |ID |string|true|重点部位信息表业务流水号|
        |ZDBWMC |string|true|重点部位名称|
        |ZDBWLX |string|true|重点部位类型|
        |SSQY |string|true|所属区域|
        |GLBM |string|true|管理部门|
        |ABFZR |string|true|安保负责人|
        |ZJLX |string|true|证件类型|
        |ZJHM |string|true|证件号码|
        |LXFS |string|true|位置描述|
        |PMT |string|false|景区平面图业务流水号|
        |PMTQY |string|false|平面图区域坐标字符串|
 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        | code | int|状态码
        |data | object|具体数据|
        |msg | string|返回信息|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"data": {}
    }
    ```             
 ---


 * <span id = "zdbwdelete">重点部位删除</span>
 
    * 接口地址：/zdbw/delete/
    * 返回格式：Json
    * 请求方式：Post
    * 接口备注：重点部位信息删除。
    * 请求参数说明：
        | 名称 | 类型 | 必填 |说明|
        |----- |------| ---- |----|
        |ID |string|true|重点部位信息表业务流水号|
 
    * 返回参数说明：
        | 名称 | 类型 |说明|
        |----- |------|----|
        | code | int|状态码
        |data | object|具体数据|
        |msg | string|返回信息|
 
    * JSON返回示例：
    ```json
    {
    	"code": 0,
    	"msg":"success",
    	"data": {}
    }
    ```             
 

---
 
## 错误码列表


|  错误码  | 说明 |
|------ |----- |
|   0   | 正确 |
|   -1   | 内部错误 |
|   -2   | 参数错误|
 

   </div>
</div>

</body>
</html>
