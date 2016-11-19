# qiuzhengneng.com

### Amazon AWS EC2 (Linux)
* Get public IP address


### Appache Setup in Linux
http://www.cnblogs.com/fengzheng/p/3619406.html

  * sudo apt-get build-dep xserver-xorg-video-intel (http://askubuntu.com/questions/103348/error-when-installing-makefile-make-no-targets-specified-and-no-makefile)

  * Install arp
  
  tar -zxf apr-1.5.0.tar.gz #解压压缩包 压缩包名称根据版本号决定  
  cd apr-1.5.0 #进入解压目录  
  ./configure --prefix=/usr/local/apr #进行安装配置 设置安装位置  
  make #编译  
  sudo make install #安装  
  
  *Install apr-util
  
  tar –zxvf apr-util-1.5.3.tar.gz #解压 压缩包名称根据版本号决定  
  cd apr-util-1.5.3 #进入解压目录  
  ./configure --prefix=/usr/local/apr-util --with-apr=/usr/local/apr/bin/apr-1-config  
  make   
  sudo make install  
  
  * Install pcre
  
  unzip –o pcre-8.34.zip #解压 文件名依据版本号而定  
  cd pcre-8.34  
  ./configure --prefix=/usr/local/pcre  
  make  
  sudo make install  
  
  ** for pcre issue, this may help (http://unix.stackexchange.com/questions/66692/apache-installation-configuration-cant-find-pcre-pcre-config-for-libpcre-not)
  
  * Install Apache
  
  tar –zxvf httpd-2.4.7.tar.gz #解压 我安装的为2.4.7版本  
  cd httpd-2.4.7  
  ./configure --prefix=/usr/local/apache2 --with-apr=/usr/local/apr --with-apr-util=/usr/local/apr-util/  
  make  
  sudo make install  
  之后启动Apache，
  
  cd /usr/local/apache2/bin  
    
  sudo apachectl –k start  
  或者   
  sudo service apache2 start 


  * How to control Apache services
  
    * Start：
    sudo service apache2 start   
    Or 
    sudo apachectl start  
    
    * Stop：
    sudo service apache2 stop  
    Or  
    sudo apachectl stop  
  
    * Restart：
    sudo service apache2 restart   
    Or 
    sudo apachectl restart 
  
    * Reload：
    sudo service apache2 reload


### Google Domain
* Doamin Purchasing
* DNS Setup 
  * Custom resource records (Name ---- @)
  * Registered hosts (AWS IP address)


##It Works!!! [Welcome to qiuzhengneng.com](http://www.qiuzhengneng.com)

###To be Continued...
  
