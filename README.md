# owep

#### 介绍
Online Wisdom Education Platform

#### 软件架构
本系统采用Maven进行构建，并且基于Spring Boot进行开发，采用多模块结构，按软件分层思想进行架构，整个项目分为如下模块：
| owep                      | 父级项目     |
|---------------------------|----------|
| owep-admin-entity         | 实体类模块    |
| owep-admin-web-dao        | 持久层模块    |
| owep-admin-web-service    | 业务层模块    |
| owep-admin-web-dto        | 数据传输对象模块 |
| owep-admin-web-controller | 页面模块     |
| owep-admin-utils          | 工具类模块    |
| owep-admin-web-vo         | 值对象模块    |

如下图：
![输入图片说明](https://images.gitee.com/uploads/images/2020/0628/224143_15bc2620_1104083.png "屏幕截图.png")

业务模块主要有：
1. 系统配置
2. 用户管理
3. 权限管理
4. 资源管理
5. 培养方案
6. 班级管理
7. 授课管理
8. 考试管理
9. 考评管理
10.数据分析
11.组织机构
12.通知公告
13.咨询管理
14.意向客户
15.操作日志

#### DTO的作用、编写原则和使用
1. 作用
    * 可以按页面所需来组装数据，而无需去修改Entity类
    * 可以有效地防止后台数据库结构的泄漏
    * 通过业务层的组装，可以有效减少调用的次数

2. 编写原则
    * 中间表可以编写对应的DTO，比如：只包含两个外键属性
    * 报表类的数据可以编写对应的DTO
    * 只需要部份实体类中的数据，可以编写对应的DTO
    * 如果多个页面都需要DTO，可以考虑整合成一个DTO，当然，如果个性化太强，则建议定义多个DTO
    
3. 使用
    * 在业务层中，如果需要返回数据或数据集，则应该是 DTO对象或是DTO的集合
    * 在业务层中，方法的参数，建议继续使用 Entity 类型，需要注意的是，有些属性是需要我们手动给值的，比如：version, createTime等 页页元素中没有收集的信息.



#### 使用说明

1.  在 owep-admin-web-controller模块中启动 spring boot类
2.  打开浏览器访问
3.  其它模块中，可以使用单元测试

#### 参与贡献

1.  git clone -b dev_v5 仓库地址
2.  在本地新建 Feat_xxx 分支
3.  提交代码
4.  新建 Pull Request


#### 项目组成员

1. 韦文虎
2. 陆志悦
3. 惠子岩
4. 李冉
5. 林煜翔
6. 夏汉清
7. 陈佳豪
8. 查辰玺
9. 卢涵彬