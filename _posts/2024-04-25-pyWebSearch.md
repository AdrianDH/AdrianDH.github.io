# 爬虫简易流程

1. 向服务器发送请求，获取网页内容 --> http请求 request库
2. 解析网页内容 --> html结构 bs4库
3. 储存或分析数据 --> 数据存储+分析等具体功能 pandas库等

# 爬虫规则
1. 不要爬取公民隐私数据，不要爬去受著作权保护的内容，不要爬去国家事务、国防建设、尖端科学领域的计算机系统等。
2. 请求数量和频率不应过高
3. 不要强行突破放爬限制
4. 爬取robots.txt中允许爬取的网页


## 常用库

除了上述基本库以外，还有一下库经常使用

## 请求

selenium 自动化库

urllib 一系列操作url的功能，requests是基于urllib便携的

requests_toolbelt 应对requests对http/2、图片数据等的不支持的工具库

aiohttp 基于asyncio实现的http框架，异步操作进行数据抓取，效率提升

httpx python下一代http客户端，相较requests更加现代化

## 解析

lxml 支持html和xml的解析，支持xpath的解析方式

re 正则表达式库，对文本等进行快速分析

parsel 新一代html/xml文档解析库，也是scrapy内置的解析器，支持XPath和CSS两种风格的解析器，并集成了正则

JSONPath 查询和解析复杂json文档的语言，语法类似C，但是没有完整严格的语法规范，不同实现可能有差异

JMESPath 比JSONPath更好的JSON文档提取查询等的语言，但是语法相对复杂

pyquery jQuery的python实现，能够以jQuery的语法操作解析html文件

## 爬虫框架

Scrapy 满足简单的页面爬取，例如亚马逊商品信息的数据

Crawley 告诉爬去对应网站的内容，支持关系和非关系数据库

Portia 可视化爬去网页内容

newspaper 爬去新闻、文章、以及内容分析

python-goose java写的文章提取工具

cola 分布式爬虫框架，但是项目整体设计有点糟糕

Puppeteer google发布的Node库，通过DevTools协议控制浏览器，包括chromium、google chrome、msedge，默认为无头模式

Playwright 微软开发的Web自动化测试工具，支持Chrome、msedge、firefox、opera、safari等

## JS引擎 部分请求在传参过程中需要经过复杂的JavaScript代码生成，使用JS引擎可以避免python对js代码逻辑复现和python与js实现差异

PyMiniRacer 适用于python的最小的现代嵌入式v8，无需额外安装javascript环境


## web框架

flask 轻量级web服务程序，主要用来做一些api服务

django 一个web服务器框架，提供了一个完整的后台管理，引擎、接口等，可以做一个完整的网站。

## 抓包工具

fiddler classic 免费通过创建代理的方式抓取浏览器或其他程序的http/https流量，只适用windows平台。部分app会进行中间人攻击检测，fiddler这种情况不能顺利抓到流量。