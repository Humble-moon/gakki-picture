# Gakki Picture 图片管理系统

## 项目简介

Gakki Picture 是一个功能强大的图片管理系统，支持图片上传、管理、搜索、审核等核心功能，并集成了 AI 扩图等智能特性。系统采用前后端分离架构，提供了友好的用户界面和丰富的 API 接口。

## 项目结构

```
Java-gakki-picture/
├── gakki-picture-backend/         # 后端项目（传统架构）
├── gakki-picture-backend-ddd/     # 后端项目（DDD 架构）
└── gakki-picture-frontend/        # 前端项目
```

## 技术栈

### 前端
- Vue 3 + TypeScript
- Ant Design Vue
- Vite
- ECharts
- Vue Router
- Pinia

### 后端
- Spring Boot 2.7.6
- MyBatis-Plus
- Redis
- ShardingSphere（分库分表）
- WebSocket
- Sa-Token（认证授权）
- 腾讯云 COS（对象存储）
- 阿里云 AI（图片处理）

### 数据库
- MySQL

## 核心功能

### 图片管理
- 图片上传（支持本地文件和 URL 上传）
- 图片删除、更新、编辑
- 图片批量操作
- 图片审核流程

### 图片搜索
- 以图搜图
- 以色搜图
- 标签和分类搜索

### 智能特性
- AI 扩图功能
- 图片色彩分析

### 空间管理
- 个人空间
- 空间权限管理
- 空间成员管理

### 系统管理
- 用户认证和授权
- 角色权限控制
- API 接口文档

## 快速开始

### 前端项目

1. 进入前端项目目录
```bash
cd gakki-picture-frontend
```

2. 安装依赖
```bash
npm install
```

3. 启动开发服务器
```bash
npm run dev
```

4. 构建生产版本
```bash
npm run build
```

### 后端项目

1. 进入后端项目目录
```bash
cd gakki-picture-backend
```

2. 配置数据库连接（修改 `application.yml`）
```yaml
spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    url: jdbc:mysql://localhost:3306/gakki_picture
    username: root
    password: root
```

3. 配置对象存储（修改 `application.yml`）
```yaml
## 对象存储配置（需要从腾讯云获取）
cos:
  client:
    host: xxx
    secretId: xxx
    secretKey: xxx
    region: xxx
    bucket: xxx

# 阿里云AI配置
aliYunAi:
  apiKey: xxx
```

4. 执行数据库脚本（`sql/create_table.sql`）

5. 启动后端服务
```bash
mvn spring-boot:run
```

## API 文档

后端服务启动后，可以通过以下地址访问 API 文档：

```
http://localhost:8123/api/doc.html
```

## 系统架构

### 前端架构
- 基于 Vue 3 + TypeScript 开发
- 使用 Ant Design Vue 组件库
- 采用 Pinia 进行状态管理
- 使用 Vue Router 进行路由管理

### 后端架构
- 基于 Spring Boot 2.7.6 开发
- 使用 MyBatis-Plus 进行数据库操作
- 使用 Redis 进行缓存和会话管理
- 使用 ShardingSphere 进行分库分表
- 使用 Sa-Token 进行认证授权
- 集成腾讯云 COS 进行对象存储
- 集成阿里云 AI 进行图片处理

### 部署架构
- 前端：静态文件部署到 CDN 或 Web 服务器
- 后端：部署到 Java 应用服务器（如 Tomcat）
- 数据库：MySQL 集群
- 缓存：Redis 集群
- 对象存储：腾讯云 COS

## 核心模块

### 图片模块
- 图片上传与存储
- 图片元数据管理
- 图片搜索与检索
- 图片审核与管理

### 空间模块
- 空间创建与管理
- 空间成员管理
- 空间权限控制

### 用户模块
- 用户注册与登录
- 用户信息管理
- 角色权限管理

### AI 模块
- 图片扩图
- 图片色彩分析

## 安全特性

- 基于 Sa-Token 的认证授权
- 细粒度的权限控制
- 接口访问频率限制
- 敏感信息加密存储
- XSS 和 CSRF 防护

## 性能优化

- 图片懒加载
- 缓存策略（本地缓存 + Redis 缓存）
- 分库分表（基于 ShardingSphere）
- 异步处理（基于 Disruptor）
- 数据库索引优化

## 开发规范

### 前端开发规范
- 使用 TypeScript 进行类型检查
- 遵循 ESLint 代码规范
- 使用 Prettier 进行代码格式化
- 组件化开发

### 后端开发规范
- 遵循 Spring Boot 开发规范
- 使用 MyBatis-Plus 进行数据库操作
- 分层架构设计
- 异常统一处理
- 日志规范

## 贡献指南

1. Fork 本项目
2. 创建特性分支
3. 提交代码
4. 推送到分支
5. 打开 Pull Request

## 许可证

本项目采用 MIT 许可证。

## 联系方式

- 项目地址：https://github.com/yourusername/Java-gakki-picture
- 作者：Gakki
- 邮箱：your.email@example.com
