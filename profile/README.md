# 人脸识别考勤系统

## 项目技术栈

- C++
- OpenCV
- React
- TypeScript
- Flutter
- Redis

## 仓库说明

```text
q-video：Web 摄像头
q-face-web：管理员 Web 界面
QFaceServer：后台服务
q-face-app：员工 App
```

## 系统功能结构图

```mermaid
graph LR
人脸识别考勤系统 --> 员工
人脸识别考勤系统 --> 后台管理
人脸识别考勤系统 --> 摄像头
员工 --> 打卡管理
员工 --> 登录
员工 --> 查看反馈结果
打卡管理 --> 查看打卡记录
打卡管理 --> 查看打卡人脸
打卡管理 --> 提出反馈
后台管理 --> 管理打卡
后台管理 --> 管理反馈
后台管理 --> 管理员工
管理打卡 --> 查看已打卡员工
管理打卡 --> 查看未打卡员工
管理反馈 --> 查看反馈
管理反馈 --> 处理反馈
管理员工 --> 查看员工信息
管理员工 --> 查看员工打卡记录
管理员工 --> 更新员工人脸
管理员工 --> 查看员工人脸
摄像头 --> 人脸检测
```

## 系统架构

```mermaid
C4Context
title 系统架构
Enterprise_Boundary(b0, "人脸识别考勤系统") {
  Person(admin, "管理员", "一个人脸识别系统管理员")
  System(Web, "人脸识别考勤系统 Web 页面", "允许管理员查询打卡记录、查看和修改人脸、查看和处理反馈等")
  System(Server, "后台服务", "负责处理请求和人脸检测和识别")
  SystemDb(MySQL, "MySQL", "存储数据")
  Person(worker, "员工", "一个人脸识别系统管理员")
  System(App, "人脸识别考勤系统手机 App", "允许员工查询打卡记录、提交反馈等")
  System(Video, "Web 摄像头", "人脸检测")
  SystemDb(Redis, "Redis", "存储 Token")
  BiRel(admin, Web, "use")
  BiRel(worker, App, "use")
  BiRel(worker, Video, "use")
  Rel(Web, Server, "request", "HTTP")
  Rel(App, Server, "request", "HTTP")
  Rel(Video, Server, "request", "HTTP")
  Rel(Server, MySQL, "request", "TCP")
  Rel(Server, Redis, "request", "TCP")
}
```

## 项目开发进度

```mermaid
gantt
dateFormat YYYY-MM-DD

section QFaceServer
开发:a1, 2023-01-12, 50d

section q-face-web
开发:a1, 2023-01-15, 22d

section q-video
开发:a1, 2023-02-14, 8d

section QFace
开发:a1, 2023-02-26, 5d
```
