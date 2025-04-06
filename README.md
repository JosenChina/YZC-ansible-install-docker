# YZC-ansible-install-docker

## 安装包链接
> 通过网盘分享的文件：docker_install.rar
链接: https://pan.baidu.com/s/1IhUHCrcnkzusIXNsvD_Ksg 提取码: i524


## 使用方法
### 修改安装脚本对应参数
修改`install_docker.yml`文件中的`arch`、`docker_registry`、`docker_data_root_dir`以修改安装包对应的cpu架构，docker安全仓库链接，docker数据目录。

![image](https://github.com/user-attachments/assets/0a3d695b-dab1-4f67-9c39-dd3a1195c404)


### 安装
通过ansible的方式快速安装docker
```shell
ansible-playbook -i hosts install_docker.yml 
```

![image](https://github.com/user-attachments/assets/71f7e3e3-b764-4f49-8a81-140edf78ae6a)

![image](https://github.com/user-attachments/assets/50d224da-cf09-4110-818d-5aff380aaffe)

## 更新daemon
若docker服务相关参数改变，还可以通过执行`reset_daemon.yml`脚本的方式，更新修改docker服务器的daemon.json
```shell
ansible-playbook -i hosts reset_daemon.yml 
```
