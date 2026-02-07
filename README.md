# 前言

随着后疫情时代的到来，高校宿舍管理面临着新的挑战与需求。为此，我们开发了这款基于Spring Boot的高校宿舍管理系统小程序，旨在为高校宿舍管理提供便捷、高效的解决方案。

# 内容介绍

本项目是一款集宿舍管理、疫情防控、生活服务等功能于一体的微信小程序。通过本系统，可以实现以下功能：

1. 宿舍基本信息管理：包括宿舍楼栋、房间、床位信息的管理与查询。
2. 学生信息管理：实现对学生基本信息、入住信息、健康状态的管理与查询。
3. 疫情防控：实时更新学生健康状况，记录体温、健康码等信息。
4. 生活服务：提供报修、投诉、建议等功能，方便学生日常生活。

# 技术介绍

- 语言：Java
- 使用框架：Spring、Spring MVC、MyBatis、微信小程序
- 前端技术：JS、Vue、CSS3、Uniapp
- 开发工具：IDEA/Eclipse，Uniapp
- 数据库：MySQL 5.7/8.0
- 数据库管理工具：phpstudy/Navicat
- JDK版本：jdk1.8
- Maven：apache-maven 3.8.1-bin
- 前端环境：Node.js 12\14\16

# 核心代码

以下是项目中的一段核心代码，展示了如何通过Spring Boot与MyBatis实现宿舍信息的查询：

```java
// 宿舍管理Controller层
@RestController
@RequestMapping("/dormitory")
public class DormitoryController {

    @Autowired
    private DormitoryService dormitoryService;

    // 查询宿舍信息
    @GetMapping("/list")
    public ResponseEntity<List<Dormitory>> list() {
        List<Dormitory> dormitoryList = dormitoryService.list();
        return ResponseEntity.ok(dormitoryList);
    }
}

// 宿舍管理Service层
@Service
public class DormitoryServiceImpl implements DormitoryService {

    @Autowired
    private DormitoryMapper dormitoryMapper;

    @Override
    public List<Dormitory> list() {
        return dormitoryMapper.list();
    }
}

// 宿舍管理Mapper层
public interface DormitoryMapper {

    @Select("SELECT * FROM dormitory")
    List<Dormitory> list();
}
```

# 免费源码获取

```
5000套系统成品在线演示视频，复制到流浪器： 
```
```
https://www.yuque.com/yuqueyonghux32e1j/kxdc9g/ad8oz3bamkxmay0e#Cxun
```
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

# 项目截图
