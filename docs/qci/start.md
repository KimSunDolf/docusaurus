---
title: 快速开始
pageTitle: 快速开始
pagePrevTitle: 产品能力
pagePrev: qci/intro/ci.html
pageNextTitle: 触发方式
pageNext: ci/start.html
sitemap: false
sidebar_position: 2
---

创建[项目](/docs/start/project.html)后，点击左侧菜单栏的“持续集成”开始使用。下文将引导你通过模板创建一个简单的流水线自动化发布制品，并简要概述其中的基础功能。点击页面中的“创建流水线”按钮开始进行配置。

![](https://help-assets.codehub.cn/enterprise/20220713152146.png)

### [1. 新建流水线模板](#init)

选择系统模板中的 `Python + Flask + Docker` 项目，填写名称与选择代码库。流水线本质上由配置文件生成，在页面左侧可以通过图形化方式选定所检出的代码源与需推送的目标制品库，在右侧则展示了以 YAML 语言所生成的 CIFile。对构建过程的所有更改本质上都会体现在 CIFile 中。有关于 CIFile 的语法说明请参考[此文档](/docs/qci/cifile.html)。

![](https://help-assets.codehub.cn/enterprise/20220713161237.png)

### [2. 选择代码源](#source-code)

标签功能用于为流水线分类，方便后续检索中快速找到目标构建计划。按照提示依次输入任务名，在代码仓库栏选择“示例代码”作为代码源，系统将自动在您的项目中新建立一个示例代码仓库。

### [3. 选择制品库](#artifacts)

流水线运行结束后会生成一个应用制品，在这里选择拟推送的目标 Docker 制品库。若项目内尚未存在制品库，可以利用快捷方式进行新建。

![](https://help-assets.codehub.cn/enterprise/20220713161647.png)

### [4.  填写远端服务器（可选步骤）](#remote-server)

填写拟部署的远端服务器信息，包含 IP 地址及端口等信息。待流水线运行完成后将自动发送制品至远端服务器中，通过一个网址 + 端口号便可预览发布后的效果。CODING 采用转义后的公钥作为流水线的 SSH 登录凭据，因此需要将 SSH 登录凭据录入至项目设置中的“凭据管理”中，点击“凭据录入”按钮进行录入。如果暂时不需要部署到远端服务器，可跳过此步骤。

![](https://help-assets.codehub.cn/enterprise/20220713171044.png)

点击右上角的触发按钮，在任务执行页面可以查看配置任务与任务的执行详情、执行历史等。

![](https://help-assets.codehub.cn/enterprise/20211020173707.png)

### [5. 点击创建并触发流水线](#results)

点击保存流水线，你可以在新跳转页面查看本次流水线完整概览。确认无误后点击右上角的“立即构建”按钮进行触发。

![](https://help-assets.codehub.cn/enterprise/20220713171803.png)

点击构建记录可以查看流水线上每一个阶段是否运行成功，还可以看到每一个步骤命令的具体的执行效果和日志。

![](https://help-assets.codehub.cn/enterprise/20220713171857.png)

流水线运行后将自动保存本次运行过程中所使用的的启动参数、环境变量等信息。此部分信息主要用于描述本次流水线所使用的的环境与资源，方便后期排障与优化。

![](https://help-assets.codehub.cn/enterprise/20220713173648.png)

### [可选模板](#another-template)

除了本文中的 `Python + Flask + Docker` 项目，持续集成还内置了许多模板，你可以按照实际的开发需求选择对应的模板。

-   Java + Spring + Docker

    该模版演示基于 Java + Spring 实现全自动检出代码 -> 单元测试 -> 构建 Docker 镜像 -> 推送到 Docker 制品库 -> 部署到远端服务器

-   Nodejs + Express + Docker

    该模版演示基于 Nodejs + Express 实现全自动检出代码 -> 单元测试 -> 构建 Docker 镜像 -> 推送到 Docker 制品库 -> 部署到远端服务器

-   GoLang + Gin + Docker

    该模版演示基于 GoLang + Gin 实现全自动检出代码 -> 单元测试 -> 构建 Docker 镜像 -> 推送到 Docker 制品库 -> 部署到远端服务器

-   .Net Core + Docker

    该模版演示基于 .Net Core 实现全自动 检出代码 -> 单元测试 -> 编译构建 -> 构建 Docker 镜像 -> 推送到 Docker 制品库 -> 部署到远端服务器 整个流程。

-   PHP + Laravel + Docker

    该模版演示基于 PHP + Laravel 实现全自动 检出代码 -> 单元测试 -> 构建 Docker 镜像 -> 推送到 Docker 制品库 -> 部署到远端服务器 整个流程。

-   Java + Spring + Maven

    该模版演示基于 Java + Spring 实现全自动检出代码 -> 编译构建 -> 单元测试 -> 推送到 Maven 制品库
