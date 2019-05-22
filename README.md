# Crawler | 渣男爬虫

快读从互联网上爬取大量渣男的信息。

## 架构与技术栈

### 搜索器(python)

按照给定的关键词生成搜索策略，从搜索引擎中获取结果页 url。

### 生成器(python)

从给定的结果页 url 获取网页内容。

### 辅助器(python)

- IP 池
- 站点相关 Cookie 池
- Selenium 容器

### 解析器(python)

从网页内容中抽取出人物信息，即实体-关系抽取。

### 持久化器(go)

接收解析器抽取的信息并存储到数据库中。

## 运行模式

### 单人模式

`sobcrawler --singleton "(叶飞杨 or Yefeiyang or 'feiyang ye' or yfy or ronso) and (南方科技 or SUST)" --output result.json`

### 随机游走模式

`sobcrawler --walk "湖北" --persist-server localhost:3500`

