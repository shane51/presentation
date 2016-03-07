# 大数据相关
---------
## 1.常见名词
#### 1.1 数据篇：
#####  *结构化数据 & 非结构化数据*

-  **结构化数据**: 即行数据,存储在数据库里,可以用二维表结构来逻辑表达实现的数据。

-  **非结构化数据**: 不方便用数据库二维逻辑表来表现的数据即称为非结构化数据。包括所有格式的办公文档、文本、图片、XML、HTML、各类报表、图像和音频/视频信息等等。

-  **半结构化数据**: 就是介于**完全**结构化数据（如关系型数据库、面向对象数据库中的数据）和*完全*无结构的数据（如声音、图像文件等）之间的数据，HTML文档就属于半结构化数据。它一般是自描述的，数据的结构和内容混在一起，没有明显的区分。

具备的数据模型：

	结构化数据：二维表（关系型）

	半结构化数据：树、图

	非结构化数据：无

	特点：
	结构化数据：先有结构、再有数据
	半结构化数据：先有数据，再有结构

##### *数据存取技术*
- **SQL**  
结构化查询语言(Structured Query Language)，操作对象为关系型数据库。存储结构化数据。

- **NoSQL**  
Not only SQL, 泛指非关系型数据库。存储包括非结构化数据和半结构化数据。
 
	![image](https://aryannava.files.wordpress.com/2014/04/nosql-database-family.jpg =400x)   

	关系型数据库：是指采用了关系模型来组织数据的数据库，简单来说，关系模型指的就是二维表格模型，而一个关系型  
				数据库就是由二维表及其之间的联系所组成的一个数据组织  

	非关系型数据库：非关系型数据库提出另一种理念，例如，以键值对存储，且结构不固定，每一个元组可以有不一样的  
				字段，每个元组可以根据需要增加一些自己的键值对，这样就不会局限于固定的结构，可以减少一些时  
				间和空间的开销。
				只适合存储一些较为简单的数据，对于需要进行较复杂查询的数据，SQL数据库显的更为合适。 


#### 1.2 存储篇
- **hadoop & Spark**  
	*Hadoop:*是一个由Apache基金会所开发的分布式系统基础架构，是项目的总称，Hadoop的框架最核心的设计就是：HDFS和MapReduce。HDFS为海量的数据提供了存储，则MapReduce为海量的数据提供了计算。   
![image](http://blogs.cisco.com/wp-content/uploads/Hadoop_Arc.jpg =400x)

	*Spark:* Spark是UC Berkeley AMP lab所开源的类Hadoop MapReduce的通用并行框架。通常与Hadoop中的HDFS合用，也可以选择其他平台  
![image](http://tech.uc.cn/wp-content/uploads/2013/09/spark-framwork.jpg =400x)  
  
	![image](http://image.slidesharecdn.com/2014-11-17clickstreamsocialmediaanalysiswithapachespark-141120023949-conversion-gate01/95/clickstream-social-media-analysis-using-apache-spark-14-638.jpg?cb=1416451409 =400x
)

- **流计算**   
 为了达到更实时的更新，在数据流进来的时候就处理。与Hadoop的中低速应用场景，用于处理高速数据。（如搜索和微博）  
 
 	3种常见的流计算框架  
![image](http://www.altaterra.net/resource/resmgr/a-zen/op-c4.jpg =400x)    
另外还有Facebook的数据流处理系统Puma以及Yahoo的S4（Simple Scalable Streaming System）  
![image](http://www.zhouyoudao.com/wp-content/uploads/2013/10/10-1024x481.png =400x)

- **数据仓库**  
	数据仓库 ，由数据仓库之父比尔·恩门（Bill Inmon）于1990年提出，主要功能仍是将组织透过资讯系统之联机事务处理(OLTP)经年累月所累积的大量资料，透过数据仓库理论所特有的资料储存架构，作一有系统的分析整理，以利各种分析方法如联机分析处理(OLAP)、数据挖掘(Data Mining)之进行，并进而支持如决策支持系统(DSS)、主管资讯系统(EIS)之创建，帮助决策者能快速有效的自大量资料中，分析出有价值的资讯，以利决策拟定及快速回应外在环境变动，帮助建构商业智能(BI)。
![image](http://a.hiphotos.baidu.com/baike/c0%3Dbaike180%2C5%2C5%2C180%2C60/sign=eaa4cccb1ad5ad6ebef46cb8e0a252be/aec379310a55b319d37b757a42a98226cffc173a.jpg =500x)

	- *星型*  
	星型模式：一种使用关系数据库实现多维分析空间的模式，称为星型模式。星型模式的基本形式必须实现多维空间（常常被称为方块），以使用关系数据库的基本功能。星型模式就演进为雪花模式。 通常可做切片，切块和旋转。
![image](http://hi.csdn.net/attachment/201108/12/0_1313117535z0xy.gif)
	- *雪花型*  
	雪花模式：不管什么原因，当星型模式的维度需要进行规范化时，	基本的星型模式并不能满足数据挖掘的所有需要。我们需要更复杂的维度:
![image](http://hi.csdn.net/attachment/201108/12/0_131311750167s4.gif)


#### 1.3 云计算篇
- **Iaas**（AWS）   
Infrastructure-as-a-Service（基础设施即服务）Iaas 提供商Amazon, Microsoft, VMWare, Rackspace和Red Hat
- **Paas**（heroku）  
Platform-as-a-Service（平台即服务）
PaaS提供者有Google App Engine,Microsoft Azure，Force.com,Heroku，Engine Yard
- **Saas** （金数据）  
Software-as-a-Service（软件即服务）

	![image](http://img4.07net01.com/upload/images/2015/12/23/1816987230855511.jpg =500x)


## 2. 大数据系统构架
####     2.1 大数据系统一般构架  
![image](http://images2015.cnblogs.com/blog/321721/201510/321721-20151013125211866-32477296.png =500x)

![image](http://blogs-images.forbes.com/davefeinleib/files/2012/07/Big-Data-Landscape-Jul-4-2012.00111.png =500x)  
![image](https://www.meetuniversity.com/blog/wp-content/uploads/2016/01/Data-Integration-Ecosystem-for-Big-Data-and-Analytics.jpg =500x)
####     2.2 大数据处理技术
![image](http://img.blog.csdn.net/20150215103059348?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvQmVpaUdhbmc=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center =500x)

## 3. 大数据应用
####     3.1 商业智能（BI）与报表
- **SAS、BO、Brio、Cognos  (企业级) **
	- Cognos  
![image](http://image.slidesharecdn.com/bestpracticeswitholapmodelingwithcognostransformer-120405022320-phpapp01/95/ibm-cognos-olap-modeling-with-cognos-transformer-best-practices-9-728.jpg?cb=1371712255 =500x)  
	- SAP Business Objects
![image](http://news.sap.com/wp-content/blogs.dir/1/files/Semantic_Layer1.jpg =500x)  

- **Tableau**  
![image](http://static1.squarespace.com/static/541959a7e4b07421cfbf4ae7/t/541a8aece4b0d5fed9414c6e/1411025644879/tableau+architecture)
####     3.2 数据挖掘  

####     3.3 数据预测
####     3.4 行业应用
