## 上班打卡后台


### 概述

这是个WEB项目，主要为上班打卡项目提供a 产品介绍网站 b 管理后台 c 与APP的API，你需要通过以下步骤成功运行起来

这是一个使用Python开发WEB程序教学示范项目，欢迎你参与，可以邮件联系说明最后的产品经理请求加入

### 关于

项目基于Python的bottle web开发框架，前端基于bootstrap (http://getbootstrap.com) 构建

### 安装

* 1 安装Python (http://python.org)
* 2 安装pip (Python的Package管理工具, http://www.pip-installer.org)
* 3 通过pip安装bottle (一个轻量级的Python web开发框架, http://bottlepy.org)
* 4 运行python main.py, 在浏览器输入http://localhost:8080 顺利地话即可顺利启动


### 设计截图
- UE流程设计图
![UE设计](https://raw.githubusercontent.com/NANNING/Shangbandaka-backend/master/design/ue.png "UE设计")

- 登录界面
![登录界面](https://raw.githubusercontent.com/NANNING/Shangbandaka-backend/master/design/0-login.jpg "登录界面")

- 开通打卡服务
![开通打卡服务](https://raw.githubusercontent.com/NANNING/Shangbandaka-backend/master/design/1-register.png "开通打卡服务")

- 管理系统
![管理系统](https://raw.githubusercontent.com/NANNING/Shangbandaka-backend/master/design/2-manager.png "管理系统")


其他未展示的页面（如部门管理、更改密码等）根据上述设计稿所实现的规则灵活处理

### API for .net backend

#### 验证 IMEI 

/api/reimei 通过员工id查询绑定手机的imei串

@parameters: id=<员工id>

@return 
{
"errno": int <错误代码>, 
"msg": imei串或者错误信息
}

#### 登录

/api/mlogin 通过员工id查询绑定手机的imei串

@parameters: name=<username>,pwd=<password>

@return 
{
"errno": int <错误代码>, 
"msg": string <提示消息>
"ret": {
    "id":"用户id",
    "token":"<登录成功后后台生成的token验证串>"
    }
}

#### 请假请求

/api/reqingjia 通过员工id和公司id

@parameters: id 员工id  cid 公司id Start开始时间 end结束时间 reason 原因

@return 
{
"errno": int <错误代码>, 
"msg": string <提示消息>

}

### 签到
/api/redaka  通过员工id和公司id
@parameters: id 员工id  cid 公司id lat 纬度 lon经度

@return 
{
"errno": int <错误代码>, 
"msg": string <提示消息>

}

### 联系
- 项目网站 : http://nanning.github.io
- 产品经理: [River](https://github.com/riverfor) - riverfor at gmail.com
- 项目经理: [冰哥](https://github.com/Airfly)
- 开发者 : [Chifeng](https://github.com/chifeng)
- 网站设计师 : [廖炎](https://github.com/liaoyanly)
