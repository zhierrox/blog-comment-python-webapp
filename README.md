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

查看python安装的包：：pip list

.gitignore：：新建一个.gitignore文件，env/表示忽略整个文件夹，包括env, 通过git status可以检验