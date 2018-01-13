# blog-comment-python-webapp

python 2, 3 默认为3：：
echo "alias python='python3'" >> ~/.bash_profile

echo "alias pip='pip3'" >> ~/.bash_profile
source ~/.bash_profile



删除文件夹：：rm -rf env

安装virtualenv：：
		To install virtualenv via pip run:
			$ pip3 install virtualenv
		
		Creation of virtualenv:
			$ virtualenv -p python3 <desired-path>
		
		Activate the virtualenv: 重新进入时，也是执行这个命令
			$ source <desired-path>/bin/activate
		
		Deactivate the virtualenv:
			$ deactivate

进入python env也是直接用pip install：：(env) Mac:awesome-python3-webapp xun$

生成类似于package.json的版本信息文件：：只保存当前的package，不会自动更新
		$pip freeze > requirements.txt
之后直接使用：：
		$pip install -r requirements.txt
		安装的地方就没有virtualenv了
		pip3和python3

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

	3， ~/.bash_profile

mac下查找文件：：
	sudo find /usr/local -name mysql.sock

mac安装mysql，不要直接安装，用brew install：：否则会找不到sock文件：：
	－－Remove MySQL completely
		ps -ax | grep mysql stop and kill any MySQL processes
		brew remove mysql
		brew cleanup
		sudo rm /usr/local/mysql
		sudo rm -rf /usr/local/var/mysql
		sudo rm -rf /usr/local/mysql*
		sudo rm ~/Library/LaunchAgents/homebrew.mxcl.mysql.plist
		sudo rm -rf /Library/StartupItems/MySQLCOM
		sudo rm -rf /Library/PreferencePanes/My*
		launchctl unload -w ~/Library/LaunchAgents/homebrew.mxcl.mysql.plist
		edit /etc/hostconfig and remove the line MYSQLCOM=-YES-
		rm -rf ~/Library/PreferencePanes/My*
		sudo rm -rf /Library/Receipts/mysql*
		sudo rm -rf /Library/Receipts/MySQL*
		sudo rm -rf /private/var/db/receipts/*mysql*
		edit ~/.bash_profile and remove any aliases for mysql or mysqlAdmin
		restart your computer just to ensure any MySQL processes are killed try to run mysql, it shouldn't work

	－－Reinstall MySQL with Homebrew
		brew doctor
		brew update
		brew install mysql
		unset TMPDIR
		mysqld -initialize --verbose --user=whoami --basedir="$(brew --prefix mysql)" --datadir=/usr/local/var/mysql --tmpdir=/tmp
		mysql.server start
		brew services start mysql

brew install的问题：：Homebrew must be run under Ruby 2.3
	run brew update before any brew install

mysql的基本命令操作：：
	1， 打开：：mysql -uroot -p
	2， 退出：：exit
	3， 显示数据了列表：：show databases; show tables

修改mysql密码：：
	$mysql -uroot -p
	$mysql> FLUSH PRIVILEGES;
	$ALTER USER 'root'@'localhost' IDENTIFIED BY 'password';












