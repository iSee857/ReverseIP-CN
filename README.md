简介：

ReverseIP-CN 是一款专为中文网络环境优化的IP反查工具，能够快速查询指定IP/域名关联的所有网站，是网络安全检测、资产梳理的利器。

依赖包安装：

pip install -r requirements.txt

  
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

127.0.0.1

127.0.0.1:8080

http://127.0.0.1

https://127.0.0.1/path

![image](https://github.com/user-attachments/assets/7a594455-c085-4d6e-85d1-0808614d0e14)

导出结果

![image](https://github.com/user-attachments/assets/874eaccd-6d60-4900-a9c9-8520116194c5)


⚠️ 注意事项

国内接口有频率限制，建议：

  单次批量查询不超过50个目标
  
  每个查询间隔1-2秒
  
结果文件会自动高亮显示：

  黄色：包含原始域名的结果
  
  绿色IP：表示该IP存在关联域名
