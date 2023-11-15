# 开发手册

### 写在前面

        基于微信小程序与Django后端实现的“漆艺乡村”小程序应用开发，本文档将从0开始记录全部开发过程，包括项目的搭建以及部署上线。



## GitHub



## 前端



## 后端



### 技术栈

- Djnago、MySql
  
  

服务器

### Django



#### 项目搭建



##### 创建虚拟环境

###### **为什么要创建虚拟环境？**

1. 避免依赖冲突：每个项目可能需要不同的Python版本和库，如果不使用虚拟环境，可能会出现依赖冲突的问题，这可能导致项目无法正常运行。

2. 保持项目隔离：使用虚拟环境可以确保项目之间互不影响，即使在同一台服务器上也可以同时运行多个Django项目。

3. 方便共享和备份：使用虚拟环境可以方便地打包和共享项目以及备份整个项目所需的Python环境。

4. 更好的可重复性：使用虚拟环境可以确保项目在任何机器上都能够正常运行，因为每个机器上的环境都是相同的。
   
   

###### **流程**

```python
conda create -n 环境名称 python=版本
```

![0a32e980-b0e0-46c0-8f61-f2c873c83b17](file:///C:/Users/31926/Pictures/Typedown/0a32e980-b0e0-46c0-8f61-f2c873c83b17.png)

![d4c76915-fa75-41d8-aea8-e5f275613516](file:///C:/Users/31926/Pictures/Typedown/d4c76915-fa75-41d8-aea8-e5f275613516.png)

![9798465f-bbbc-4bd6-871e-29f2e4bc6a9e](file:///C:/Users/31926/Pictures/Typedown/9798465f-bbbc-4bd6-871e-29f2e4bc6a9e.png)

创建成功！

![aa109ae4-f40c-4359-863e-d2a4545ca063](file:///C:/Users/31926/Pictures/Typedown/aa109ae4-f40c-4359-863e-d2a4545ca063.png)

##### 创建DJANGO项目

下载django3.2.18

![d356931e-49d5-4eb9-affb-261d52ee751b](file:///C:/Users/31926/Pictures/Typedown/d356931e-49d5-4eb9-affb-261d52ee751b.png)

###### 创建django项目

django-admin startproject 项目名称

![64eaa0bc-af94-4f0e-80a5-62f2f84930a0](file:///C:/Users/31926/Pictures/Typedown/64eaa0bc-af94-4f0e-80a5-62f2f84930a0.png)

###### 启动django项目

进入tom文件夹后执行

python manage.py runserver

打开浏览器输入

http://127.0.0.1:8000/

![1fc82292-47c7-495d-928e-1ec4efb5b457](file:///C:/Users/31926/Pictures/Typedown/1fc82292-47c7-495d-928e-1ec4efb5b457.png)

##### 在pycharm中打开项目

###### 打开项目路径

![57baa2b0-81dc-4c8b-ad50-e7c93a62899a](file:///C:/Users/31926/Pictures/Typedown/57baa2b0-81dc-4c8b-ad50-e7c93a62899a.png)

###### 设置虚拟环境

file->settings->Project projectname->python InTerpreter

![555a4d9b-d870-4d52-bb74-193d478c76c1](file:///C:/Users/31926/Pictures/Typedown/555a4d9b-d870-4d52-bb74-193d478c76c1.png)



![a336a5ee-73b4-4a60-aad2-c2b8b11754b7](file:///C:/Users/31926/Pictures/Typedown/a336a5ee-73b4-4a60-aad2-c2b8b11754b7.png)

![8392b55e-f873-4950-8fe7-fa862e6a7dcb](file:///C:/Users/31926/Pictures/Typedown/8392b55e-f873-4950-8fe7-fa862e6a7dcb.png)

查看以下验证是否成功

![0e366c39-ee95-4d7a-8379-60591fbe9536](file:///C:/Users/31926/Pictures/Typedown/0e366c39-ee95-4d7a-8379-60591fbe9536.png)

![858c7c62-5c1e-4997-9e5a-e9b699af2f23](file:///C:/Users/31926/Pictures/Typedown/858c7c62-5c1e-4997-9e5a-e9b699af2f23.png)

![2de5a8f9-b005-41f4-a994-757f99128878](file:///C:/Users/31926/Pictures/Typedown/2de5a8f9-b005-41f4-a994-757f99128878.png)

![7b595747-6eb6-4376-82a4-dc3370cadccd](file:///C:/Users/31926/Pictures/Typedown/7b595747-6eb6-4376-82a4-dc3370cadccd.png)

##### MySql在Django中的配置





### 数据库

#### MySql在服务器上的配置

登录阿里云ecs并远程链接

![8367942a-6a1f-4bd0-a290-a16b20d8e367](file:///C:/Users/31926/Pictures/Typedown/8367942a-6a1f-4bd0-a290-a16b20d8e367.png)

下载linux版本的mysql

https://www.mysql.com/

![d0e003b3-6831-4927-b8f7-09a656bc3d5e](file:///C:/Users/31926/Pictures/Typedown/d0e003b3-6831-4927-b8f7-09a656bc3d5e.png)

![3ede6508-ad66-4a95-a398-2a8cd7507f1e](file:///C:/Users/31926/Pictures/Typedown/3ede6508-ad66-4a95-a398-2a8cd7507f1e.png)

![c6628dbe-3aee-46b1-8596-37c2b4c035b0](file:///C:/Users/31926/Pictures/Typedown/c6628dbe-3aee-46b1-8596-37c2b4c035b0.png)

![586fee8a-70ac-47b2-baf8-daffa1a7adc9](file:///C:/Users/31926/Pictures/Typedown/586fee8a-70ac-47b2-baf8-daffa1a7adc9.png)

![a0c19690-9c72-415a-8c15-7dbd40d13711](file:///C:/Users/31926/Pictures/Typedown/a0c19690-9c72-415a-8c15-7dbd40d13711.png)

准被上传压缩包

使用xhell远程链接后，查看是否安装了lrzsz

若没有则执行安装

```
yum -y install lrzsz
```

![9e51cb6c-e087-4153-b226-07d5a13d1660](file:///C:/Users/31926/Pictures/Typedown/9e51cb6c-e087-4153-b226-07d5a13d1660.png)

##### 安装mysql

```
yum install -y mysql-server
```

设置开机自启动

```
systemctl enable mysqld.service
```

检查开机自启动是否成功

```
systemctl list-unit-files | grep mysqld
```

设置开启服务

```
systemctl start mysqld.service
```

登录

```
##为空就不需要输入
mysql -uroot -p       //密码也就是第九步里面查看到的默认密码
```

修改密码

```
alter user 'root'@'localhost' identified by '123456'; 
```

进入mysql库，设置远程登录

```
#运行下面两句话之后就可以通过root账户远程登陆。
update user set host='%' where user='root';
#命令立即执行生效(千万不要忘记刷新！！！！！)
#这句表示从mysql数据库的grant表中重新加载权限数据
flush privileges;
```

![18f57d39-bccb-40a9-8364-40bd5c4b1956](file:///C:/Users/31926/Pictures/Typedown/18f57d39-bccb-40a9-8364-40bd5c4b1956.png)

开放对应安全组3306

![41ebc597-ce0e-44e0-ae29-373e26ee5696](file:///C:/Users/31926/Pictures/Typedown/41ebc597-ce0e-44e0-ae29-373e26ee5696.png)



#### MySql在Django项目中的配置


