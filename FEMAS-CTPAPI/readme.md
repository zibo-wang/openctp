# CTP程序接入飞马开放柜台
飞马开放柜台是中金所数据有限公司开发的期货交易柜台

## 模拟账号注册
请联系提供飞马柜台的期货公司申请

## 配置文件
由于对外封装为ctp接口，飞马额外需要的参数须在femasapi.ini配置文件中进行配置
femasapi.ini应和CTPAPI兼容接口（thosttraderapi_se.dll/thostmduserapi_se.dll）放在同级目录下

femasapi.ini内容如下：
```
#飞马查询前置地址 支持多组 使用";"分隔
QryfrontAddr=tcp://127.0.0.1:60618
#飞马AppID 只支持直连
FemasAppID=xxx
#飞马授权码
FemasAuthCode=xxx
#是否开启api日志(yes/no) 将记录在femasapi.log文件中
OpenLog=yes
#是否开启行情api日志(yes/no) 将记录在femasapi.log文件中
OpenMdLog=yes
```

## 模拟环境
模拟环境的交易前置、行情前置、查询前置地址请联系提供飞马柜台的期货公司申请
注：查询前置地址需在femasapi.ini中配置，交易和行情前置地址按照CTP程序原先方式设置

## CTPAPI兼容接口
飞马API封装后的CTP格式接口，CTP程序只需更换ctp的交易和行情dll即可对接到飞马柜台，程序无需重新编译

#### 认证信息：
- BrokerID: 需申请
- AppID: 需申请
- AuthCode: 需申请

#### 下载地址：
[飞马柜台CTPAPI兼容接口下载](http://www.openctp.cn/download.html)