# jfinal_demo

## 项目启动步骤
```ruby
1： 使用 blog.sql 中的 sql 语句创建数据库与数据库表

2: 修改 res/a_little_config.txt 文件，填入正确的数据库连接用户名、密码

3: 将项目导入 eclipse。推荐使用 Eclipse IDE for Java EE Developers

4: 打开 com.demo.common包下的 DemoConfig 文件，右键单击该文件并选择 Debug As ---> Java Application。
        其它启动项目的方式见 《JFinal手册》。除此之外，项目还可以与其它普通java web 项目一样使用 tomcat
   jetty 等 web server 来启动，启动方式与非jfinal项目完全一样。

5: 打开浏览器输入  localhost：83 即可查看运行效果

注意： 请确保您安装了 JavaSE 1.6 或更高版本，tomcat下运行项目需要先删除 jetty-server-xxx.jar，否则会有冲突
```

## 在mysql中创建数据库与数据库表
```ruby
CREATE DATABASE jfinal_demo;

USE jfinal_demo;

CREATE TABLE `blog` (
  `id` int(11) NOT NULL auto_increment,
  `title` varchar(200) NOT NULL,
  `content` mediumtext NOT NULL,
  PRIMARY KEY  (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;


INSERT INTO `blog` VALUES ('1', 'JFinal Demo Title here', 'JFinal Demo Content here');
INSERT INTO `blog` VALUES ('2', 'test 1', 'test 1');
INSERT INTO `blog` VALUES ('3', 'test 2', 'test 2');
INSERT INTO `blog` VALUES ('4', 'test 3', 'test 3');
INSERT INTO `blog` VALUES ('5', 'test 4', 'test 4');
```
## 运行后的结果展示

### 点击JFinal web framework会跳转到[JFinal官网首页](http://www.jfinal.com/)
![](https://github.com/wang911205/jfinal_demo/blob/master/1.png)

### 点击上图中Blog管理或者点击此处会进入下图页面：
![](https://github.com/wang911205/jfinal_demo/blob/master/2.png)

### 点击上图的修改会进入下图页面：
![](https://github.com/wang911205/jfinal_demo/blob/master/3.png)
