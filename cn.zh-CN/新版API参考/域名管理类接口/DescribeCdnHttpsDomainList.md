# DescribeCdnHttpsDomainList {#doc_api_Cdn_DescribeCdnHttpsDomainList .reference}

调用DescribeCdnHttpsDomainList获取用户所有证书信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Cdn&api=DescribeCdnHttpsDomainList&type=RPC&version=2018-05-10)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeCdnHttpsDomainList|操作接口名，系统规定参数：**DescribeCdnHttpsDomainList**。

 |
|Keyword|String|否|com|搜索关键字。

 |
|PageNumber|Integer|否|5|取得第几页，取值范围为：1~100000。

 |
|PageSize|Integer|否|20|分页大小，默认20。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|CertInfos| | |证书信息。

 |
|CertCommonName|String|xxx.com|证书主域名。

 |
|CertExpireTime|String|2018-12-26 14:45:09|证书过期时间。

 |
|CertName|String|xxx|证书名称。

 |
|CertStartTime|String|2018-11-26 14:45:09|证书开始时间。

 |
|CertStatus|String|mismatch|证书状态：

 -   **ok**：正常。
-   **mismatch**：域名与证书不匹配。
-   **expired**：已过期。
-   **expire\_soon**：即将过期。

 |
|CertType|String|free|证书类型：

 -   **free**：免费证书。
-   **cas**：云盾证书。
-   **upload**：自定义上传。

 |
|CertUpdateTime|String|2019-01-08 18:33:16|证书更新时间。

 |
|DomainName|String|xxx|加速域名。

 |
|RequestId|String|F5E8DF64-7175-4186-9B06-F002C0BBD0C5|请求ID。

 |
|TotalCount|Integer|16|总条数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}
http(s)://cdn.aliyuncs.com?Action=DescribeCdnHttpsDomainList
&<公共请求参数>
```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeCdnHttpsDomainList>
	  <CertInfos>
		    <CertInfo>
			      <CertUpdateTime>2019-01-08 18:33:16</CertUpdateTime>
			      <CertType></CertType>
			      <CertName></CertName>
			      <DomainName>xxx</DomainName>
			      <CertStatus>mismatch</CertStatus>
			      <CertExpireTime>2018-12-26 14:45:09</CertExpireTime>
			      <CertStartTime>2018-11-26 14:45:09</CertStartTime>
			      <CertCommonName>*.xxx.com</CertCommonName>
		    </CertInfo>
	  </CertInfos>
	  <TotalCount>16</TotalCount>
	  <RequestId>F5E8DF64-7175-4186-9B06-F002C0BBD0C5</RequestId>
</DescribeCdnHttpsDomainList>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"TotalCount":16,
	"RequestId":"F5E8DF64-7175-4186-9B06-F002C0BBD0C5",
	"CertInfos":{
		"CertInfo":[
			{
				"CertUpdateTime":"2019-01-08 18:33:16",
				"CertType":"",
				"CertName":"",
				"DomainName":"xxx",
				"CertStatus":"mismatch",
				"CertExpireTime":"2018-12-26 14:45:09",
				"CertStartTime":"2018-11-26 14:45:09",
				"CertCommonName":"*.xxx.com"
			}
		]
	}
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/Cdn)查看更多错误码。

