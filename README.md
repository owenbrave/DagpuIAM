# weixin450-springboot校园外卖点餐平台小程序

## 前言

本项目是基于Java语言，结合Spring Boot、Spring MVC、MyBatis等主流框架，以及微信小程序、Uniapp等前端技术，开发的一款适用于校园场景的外卖点餐平台。项目涵盖了用户点餐、商家接单、配送员配送等环节，旨在为校园师生提供便捷、高效的外卖点餐服务。

## 内容介绍

本项目主要包括以下功能模块：

1. 用户模块：注册、登录、查看菜单、下单、查看订单等。
2. 商家模块：注册、登录、发布菜品、接单、管理订单等。
3. 配送员模块：注册、登录、接单、配送、查看收入等。
4. 管理员模块：管理用户、商家、配送员信息，查看平台数据等。

## 技术介绍

- 语言：Java
- 使用框架：Spring Boot、Spring MVC、MyBatis、微信小程序
- 前端技术：JS、Vue、CSS3、Uniapp
- 开发工具：IDEA/Eclipse、Uniapp
- 数据库：MySQL 5.7/8.0
- 数据库管理工具：phpstudy/Navicat
- JDK版本：jdk1.8
- Maven：apache-maven 3.8.1-bin
- 前端环境：Node.Js 12\14\16

## 核心代码

以下为项目中的一段核心代码，展示了商家接单的处理逻辑：

```java
@Service
public class OrderService {

    @Autowired
    private OrderMapper orderMapper;

    // 商家接单
    public boolean receiveOrder(int orderId, int businessId) {
        // 检查订单是否存在且未接单
        Order order = orderMapper.selectByPrimaryKey(orderId);
        if (order != null && order.getStatus() == 0) {
            // 更新订单状态为已接单
            order.setStatus(1);
            order.setBusinessId(businessId);
            orderMapper.updateByPrimaryKey(order);
            return true;
        }
        return false;
    }
}
```

## 免费源码获取

```
5000套系统成品在线演示视频，复制到流浪器： 
```
```
https://www.yuque.com/yuqueyonghux32e1j/kxdc9g/ad8oz3bamkxmay0e#Cxun
```
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

## 项目截图
