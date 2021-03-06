* [腾讯云物联网通信 Android-SDK](#腾讯云物联网通信-Android-SDK)
  * [基于TCP的MQTT设备接入](#基于TCP的MQTT设备接入)
  * [动态注册](#动态注册)
  * [RRPC同步通信](#RRPC同步通信)
  * [广播通信](#广播通信)
  * [网关功能](#网关功能)
  * [固件升级](#固件升级)
  * [设备日志上报](#设备日志上报)
  * [网关设备拓扑关系](#网关设备拓扑关系)
  * [基于Websocket的MQTT设备接入](#基于Websocket的MQTT设备接入)
  * [设备互通](#设备互通)
  * [设备影子](#设备影子)


# 腾讯云物联网通信 Android-SDK

腾讯云物联网通信IoT Hub Android-SDK 依靠安全且性能强大的数据通道，为物联网领域开发人员提供设备终端(如传感器, 执行器, 嵌入式设备或智能家电等等)和云端的双向通信能力，基于规则引擎和腾讯云产品打通，实现设备之间的互动、设备的数据上报和配置下发。

以下为SDK各项功能对应的文档。

## 基于TCP的MQTT设备接入
请参考 [基于TCP的MQTT设备接入.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/基于TCP的MQTT设备接入.md) 文档，介绍如何在腾讯云物联网通信IoT Hub控制台创建设备, 并结合 SDK Demo 快速体验设备端通过 MQTT 协议连接到腾讯云IoT Hub, 发送和接收消息。

## 动态注册
请参考 [动态注册.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/动态注册.md) 文档，介绍动态注册功能，并结合 SDK Demo 体验动态注册使用，方便用户为同一批设备烧录相同的配置信息。

## RRPC同步通信
请参考 [RRPC同步通信.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/RRPC同步通信.md) 文档，介绍RRPC同步通信功能，利用 RRPC（Revert RPC）实现同步通信机制。

## 广播通信
请参考 [广播通信.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/广播通信.md) 文档，介绍广播通信功能，订阅了相应的广播 Topic 的在线设备便可收到服务器通过广播 Topic 发布的广播消息。

## 网关功能
请参考 [网关功能.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/网关功能.md) 文档，介绍如何在腾讯IoT Hub控制台申请网关设备并绑定子设备, 并结合 SDK Demo 快速体验网关设备通过 MQTT 协议连接到腾讯云IoT Hub, 代理子设备上下线，发送和接收消息。

## 固件升级
请参考 [固件升级.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/固件升级.md) 文档，介绍固件升级功能，并结合 SDK Demo 展示固件升级的流程和功能

## 设备日志上报
请参考 [设备日志上报.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/设备日志上报.md) 文档，介绍设备日志上报功能及使用。

## 网关设备拓扑关系
请参考 [网关设备拓扑关系.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/网关设备拓扑关系.md) 文档，介绍查看网关设备拓扑中子设备的关系。

## 基于Websocket的MQTT设备接入
请参考 [基于Websocket的MQTT设备接入.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/基于Websocket的MQTT设备接入.md) 文档，结合 SDK Demo 快速体验设备在 WebSocket 协议的基础之上使用 MQTT 协议连接到腾讯云IoT Hub。

## 设备互通
请参考 [设备互通.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/设备互通.md) 文档，介绍一个智能家居设备互通的场景, 结合 SDK Demo 快速体验基于IoT Hub的消息转发和规则引擎实现设备之间的联动。

## 设备影子
请参考 [设备影子.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/设备影子.md) 文档，介绍设备影子功能，结合 SDK Demo 展示影子的数据流和功能。

