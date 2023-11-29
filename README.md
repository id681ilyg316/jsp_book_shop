## 本项目实现的最终作用是基于JSP图书商城项目管理系统
## 分为2个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 图书管理
 - 图书类别管理
 - 增删改查用户
 - 管理员登录
 - 管理员角色
 - 订单管理
### 第2个角色为用户角色，实现了如下功能：
 - 修改个人信息
 - 提交订单
 - 查看分类
 - 查看订单
 - 查看购物车
 - 用户注册
 - 用户详情
 - 用户首页
## 数据库设计如下：
# 数据库设计文档

**数据库名：** book

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [t_admin_pqy](#t_admin_pqy) |  |
| [t_book_pqy](#t_book_pqy) |  |
| [t_catelog_pqy](#t_catelog_pqy) |  |
| [t_jieyue_pqy](#t_jieyue_pqy) |  |
| [t_user_pqy](#t_user_pqy) |  |

**表名：** <a id="t_admin_pqy">t_admin_pqy</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | userId |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | username |   varchar   | 255 |   0    |    N     |  N   |       | 用户名  |
|  3   | userPw |   varchar   | 255 |   0    |    N     |  N   |       | 密码  |
|  4   | userRole |   varchar   | 255 |   0    |    N     |  N   |       |   |

**表名：** <a id="t_book_pqy">t_book_pqy</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    N     |  N   |       | 名字  |
|  3   | zuozhe |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  4   | chubanshe |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  5   | chubanriqi |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  6   | isbm |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  7   | price |   varchar   | 255 |   0    |    N     |  N   |       | 价格  |
|  8   | yeshu |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  9   | kucun |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  10   | catelog_id |   int   | 10 |   0    |    N     |  N   |       |   |
|  11   | del |   varchar   | 255 |   0    |    N     |  N   |       | 是否删除  |

**表名：** <a id="t_catelog_pqy">t_catelog_pqy</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    N     |  N   |       | 名字  |
|  3   | jieshao |   varchar   | 255 |   0    |    N     |  N   |       | 介绍  |
|  4   | del |   varchar   | 255 |   0    |    N     |  N   |       | 是否删除  |

**表名：** <a id="t_jieyue_pqy">t_jieyue_pqy</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | user_id |   int   | 10 |   0    |    N     |  N   |       | 用户ID  |
|  3   | book_id |   int   | 10 |   0    |    N     |  N   |       | 图书ID  |
|  4   | jieyueshuliang |   int   | 10 |   0    |    N     |  N   |       |   |
|  5   | jieyueshijian |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  6   | shifouguihuan |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  7   | guihuanshijian |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  8   | del |   varchar   | 255 |   0    |    N     |  N   |       | 是否删除  |

**表名：** <a id="t_user_pqy">t_user_pqy</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | name |   varchar   | 255 |   0    |    N     |  N   |       | 名字  |
|  3   | sex |   varchar   | 255 |   0    |    N     |  N   |       | 性别  |
|  4   | age |   varchar   | 255 |   0    |    N     |  N   |       | 年龄  |
|  5   | address |   varchar   | 255 |   0    |    N     |  N   |       | 地址  |
|  6   | tel |   varchar   | 255 |   0    |    N     |  N   |       | 电话  |
|  7   | email |   varchar   | 255 |   0    |    N     |  N   |       | 邮箱  |
|  8   | jiehao |   varchar   | 255 |   0    |    N     |  N   |       |   |
|  9   | del |   varchar   | 255 |   0    |    N     |  N   |       | 是否删除  |

**运行不出来可以微信 javape 我的公众号：源码码头**
