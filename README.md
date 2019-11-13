# SSM模板搭建

## 1）包结构

### 1.1）cn.bysjm

- 根据需要自行更改

```markdown
- 控制层：cn.bysjm.controller
- 业务层：cn.bysjm.service
- 数据层：cn.bysjm.dao
- 实体层：cn.bysjm.service
```

## 2）配置文件

### 2.1）applicationContext.xml

```markdown
- 已经配置的内容:
- 1.注解组件扫描
- 2.第三方配置文件：数据库的连接四项
- 3.druid连接池
- 4.spring创建SqlSessionFactory工厂给IOC容器
- 5.开启接口扫描，创建代理对象，交给IOC容器
- 6.事务管理器
- 7.事务注解支持
```

### 2.2）jdbc.properties

- 1.自行添加数据库名！！！

- 2.自行添加用户名！！！

- 3.自行添加密码！！！

```markdown
- 数据库四项
- 1.jdbc.driver=com.mysql.jdbc.Driver
- 2.jdbc.url=jdbc:mysql://localhost:3306/
- 3.jdbc.username=
- 4.jdbc.password=
```

### 2.3）spring-mvc.xml

- 根据需求自行设计

### 2.4）spring-mvc.xml

- 视图解析器的前缀、后缀自己配置！！！！

```markdown
- 已经配置的内容:
- 1.注解组件扫描
- 2.MVC注解增强
- 3.视图解析器
	前缀：==自己配置！！！==
	后缀：==自己配置！！！==
- 4.静态资源放行
```

### 2.5）web.xml

```markdown
- 已经配置的内容:
- 1.前端控制器DispatcherServlet
- 2.中文乱码的配置
- 3.spring集成web容器
```

### 2.6）xxxDao.xml

- 指定好了模板
  - 文件名，命名空间自行更改

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="">

</mapper>
```



## 3）pom文件

```markdown
- 已经添加的dependency
- 1.MySql驱动 版本:5.1.47
- 2.druid 版本:1.1.15
- 3.MyBatis 版本:3.5.1
- 4.junit 版本:4.12
- 5.lombok 版本:1.18.6
- 6.spring-context 版本:5.1.5.RELEASE
- 7.aspectjweaver 版本:1.8.13
- 8.spring-jdbc 版本:5.1.5.RELEASE
- 9.spring-tx 版本:5.1.5.RELEASE
- 10.spring-test 版本:5.1.5.RELEASE
- 11.mybatis-spring 版本:1.3.2
- 12.spring-webmvc 版本:5.1.5.RELEASE
- 13.servlet-api 版本:2.5
- 14.jsp-api 版本:2.2
- 15.jstl 版本:1.2
```

## 4）Test

- 测试模板：

```java
@RunWith(SpringJUnit4ClassRunner.class)
@ContextConfiguration("classpath:applicationContext.xml")
public class SpringTest {

    @Test
    public void test01() throws Exception {

    }

}
```

