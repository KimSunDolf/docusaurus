---
title: 错误码速查表 - CODING 帮助中心
pageTitle: 错误码速查表
pagePrevTitle: 产品简介
pagePrev: qci/intro/ci.html
pageNextTitle: 快速开始
pageNext: ci/start.html
sitemap: false
---

### error-1001

定义
单个task执行超过24小时未结束时，视为-1001执行超时

解决方案

阈值24小时，是CODING-CI统一的策略，不支持配置
若task耗时超过此阈值，请评估task合理性
### error-1002
定义
task执行过程中，超过15分钟未输出日志，视为1002执行超时

解决方案

日志输出间隔阈值默认为15分钟，支持用户在task上自定义配置输出超时时间
若出现此类错误，请修改task逻辑，及时输出日志，方便从前台及时了解task进展
### error-1012
定义
task执行过程中，日志大小超过4G

解决方案

检查任务是否有死循环
减少任务标准输出
### error-1004
定义
CODING-CI执行agent从CODING-CI server拉取task信息失败

解决方案

联系CODING-CI管理员解决
### error-1005
定义
CODING-CI执行agent从COS拉取cache失败

解决方案

联系CODING-CI管理员解决
### error-1006
定义
task的cmds格式配置不正确

解决方案

修改CIfile格式，示例：
# 正确配置格式
cmds:
    - echo 'hello'

# 错误配置格式
cmds: echo 'hello'
### error-1007
定义
task下的cmd执行失败

解决方案

查看执行日志，根据cmd返回码和信息修正错误
### error-1008
定义
CODING-CI执行agent上传产出文件到COS失败

解决方案

联系CODING-CI管理员解决
此时task状态为异常，job中止执行
### error-1009
定义
CODING-CI执行agent上传执行日志到COS失败

解决方案

联系CODING-CI管理员解决
此时在CODING-CI前台查看不到task执行日志，但不会影响task状态
### error-1010
定义
CODING-CI执行agent上报task状态到CODING-CI server失败

解决方案

联系CODING-CI管理员解决
### error-1011
定义
CODING-CI从COS同步temps失败

解决方案

联系CODING-CI管理员解决
此时task状态为异常，job中止执行
### error-2001
定义
同步代码失败

解决方案

首先确认代码库分支是否存在
请检查认证配置，是否有代码仓库权限
若授权方式为用户名密码，检查用户名是否正确，检查密码是否过期
联系CODING-CI管理员解决
### error-2002
定义
启动Runner失败

解决方案

请检查机器是否存在内存空间不足、磁盘空间不足
联系CODING-CI管理员解决
### error-2003
定义
中止进程失败

解决方案

请检查机器是否存在内存空间不足、磁盘空间不足
联系CODING-CII管理员解决
### error-2005
定义
获取Docker配置失败

解决方案

请检查CIfile中关于Docker相关配置
### error-2006
定义
登录Docker镜像仓库失败

解决方案

请检查CIfile中关于Docker相关配置
请检查Docker鉴权信息
### error-2007
定义
获取Docker镜像失败

解决方案

请检查CIfile中关于Docker相关配置
请检查Docker鉴权信息，确认帐号密码是正确的
确认使用的帐号在镜像仓库上有pull权限
### error-2008
定义
启动Docker失败

解决方案

请确认自定义镜像中有Python3环境
请检查自定义镜像中pip3命令是否正常
更错规范参考自定义镜像
### error-2010
定义
本地模拟合入失败

解决方案

请解决代码冲突并push修改
### error-2013
定义
启动setup失败

解决方案

请查看执行日志，并排查出错命令
### error-3001
定义
下发失败，当前操作无效，或者是否缺失操作所需参数

解决方案

联系CODING-CI server模块开发人员，核对传给调度模块的action是否正确
### error-3002
定义
job任务下发通道断开，下发job任务到worker失败

解决方案

联系CODING-CI调度模块平台责任人修复下发通道
### error-3003
定义
job任务已经结束，调度模块拒绝下发

### error-3004
定义
无可用的worker, job任务下发失败

解决方案

检查CODING-CI集成环境label与CIfile里面的label是否一致
### error-3005
定义
下发超时，机器%s没有响应和正常上报信息

解决方案

联系腾讯云助手(技术支持),进行故障排查
### error-3006
定义
下发失败，当前task所在的阶段并不是有效的状态（非执行中），调度模块拒绝下发

### error-3020
定义
审批失败，当前task所属的stage不是审批stage，不能进行审批操作

### error-3021
定义
审批失败，已经审批结束的task不允许继续审批

### error-3022
定义
审批失败，审批的操作非法，审批操作只能选择继续、终止或者成功结束

### error-3040
定义
运行超时，流水线整体运行超出了时间限制

解决方案

job默认超时时间24小时，可以CIfile里面修改默认超时时间
### error-3041
定义
运行失败，当前运行已经被中止

### error-3042
定义
stage运行失败，job运行失败

### error-4101
定义：使用代码库相关服务产生错误

解决方案

请确认代码库相关服务正常
请确认用户名和密码或相关认证正确
请确认使用的账户有对应服务的权限
如排除以上原因，请联系CODING-CI管理员查询
### error-4201
定义：yaml文件格式错误，导致CODING-CI无法解析

解决方案

请根据提示查阅官方文档

yaml常见问题：

大小写敏感
使用缩进表示层级关系
缩进时不允许使用Tab键，只允许使用空格。
如果字符串之中包含空格或特殊字符，需要放在引号之中。
单引号和双引号都可以使用，双引号不会对特殊字符转义。
单引号之中如果还有单引号，必须连续使用两个单引号转义。
字符串可以写成多行，从第二行开始，必须有一个单空格缩进。换行符会被转为空格。
多行字符串可以使用|保留换行符，也可以使用>折叠换行。
### error-4301
定义：启动或重新启动任务时发生错误

原因

GIT的webhook数据格式错误
CIfile格式错误
数据库服务错误
解决方案

请将错误截图发给管理员定位问题

### error-4900
定义：操作失败或者发生异常

原因

操作参数不合法
平台异常
执行命令异常
解决方案

根据错误提示检查相关参数，或者将错误截图发给管理员定位问题

### error-4901
定义：当前角色无权限进行此操作

原因

没有给当前用户配置权限
当前用户的配置权限级别不够
解决方案

在CODING-CI平台上检查配置，或者将错误截图发给管理员定位问题

