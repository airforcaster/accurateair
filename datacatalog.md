数据说明

主页 https://quotsoft.net/air/
新浪微博@王_晓磊 ，邮箱 quotsoft@qq.com


本站免费提供自1942年以来的中国地面气象数据下载。数据源为NCDC（美国国家气候数据中心，National Climatic Data Center），隶属于NOAA（美国国家海洋及大气管理局，National Oceanic and Atmospheric Administration）。 
数据来自NCDC的公开FTP服务器 ftp://ftp.ncdc.noaa.gov/pub/data/noaa/isd-lite/，本站只选取了中国区域（含港澳台）的观测站点数据，重新按年打包。

时间范围：1942年至今。 
时间精度：近年的数据大多为3小时数据，少量站点有1小时数据。 
站点数量：近年为400多个。 
气象要素：气温、气压、露点、风向风速、云量、降水量。 


按年打包文件china_isd_lite_****.zip解压后是几百个站点数据文件，每个文件是单个站点全年的数据。文件名如“552990-99999-2000”，第1段数字是站点ID，第3段数字是年份。 

数据格式ISD-Lite，是简化的ISD（Integrated Surface Data）数据。每列固定宽度，非常易于程序解析，也可直接当做“空格分隔的CSV”使用。具体每列的含义及数据格式见isd-lite-format.txt，有详细解释。时间是GMT时间。

站点ID和站点名、经纬度的对应关系见isd-history.csv，该列表各列含义见isd-history.txt文件开头。isd-history.csv里包含了所有用到过的站点，包括大量现在已经不在使用的。经纬度是WGS-84坐标系。
国家ID列表见country-list.txt。本站数据只包含了国家ID为CH、HK、MC、TW的站点。

另附一份中文的站点列表“中国地面气象站基本气象要素观测资料台站表.pdf”，此份文件来自中国国家气象科学数据中心的中国气象数据网 http://data.cma.cn/，里面的区站号加上个0即isd-history.csv里的站点ID。

此处所用的ISD-Lite数据，只包含了部分气象要素。更全面的数据可在前述FTP服务器的 /pub/data/noaa/ 目录里按年下载，但ISD格式解析起来不如ISD-Lite方便，所以本站没有采用。 



