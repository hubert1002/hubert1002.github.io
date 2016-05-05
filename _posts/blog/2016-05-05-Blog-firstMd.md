---
layout: post
title: Messaging流程
category: ZXMessage
tags: ZXMessage
keywords:
description: 掌信消息通道建立和维护
---

##一 消息通道的建立
---  

流程：
> 1 访问Dispatch接口得到 Host Port 
> 2 如果SK为空，获取SK
> 2 创建Connection，设置监听回调，设置 
> 3 Login 
> 4 Ping

##二 消息通道的维护
---  

通过ping包机制，每隔4min发一个ping包，如果两次

##三 检查连接是否可用时机，以及后续操作
---  

> 1.网络变为可用
> 2.手机状态改变，主要是监听各种系统广播

```  
                <action android:name="android.intent.action.BOOT_COMPLETED" />
                <action android:name="android.provider.Telephony.SMS_RECEIVED" />
                <action android:name="android.intent.action.USER_PRESENT" />
                <action android:name="android.intent.action.BATTERY_CHANGED" />
```  

> 3.登录成功后，去发起连接
> 4.应用启动时
> 5.各个继承自BaseActionBarActivity的界面onResume时
> 6.当访问网络接口，返回SK失效（resultCode = 401）时，清空SK，并检查重连


> 标签  

```
//test
if(true){
  
}
val tuple = (1, ture, "abc")  
tuple._1
```  

#### package scala.collection  


![collection](/public/img/collection.png)  
