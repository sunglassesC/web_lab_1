# web lab



## 运行环境

#### 语言

python



#### 依赖模块

nltk



In order to install NLTK run the following commands in your terminal.

- `sudo pip install nltk`
- Then, enter the python shell in your terminal by simply typing `python`
- Type `import nltk`
- `nltk.download(‘all’)`

> [参考](https://www.geeksforgeeks.org/tokenize-text-using-nltk-python/?ref=lbp)



## 处理步骤

- 仅保留邮件的主体和正文部分

- 分词

- 词根化

- 去停用词

- 得到倒排表（取词频前1000的词）

倒排表使用python中的字典结构，以单词为键，出现的文档编号组成的数组为值。这里需要说明的是，如果使用邮件的路径作为文档名，类似`./dataset/maildir\allen-p\all_documents\2`这样的字符串，占用空间太多，且由于文档和词的关系是一对多，倒排表中文档名会大量出现，故对所有文档进行编号，将编号和路径的映射输出并存储到`output`文件中，在后续查询时可先得到文档编号，后根据编号及映射表找到文档路径。

