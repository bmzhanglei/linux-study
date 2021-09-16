# linux-study
linux和dock的学习

### Linux 常用命令
pwd 
ctrl+l / (clear)   清屏
history 查看命令历史
!22 调用历史中编号为22的命令
!h 调用历史中最后一次以h开头的命令

ls --help //获取帮助

### Linux 创建用户修改密码
   1.添加用户
		useradd zhangsan

	2.设置密码
		passwd zhangsan

	3.删除用户
		
		userdel -rf zhangsan

		-r：递归的删除目录下面文件以及子目录下文件。

批量创建文件
      touch file{1..10}
		rm -rf file{1..10}

查看文件前3行
    cat file1 | head -3
查看文件后3行  
   cat file1 | tail -3

查找文件 
    find / -name  httpd.conf

   updatedb   查找速度快
			1、建立一个小型数据库   updatedb
			2、再数据库里面搜索   locate httpd.conf

查找文件里面内容   找到httpd.conf 里面有listen				
	cat httpd.conf | grep listen
	cat httpd.conf | grep -ignore listen   /  cat httpd.conf | grep -i listen  忽略大小写

查找文件里面内容  vi搜索 
		vi  httpd.conf
		输入 /Listen    搜索Listen     N下一个

### Linux 目录管理
mkdir dir1 dir2 dir3
rm -rf dir1 dir2
rm -rf  dir*      以dir开头的所有文件删除

递归查看目录
mkdir -p a/b/c/d/e/f/g

递归查看目录
	tree a

复制目录
cp  -rf  wwwroot/ mywwwroot/	

tree命令不存在的话需要安装			
	yum install tree -y