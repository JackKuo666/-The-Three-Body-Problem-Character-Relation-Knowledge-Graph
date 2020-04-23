# -The-Three-Body-Problem-Character-Relation-Knowledge-Graph
这个是 开源项目【基于cnSchema的《三体》人物关系知识图谱】体验使用说明
# 这个是 开源项目【基于cnSchema的《三体》人物关系知识图谱】体验使用说明
代码来自：http://openkg.cn/dataset/kg-santi

---

## 安装使用
### 1.安装 python 依赖
```py
pip install -r requirement.txt
``` 

### 2.在`KGQA`目录下安装 ltp_data_v3.4.0 模型
下载地址：https://ltp.ai/download.html

注意：下载模型之后，需要修改相应的`ltp.py`中的模型地址`LTP_DATA_DIR`,要使用绝对路径。

### 3.安装 Neo4j 数据库
3.1 下载地址： https://neo4j.com/download-center/#desktop

3.2 安装之后需要创建一个新的空的数据库，同时设置的账号密码要与 `./neo_db/config.py`中的一致；

3.3 创建之后打开该数据库

### 4.使用py2neo创建图数据
运行`./neo_db/creat_graph.py`代码，在第三步打开的新的数据库中加入数据

### 5.打开flask运行该网页
运行`./app.py`


### 6.在浏览器打开相应网址，即可体验


// todo: 
体验了一下该项目：总共分为三个部分：检索人物关系、三体人物关系全貌、人物关系问答。
其中（人物关系问答）做的还是有些问题，当输入问题没有解析到，或者库中没有时，后端代码直接报错。可以进一步做一些语义理解相关工作。
 
