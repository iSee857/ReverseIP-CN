简介：

ReverseIP-CN 是一款专为中文网络环境优化的IP反查工具，能够快速查询指定IP/域名关联的所有网站，是网络安全检测、资产梳理的利器。

设计流程图

输入处理 -> 协议/端口清洗 -> 域名查询 -> 结果分析 -> Excel导出
  │          │              │           │
  └─无效输入─┘              └─失败重试─┘
  
参数说明：

参数	全称	说明
-u	--url	指定单个目标URL/IP
-l	--list	指定包含多个目标的文件路径
-o	--output	指定输出Excel文件名（可选）
-h	--help	显示帮助信息

目前支持以下功能

1. 查询单个目标

python revip_cn.py -u "目标URL/IP"

2. 批量查询（从文件读取）

python revip_cn.py -l 目标列表.txt -o 结果.xlsx

3、智能输入清洗：

自动处理各种输入格式：

218.56.165.110

218.56.165.110:8080

http://218.56.165.110

https://218.56.165.110/path

⚠️ 注意事项

国内接口有频率限制，建议：

  单次批量查询不超过50个目标
  
  每个查询间隔1-2秒
  
结果文件会自动高亮显示：

  黄色：包含原始域名的结果
  
  绿色IP：表示该IP存在关联域名
