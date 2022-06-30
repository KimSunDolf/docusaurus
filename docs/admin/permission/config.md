---
title: 权限配置 - CODING 帮助中心
pageTitle: 权限配置
pagePrevTitle: true
pagePrev: true
pageNextTitle: true
pageNext: true
alias: 
-   admin/permission/migrate.html  
-   admin/permission.html 
---

{% tabs tab,1 %} 名字为tab，默认在第1个选项卡，如果是-1则隐藏
<!-- tab 旧版权限方案-->

本文适用于 2022 年 8 月 1 日之前注册、仍在为每个项目单独配置权限方案的团队。


### [配置团队权限](#config-team-permission)

团队负责人/管理员可进入「团队设置中心」->「全局设置」->「组织与成员」->「权限配置」更改团队成员权限配置，为团队量身打造高效灵活的权限管理体系。

![](https://help-assets.codehub.cn/enterprise/20210929165448.png)

-   默认给系统用户组分配了对应权限，可由团队负责人/管理员对其默认权限进行修改。

-   成员的权限为其在各个用户组的权限之和（例如：某团队成员既是管理员也是某一自定义用户组成员，该团队成员权限为管理员权限加上自定义用户组权限之和）。

-   团队负责人/管理员修改系统用户组/自定义用户组权限后，被修改权限的成员在强制刷新页面后即可生效新权限。

#### [系统分组](#system-group)

系统分组分为团队负责人、管理员、普通成员三组，且系统分组不支持删除。


| 用户组 |用户数量| 对应权限 | 备注|
| ------------ | ------------- | ------------- |------------- |
| 团队负责人 |唯一| 默认拥有团队所有权限 |默认为团队创建者|
团队管理员 |一个或多个| 默认拥有除「变更团队负责人」和「设置管理员」外的所有权限|由团队负责人指定|
团队普通成员 | 一个或多个|默认拥有「创建项目」、「访问令牌」、「应用授权」、「应用管理」等权限|由团队负责人/管理员指定|


#### [自定义用户组](#custom-group)

当团队成员架构比较复杂，涉及不同模块时，可由团队负责人/管理员创建自定义用户组给不同成员分配不同的权限。

1.  在「团队设置中心」->「全局设置」->「组织与成员」->「权限配置」中，点击蓝色 + 号，输入用户组名称完成确认，即可创建自定义用户组。

> 新建的用户组默认没有任何功能权限，需要手动勾选需要的功能权限。

![](https://help-assets.codehub.cn/enterprise/20210929165758.png)

2.  点击右上角「添加成员」按钮，可将指定成员加入该用户组。

![](https://help-assets.codehub.cn/enterprise/20210929165907.png)

3.  在权限列表中，按需为该用户组添加权限并保存。该用户组成员在强制刷新页面后即可生效新权限。

![](https://help-assets.codehub.cn/enterprise/20210914154412.png)

4.  自定义用户组支持重命名和删除操作。

![](https://help-assets.codehub.cn/enterprise/20210914154341.png)

### [配置项目权限](#config-project-permission)

项目权限需由项目管理员（或具有配置权限的用户）进入具体项目进行配置。详情请参考[项目权限配置](/docs/project-settings/permission.html)。

<!-- endtab -->
<!-- tab 新版权限方案-->

本文适用于 2022 年 8 月 1 日之后注册、使用全局项目权限配置方案的团队。

在新版权限管理中，用户组以及团队、项目级别的权限均可在「团队设置中心」->「全局设置」->「组织与成员」中完成配置。

![](https://help-assets.codehub.cn/enterprise/20220629141302.png)

### [前提条件](#prerequisite)

在执行下文所述操作之前，请确保你所在的团队权限组拥有对应的权限点配置。如缺少对应权限，请联系团队负责人或管理员进行授权。

![](https://help-assets.codehub.cn/enterprise/20220630152131.png)

### [配置团队权限方案](#config-team)

在新版权限管理中，团队权限的配置方法与旧版类似。新增的亮点为：
*   新建自定义权限组时，可通过参考权限组快速填充权限点配置。

![](https://help-assets.codehub.cn/enterprise/20220630115654.png)

*   支持添加用户组、部门至团队权限组，快速实现批量授权。

![](https://help-assets.codehub.cn/enterprise/20220630120441.png)

### [配置项目权限方案](#config-team)

在升级至新版权限管理方案之后，你可以在「团队设置中心」->「全局设置」->「组织与成员」->「项目权限方案」中按照以下步骤重新规整团队的项目权限配置。

#### [1.  查看项目权限组引用情况](#view)

权限管理功能升级之后，可能会产生冗余的项目权限组。你可以通过下文查看此类冗余权限组正在被哪些项目所使用，再重新调整项目权限配置。

在项目权限组列表，点击指定权限组的「引用情况」按钮，即可查看该权限组在哪些项目被使用。

![](https://help-assets.codehub.cn/enterprise/20220630134904.png)

点击具体项目的角色成员数量，即可进入「项目成员管理」页签查看指定权限组被该项目的哪些用户/用户组/部门所关联。

![](https://help-assets.codehub.cn/enterprise/20220630135028.png)

#### [2.  查看项目权限组引用情况](#view)

在新版权限管理中，系统预设项目预设权限组不支持删除或修改。如有必要，你可以自定义合适的项目权限组。

在「团队设置中心」->「全局设置」->「组织与成员」->「项目权限方案」中，点击右上角「添加权限组」。

![](https://help-assets.codehub.cn/enterprise/20220630134658.png)

输入权限组名称和描述，指定参考权限组，保存即可完成权限组创建。

#### [3.  编排用户组](#view)

新版权限管理支持将一个用户组或部门直接加入项目并分配权限，实现批量授权。在分配项目权限之前，建议你先组织并梳理好团队成员，**将需要授权相同权限点的成员编排为一个用户组**，后续直接给该用户组授权。

在「团队设置中心」->「全局设置」->「组织与成员」->「用户组」中，点击右上角「添加用户组」，输入用户组名称和描述，即可创建用户组。

![](https://help-assets.codehub.cn/enterprise/20220120140242.png)

创建成功的用户组会出现在用户组列表。点击用户组的「添加成员」按钮，可添加团队成员至该用户组。你可以通过搜索框指定成员，或按照部门或项目批量添加成员。

![](https://help-assets.codehub.cn/enterprise/20220120141453.png)


#### [4.  为成员分配项目权限](#view)

新版权限管理提供了灵活的项目成员管理视角，支持以下任一方式为团队成员分配项目权限：

*   在「项目权限方案」->「项目成员管理」中，选择指定项目，快速将多个用户、用户组或部门加入当前项目并设置权限。

![](https://help-assets.codehub.cn/enterprise/20220630135956.png)

*   在「项目权限方案」->「项目管理」中，选择指定的用户、用户组或部门，快速将其加入多个项目并设置权限。

![](https://help-assets.codehub.cn/enterprise/20220630141341.png)

在新版权限管理界面重新配置团队与项目权限之后，你便可以将升级之后产生的冗余权限数据删除。

<!-- endtab -->
{% endtabs %}



