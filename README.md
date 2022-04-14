# Course-Bullying-in-GZHU
广州大学选课脚本，务必阅读一下信息：
- 课程：课程是大课程，一个课程下可以有很多个教学班。例如大学体育4下面有142个教学班。课程号为8~10位的数字。
- 教学班：一个课程下的教学班，同一课程下的教学班可以是不同老师教也可以是同一个老师教。格式为：（学年）-课程号-教学班号。  
![iAMZk.png](https://s1.328888.xyz/2022/04/14/iAMZk.png)
- 课程所属板块：一共有三种：主修、体育、通识。

## 三种功能：
1. 自动抢课（不推荐）：  
当下达命令后将会按照配置文件逐一进行选课操作，可以蹲点中午12点开始。按照经验，教务系统回应每一个请求均需30秒以上，脚本可以跳过5个资源请求直接向服务器提交选课请求，因此脚本比手选节约250~300秒左右。
2. 课程捡漏（推荐使用）：  
想选的教学班爆满时使用。以1次/秒频率查询想选的教学班并且当有空位时自动选课。
3. 替换选课（未来计划）：  
该功能适用于：你想选的A、B两个教学班冲突（时间冲突或者是因为一课程但不同老师教），而你选了A课程保底且当B有空位的时候使用。简单来说就是先选A，当B可选退掉A再选B

## 注意事项
1. 确保您的网络环境正常未使用VPN  
2. 推测教务系统服务器会因为抢课人数过多导致不能及时返回数据， 比如一直加载但上不去、404、Service Unavailable等报错 。因此建议脚本和手动一起抢课。  
3. 不要多开脚本，有可能产生位置问题  
  
## 使用流程
如果使用**python**运行，直接git clone整个项目，随后`pip install -r requirements.txt`  
安装完依赖后`python main.py`运行。  
win端嫌麻烦可以下载压缩包，然后在解压双击打开`START.bat`即可。  

打开后先输入0配置信息，按照console提示信息输入即可。
配置完信息后推荐使用**捡漏模式**进行抢课。
  
![ih5qv.png](https://s1.328888.xyz/2022/04/14/ih5qv.png)  
