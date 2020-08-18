We have two databases, one is the wehther database, the other is air quality database.

weather database explanation:

主页 https://quotsoft.net/air/


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



Homepage https://quotsoft.net/air/

This site provides free download of China's surface meteorological data since 1942. The data source is NCDC (National Climatic Data Center), which belongs to NOAA (National Oceanic and Atmospheric Administration). The data comes from NCDC’s public FTP server ftp://ftp.ncdc.noaa.gov/pub/data/noaa/isd-lite/. This site only selects data from observation sites in China (including Hong Kong, Macao and Taiwan), and re-years Bale.

Time frame: 1942 to present. 
Time accuracy: Most of the data in recent years are 3 hours of data, and a small number of sites have 1 hour of data. 
Number of stations: more than 400 in recent years. 
Meteorological elements: temperature, air pressure, dew point, wind direction and speed, cloud cover, precipitation.

After decompressing the file china_isd_lite_****.zip packaged annually, there are hundreds of site data files, and each file is the annual data of a single site. The file name is like "552990-99999-2000", the number in the first segment is the site ID, and the number in the third segment is the year.

The data format ISD-Lite is simplified ISD (Integrated Surface Data) data. Each column has a fixed width, which is very easy for the program to parse, and it can also be directly used as a "space-separated CSV". 
Introduction

The ISD-Lite data contain a fixed-width formatted subset of the complete Integrated Surface Data (ISD) for a select number of observational elements.  The data are typically stored in a single file corresponding to the ISD data, i.e. one file per station per year.  For more information on the ISD-Lite format, consult the ISD-Lite technical document.

Data Format

Field 1: Pos 1-4, Length 4: Observation Year
Year of observation, rounded to nearest whole hour

Field 2: Pos 6-7, Length 2: Observation Month
Month of observation, rounded to nearest whole hour

Field 3: Pos 9-11, Length 2: Observation Day
Day of observation, rounded to nearest whole hour

Field 4: Pos 12-13, Length 2: Observation Hour
Hour of observation, rounded to nearest whole hour

Field 5: Pos 14-19, Length 6:  Air Temperature
The temperature of the air
UNITS:  Degrees Celsius
SCALING FACTOR: 10
MISSING VALUE: -9999

Field 6: Pos 20-24, Length 6: Dew Point Temperature
The temperature to which a given parcel of air must be cooled at constant pressure and water vapor content in order for saturation to occur.
UNITS: Degrees Celsius
SCALING FACTOR: 10
MISSING VALUE: -9999

Field 7: Pos 26-31, Length 6: Sea Level Pressure
The air pressure relative to Mean Sea Level (MSL).
UNITS:  Hectopascals
SCALING FACTOR: 10
MISSING VALUE: -9999

Field 8: Pos 32-37, Length 6: Wind Direction
The angle, measured in a clockwise direction, between true north and the direction from which the wind is blowing.
UNITS: Angular Degrees
SCALING FACTOR: 1
MISSING VALUE: -9999
*NOTE:  Wind direction for calm winds is coded as 0.

 
Field 9: Pos 38-43, Length 6: Wind Speed Rate
The rate of horizontal travel of air past a fixed point.
UNITS: meters per second
SCALING FACTOR: 10
MISSING VALUE: -9999

Field 10: Pos 44-49, Length 6: Sky Condition Total Coverage Code
The code that denotes the fraction of the total celestial dome covered by clouds or other obscuring phenomena.
MISSING VALUE: -9999
DOMAIN:
 0: None, SKC or CLR
 1: One okta - 1/10 or less but not zero
 2: Two oktas - 2/10 - 3/10, or FEW
 3: Three oktas - 4/10
 4: Four oktas - 5/10, or SCT
 5: Five oktas - 6/10
 6: Six oktas - 7/10 - 8/10
 7: Seven oktas - 9/10 or more but not 10/10, or BKN
 8: Eight oktas - 10/10, or OVC
 9: Sky obscured, or cloud amount cannot be estimated
10: Partial obscuration
11: Thin scattered
12: Scattered
13: Dark scattered
14: Thin broken
15: Broken
16: Dark broken
17: Thin overcast
18: Overcast
19: Dark overcast

Field 11: Pos 50-55, Length 6: Liquid Precipitation Depth Dimension - One Hour Duration
The depth of liquid precipitation that is measured over a one hour accumulation period.
UNITS: millimeters
SCALING FACTOR: 10
MISSING VALUE: -9999
*NOTE:  Trace precipitation is coded as -1

Field 12: Pos 56-61, Length 6: Liquid Precipitation Depth Dimension - Six Hour Duration
The depth of liquid precipitation that is measured over a six hour accumulation period.
UNITS: millimeters
SCALING FACTOR: 10
MISSING VALUE: -9999
*NOTE:  Trace precipitation is coded as -1



For the correspondence between site ID, site name, and latitude and longitude, see isd-history.csv, and see the beginning of the isd-history.txt file for the meaning of each column in the list. isd-history.csv contains all used sites, including a large number of sites that are no longer in use. Latitude and longitude is the WGS-84 coordinate system. See country-list.txt for the country ID list. This site data only includes sites with country IDs of CH, HK, MC, TW.

Also attached is a Chinese site list "China Ground Meteorological Station Basic Meteorological Elements Observation Data Station Table.pdf", this document comes from China Meteorological Data Network http://data.cma.cn/ of China National Meteorological Data Center , Add 0 to the district station number inside, which is the station ID in isd-history.csv.

The ISD-Lite data used here only contains some meteorological elements. More comprehensive data can be downloaded annually in the /pub/data/noaa/ directory of the aforementioned FTP server, but the ISD format is not as easy to parse as ISD-Lite, so this site does not use it.

Air quality data:
 contains 253 cities' hourly PM2.5 index data from 2015 to 2020, north to changchun south to guangzhou.


