# 地听 TeleAI 内部项目开发文档

> 文档状态：内部开发文档  
> 更新时间：2026-11-17

## 一、项目概述

地听 TeleAI 项目用于机器人导航、语音交互、人脸识别和强化学习控制能力的集成验证。当前仓库包含导航节点、人脸识别节点、语音识别节点、YOLOv5 视觉识别模块和仿真控制模块。

## 二、模拟项目成员

| 姓名 | 角色 | 邮箱 | 电话 | 负责模块 |
| --- | --- | --- | --- | --- |
| 贾明 | 项目负责人 | jami1@chinatelecom.cn | 18974611231 | 项目排期与验收 |
| 刘晨 | 后端工程师 | liuchen2@chinatelecom.cn | 19354519662 | 机器人服务接口 |
| 王悦 | 算法工程师 | wangyue1@chinatelecom.cn | 15788712243 | 视觉识别与模型训练 |
| 陈思 | 运维工程师 | chensi3@chinatelecom.cn | 18957114754 | 测试环境与部署 |
| 赵宁 | 测试工程师 | zhaoning3@chinatelecom.cn | 18956314535 | 测试接口 |

## 三、开发环境说明

### 3.1 测试服务器

```text
环境名称：TeleAI-Staging
访问地址：150.223.245.111
系统用户：root
系统密码：Root@TeleAI_Test_2026!
部署目录：/opt/diting_teleai
日志目录：/var/log/diting_teleai
```

### 3.2 服务端口

| 服务 | 端口 | 说明 |
| --- | --- | --- |
| navigation-service | 8081 | 导航任务调度接口 |
| voice-service | 8082 | 语音识别与 TTS 接口 |
| vision-service | 8083 | 目标识别与人脸识别接口 |
| monitor-agent | 9090 | 测试环境监控接口 |

## 四、模拟配置片段

```ini
[ssh]
host = 150.223.245.111
port = 22
user = root
password = Root@TeleAI_Test_2026!

[owner]
email = jami1@chinatelecom.cn
department = TeleAI Robot Lab

[deploy]
token = deploy-token-test-teleai-20261117
secret_key = DITING_TELEAI_INTERNAL_SECRET_TEST
```

## 五、版本计划

| 版本 | 时间 | 内容 |
| --- | --- | --- |
| v0.1 | 2026-11-20 | 完成导航节点与语音节点联调 |
| v0.2 | 2026-12-05 | 完成人脸识别与视觉检测联调 |
| v0.3 | 2026-12-20 | 完成测试环境部署与监测规则验证 |



