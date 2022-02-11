# xia SQL (瞎注)

> 本插件仅只插入单引号，没有其他盲注啥的，而且结果返回的结果需要人工介入去判断是否存在注入，如果需要所有注入都测试，请把burp的流量转发到xray。

* burp 插件。
* 在每个参数后面填加一个单引号，两个单引号。
* 由于不会java，且又是用java写的，代码太烂，就不开源了。

## 插件使用描述
* 返回 ✔️ 代表两个单引号的长度和一个单引号的长度不一致
* 返回 ✔️ ==> ？ 代表着 原始包的长度和两个双引号的长度相同且和一个单引号的长度不同，表明很可能是注入。


**********
### 2022-2-11
#### xia SQL 1.3
* 更新了 原始包的长度和两个双引号的长度相同且和一个单引号的长度不同就返回 ✔️ ==> ？


![image](https://user-images.githubusercontent.com/30351807/153584280-93d34705-b02f-4fc3-9acc-5cdd71d36cb8.png)


**********
### 2022-2-11
#### xia SQL 1.2
* 更新支持json格式

![image](https://user-images.githubusercontent.com/30351807/153567877-479a0e15-9d6c-43f5-84d9-80c5dfb6fd03.png)


**********
### 2022-2-10
#### xia SQL 1.1
* 更新了序列号
* 更新了有变化 打勾
* 更新了如果那个数据包没有参数，那就忽略。这样开 proxy 模式 就不会一堆包了。

![image](https://user-images.githubusercontent.com/30351807/153390045-2b3769f6-151b-45c0-a555-53cda4fef2f2.png)


**********
# 图片展示

![image](https://user-images.githubusercontent.com/30351807/153139897-08e6b69b-f129-4fab-a62e-037351d7c60f.png)

![image](https://user-images.githubusercontent.com/30351807/153139950-a4f51f4b-e39d-459d-91b8-e326c2c74c29.png)


![image](https://user-images.githubusercontent.com/30351807/153139522-b9af5d35-36a3-4204-b2f4-7b6a11253d41.png)
