# PERF AUTO
> **作者**：Dawn  
> **工具**：Jmeter  
> **概述**：本项目主要用于==接口性能测试==，所用工具为`jmeter`。项目提供了通过CSV获取数据并参数化，通过Mysql数据库获取数据并参数化，发送http请求，生成各种报告等功能。项目主要实现了负载测试和可靠性测试。  

### 项目目录介绍  
```
uiauto
  ┝ case        # 用于存放测试计划
  ┝ lib         # 用于存放公共库
  ┝ report      # 用于存放测试报告
  └ README.md   # 说明文件
```

### 使用步骤  
1. 安装`jmeter`（版本: `5.0`或更高）。  
- jmeter: https://jmeter.apache.org/download_jmeter.cgi/  

2. 安装`PluginsManager`插件及用到的图表。
- PluginsManager: https://jmeter-plugins.org/wiki/PluginsManager/  
- ResponseTimesOverTime: https://jmeter-plugins.org/wiki/ResponseTimesOverTime/  
- TransactionsPerSecond: https://jmeter-plugins.org/wiki/TransactionsPerSecond/  

3. 打开`Jmeter`，打开`case`文件夹中的测试计划，执行测试。  

4. 将报告中的数据记录在`report`文件夹的报告中，并得出测试结论。  
或使用`Jmeter`自带的生成测试报告功能：  
```
# 在cmd中切换到jmeter的bin目录下，执行下列命令生成测试报告：
# 已有jtl文件时：
jmeter -g 测试计划.jtl -o 测试报告
# 无jtl文件时：
jmeter -n -t 测试计划.jmx -l 测试计划.jtl -e -o 测试报告
```