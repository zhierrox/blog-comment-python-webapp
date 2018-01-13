# blog-comment-python-webapp

删除文件夹：：rm -rf env

安装virtualenv：：
		To install virtualenv via pip run:
			$ pip3 install virtualenv
		
		Creation of virtualenv:
			$ virtualenv -p python3 <desired-path>
		
		Activate the virtualenv:
			$ source <desired-path>/bin/activate
		
		Deactivate the virtualenv:
			$ deactivate

进入python env也是直接用pip install：：(env) Mac:awesome-python3-webapp xun$

生成类似于package.json的版本信息文件：：只保存当前的package，不会自动更新
		$pip freeze > requirements.txt
之后直接使用：：
		$pip install -r requirements.txt

查看python安装的包：：pip list

.gitignore：：新建一个.gitignore文件，env/表示忽略整个文件夹，包括env, 通过git status可以检验

MySQL 密码：：
2018-01-13T03:43:24.595877Z 1 [Note] A temporary password is 
generated for root@localhost: &jA9rd=S=Z(h

If you lose this password, please consult the section How to Reset the Root Password in the MySQL reference manual.

mac 添加系统路径：：
	mac本地安装的文件在：：/usr/local/目录下
	echo 'export PATH="/usr/local/mysql/bin:$PATH"' >> ~/.bash_profile
	source ~/.bash_profile

修改文件读写权限问题：：E212: Can't open file for writing
	1， 用sudo：：
		sudo vi my.cnf

	2， :w !sudo tee % > /dev/null

mac下查找文件：：
	sudo find /usr/local -name mysql.sock
	
mysql.server star

