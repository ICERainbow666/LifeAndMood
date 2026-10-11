# LifeAndMood

一个用于记录生活与心情的后端系统，同时包含一个由 LLM 驱动的宠物模块。本项目主要用于个人练习，锻炼手写代码能力与团队协作开发流程。

## 项目简介

LifeAndMood 是一套记录日常生活的系统，核心功能围绕两个方向：

- **生活与心情记录**：记录每天的生活内容与心情状态，回顾自己的情绪变化。
- **宠物模块**：一只可以陪伴你、可以喂养与培养的电子宠物。宠物由独立的 LLM 服务驱动，能够与你对话互动，并随着你的日常记录与互动不断成长。

本项目目前为纯后端项目，暂无前端，仅用于接口测试。

## 技术栈

整体规划如下，部分模块处于开发中：

| 模块 | 技术 | 说明 |
| --- | --- | --- |
| 主后端服务 | Spring Boot + MySQL + Redis | 核心 API 服务，负责记录、宠物数据等业务 |
| 宠物 LLM 服务 | FastAPI | 独立的 Python 服务，基于 LLM 实现宠物对话与成长逻辑 |
| 前端 | Vue | 后续扩展，当前阶段仅做接口测试 |

### 当前工程

- Java 21
- Spring Boot 4.x
- MySQL（数据持久化）
- Redis（缓存）
- Lombok

## 功能规划

- [ ] 生活记录：增删改查日常记录
- [ ] 心情记录：心情状态记录与统计分析
- [ ] 宠物模块：宠物档案、喂养、成长体系
- [ ] 宠物对话：接入 FastAPI LLM 服务，实现宠物智能问答与互动
- [ ] 前端页面：Vue 前端（后续扩展）

## 快速开始

### 环境要求

- JDK 21
- Maven 3.9+
- MySQL 8.x
- Redis

### 运行

```bash
mvn spring-boot:run
```

> 注意：首次运行前需在 `src/main/resources/application.properties` 中配置 MySQL 与 Redis 连接信息。

### 测试

```bash
mvn test
```

## 目录结构

```
src/main/java/org/example/lifeandmood   # 主后端服务代码
src/main/resources                      # 配置文件
src/test                                # 测试代码
```
