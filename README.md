这个项目是在王道集训营写下的。
功能：根据用户的输入提取关键字，输出与关键字相似的词语，帮助用户完成输入。
项目共分为离线部分和在线部分。
离线部分加载候选词文件，利用cppjieba对中文分词，创建中英词典，根据utf-8编码格式截取单个中文字符，创建中英文字符索引文件。
在线部分封装线程池和网络编程模块，获取客户端传递过来的查询词，先从Redis数据库中寻找索引，未命中再采用最小编辑距离算法计算候选词与查询词的相似度。将结果封装为Json字符串，采用私有协议发送给客户端。

