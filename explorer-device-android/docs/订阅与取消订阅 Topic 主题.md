* [订阅与取消订阅](#订阅与取消订阅)
  * [订阅 数据模板相关联 Topic 主题](#订阅-数据模板相关联-Topic-主题)
  * [取消订阅 Topic 主题](#取消订阅-Topic-主题)

# 订阅与取消订阅

当在腾讯云物联网平台创建产品时。会默认生成一套产品的数据模板，生成一些标准功能，也可以自定义功能，数据模板对应的功能种类包含三大类：属性，事件和行为。控制台数据模板的使用，请参考官网 [数据模板](https://cloud.tencent.com/document/product/1081/44921) 章节。

产品定义数据模板后，设备可以按照数据模板中的定义上报属性、事件，并可对设备下发远程控制指令，即对可写的设备属性进行修改。数据模板的管理详见 产品定义。数据模板协议包括设备属性上报、设备远程控制、获取设备最新上报信息、设备事件上报、设备行为。对应的定义和云端下发控制指令使用的 Topic 请参考官网 [数据模板协议](https://cloud.tencent.com/document/product/1081/34916) 章节。

本文主要描述 SDK Demo 对数据模板相关联 Topic 的订阅与取消订阅。

## 订阅 数据模板相关联 Topic 主题

运行示例程序，当设备已上线，在数据模板模块上，点击 订阅主题 按钮，订阅属性，事件，和行为类型的 Topic `$thing/down/property/{ProductID}/{DeviceName}` `$thing/down/event/{ProductID}/{DeviceName}` `$thing/down/action/{ProductID}/{DeviceName}`。示例代码如下：
```
mDataTemplateSample.subscribeTopic(); // 订阅主题
```

观察Logcat日志。
```
I/TXMQTT_1.3.0: Starting subscribe topic: $thing/down/property/LWVUL5SZ2L/dahei
I/TXMQTT_1.3.0: Starting subscribe topic: $thing/down/event/LWVUL5SZ2L/dahei
I/TXMQTT_1.3.0: Starting subscribe topic: $thing/down/action/LWVUL5SZ2L/dahei
D/TXDataTemplateFragment: onSubscribeCompleted, status[OK], topics[[$thing/down/property/LWVUL5SZ2L/dahei]], userContext[MQTTRequest{requestType='subscribeTopic', requestId=0}], errMsg[subscribe success]
D/TXDataTemplateFragment: onSubscribeCompleted, status[OK], topics[[$thing/down/action/LWVUL5SZ2L/dahei]], userContext[MQTTRequest{requestType='subscribeTopic', requestId=2}], errMsg[subscribe success]
D/TXDataTemplateFragment: onSubscribeCompleted, status[OK], topics[[$thing/down/event/LWVUL5SZ2L/dahei]], userContext[MQTTRequest{requestType='subscribeTopic', requestId=1}], errMsg[subscribe success]
```
以上日志为 订阅 Topic 主题 成功。

## 取消订阅 Topic 主题

运行示例程序，当设备订阅 Topic 主题成功后，在数据模板模块上，点击 取消订阅主题 按钮，取消订阅属性，事件，和行为类型的 Topic `$thing/down/property/{ProductID}/{DeviceName}` `$thing/down/event/{ProductID}/{DeviceName}` `$thing/down/action/{ProductID}/{DeviceName}`。示例代码如下：
```
mDataTemplateSample.unSubscribeTopic(); // 取消订阅主题
```

观察Logcat日志。
```
I/TXMQTT_1.3.0: Starting unSubscribe topic: $thing/down/property/LWVUL5SZ2L/dahei
I/TXMQTT_1.3.0: Starting unSubscribe topic: $thing/down/event/LWVUL5SZ2L/dahei
I/TXMQTT_1.3.0: Starting unSubscribe topic: $thing/down/action/LWVUL5SZ2L/dahei
D/TXDataTemplateFragment: onUnSubscribeCompleted, status[OK], topics[[$thing/down/property/LWVUL5SZ2L/dahei]], userContext[MQTTRequest{requestType='subscribeTopic', requestId=3}], errMsg[unsubscribe success]
D/TXDataTemplateFragment: onUnSubscribeCompleted, status[OK], topics[[$thing/down/event/LWVUL5SZ2L/dahei]], userContext[MQTTRequest{requestType='subscribeTopic', requestId=4}], errMsg[unsubscribe success]
D/TXDataTemplateFragment: onUnSubscribeCompleted, status[OK], topics[[$thing/down/action/LWVUL5SZ2L/dahei]], userContext[MQTTRequest{requestType='subscribeTopic', requestId=5}], errMsg[unsubscribe success]
```
以上日志为 取消订阅 Topic 主题 成功。
