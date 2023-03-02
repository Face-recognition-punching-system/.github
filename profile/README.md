# 人脸识别考勤系统

## 项目技术栈

- C++
- OpenCV
- React
- TypeScript
- Less
- QML
- Redis


## 系统功能结构图

```mermaid
graph LR
思维导图--> 第一部分
第一部分-->1.1小节
第一部分-->1.2小节	
思维导图--> 第二部分
第二部分-->2.2小节
思维导图--> 第三部分
第三部分--> 3.1小节
思维导图--> 若干
```

## 系统架构

```mermaid
    C4Context
      title 系统架构
      Enterprise_Boundary(b0, "BankBoundary0") {
        Person(admin, "管理员", "一个人脸识别系统管理员")
        Person(worker, "员工", "一个人脸识别系统管理员")
        System(systemA, "人脸识别考勤系统 Web 页面", "允许管理员查询打卡记录、查看和修改人脸、查看和处理反馈等")
        System(systemB, "人脸识别考勤系统手机 App", "允许员工查询打卡记录、提交反馈等")
        System(SystemC, "", "")
        Container(D, "", "")
      }
```

## 项目开发流程

```mermaid
gantt
dateFormat YYYY-MM-DD

section 项目A
任务1 :a1, 2018-06-06, 30d
任务2 :after a1 , 20```
