配置新网站
========

## 需要安装的包:

* nginx
* Python 3
* Git
* pip
* virtualenv

以Ubuntu16.04为例, 可以执行下面的安装:
```shell
sudo apt-get install nginx git python3 python3-pip
sudo pip3 install virtualenv
```

## 配置Nginx

* 参考nginx.template.conf
* 把SITENAME替换成所需的域名, 例如staging.my-domain.com

## Systemd任务

* 参考gunicorn-systemd.template.service
* 把SITENAME替换成所需的域名, 例如staging.my-domain.com

## 文件结构

假设有用户账户, HOME目录为`/home/username`

- /home/username
  - sites
    - SITENAME
        - database
        - source
        - static
        - virtualenv
