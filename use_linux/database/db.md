数据库使用：
http://blog.csdn.net/it_dream_er/article/details/52092262
goto setting.py
DATABASES = {  
1.    'default': {  
2.        'ENGINE': 'django.db.backends.mysql',  
3.        'NAME': 'mydatabase',  
4.        'USER': 'mydatabaseuser',  
5.        'PASSWORD': 'mypassword',  
6.        'HOST': '127.0.0.1',  
7.        'PORT': '3306',  
8.    }  
9.}  

http://blog.csdn.net/it_dream_er/article/details/52093362
数据库连接mysql配置文章
：
部署apache:
sudo apt-get install apache2


sudo apt-get install libapache2-mod-wsgi
