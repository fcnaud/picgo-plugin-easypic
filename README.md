# picgo-plugin-easypic

## ！！！重要
本项目为修改版，图床程序也请使用修改版。https://github.com/fcnaud/My-Easy-Pic-Bed

## 简介

[My-Easy-Pic-Bed](https://github.com/fslongjin/My-Easy-Pic-Bed) 为国内开发者 [fslongjin](https://github.com/fslongjin) 创建的开源、便捷、高效的图床服务，您可以将该服务部署在 `云服务器`、`个人主机`、`NAS` 等设备上，之后您便可以将图片上传至相应的服务器并获取图片链接。

## 环境搭建

下面我将演示如何在 `本地主机` 上搭建环境，若您要在 `云服务器` 和 `其它环境` 上搭建，这些操作也同样适用。

1. 前往 [My-Easy-Pic-Bed](https://github.com/fcnaud/My-Easy-Pic-Bed) 下载图床服务

   ![image-20220210201146087](https://i.postimg.cc/mDGVmb1x/202202102011195.png)

2. 将压缩包解压后放在你的服务器中，解压后文件如图

   ![image-20220210201042704](https://i.postimg.cc/Z54bz3k0/202202102010782.png)

3. 可在`config.ini`中设置端口号和图片最大尺寸限制

   ```ini
   [strings]
   running_domain = 0.0.0.0	
   
   
   [ints]
   max_length = 10		// 最大尺寸为10M
   port = 9999			// 端口号为9999
   ```

4. 双击 `startProgram.exe` 启动图床服务

   ![image-20220210182759058](https://gitee.com/msylj/images/raw/master/202202101827212.png)

   ![image-20220210194816559](https://i.postimg.cc/Z5zph9RQ/202202101948652.png)

5. 下载安装 `easypic`
    
    a. 下载插件 `git clone https://github.com/fcnaud/picgo-plugin-easypic`

    b. 插件设置->导入本地插件，选择插件目录
        ![](./Snipaste_2023-06-11_18-29-57-1.png)

6. 根据实际修改相关设置

   ![image-20220210195011555](https://i.postimg.cc/T3QVqddH/202202101950610.png)

   - `服务器IP`：部署图床服务的服务器IP，若部署在本机则为127.0.0.1
   - `端口号`：config.ini中设置的端口号，默认80

7. 点击确定，设置完成！

## Q & A

### 1.如何查看本机IP？

1. 键盘按下`win + r`，输入`cmd`

   ![image-20220210195431387](https://i.postimg.cc/6Q5DYpd7/202202101954425.png)

2. 输入`ipconfig`，回车

   ![image-20220210195552474](https://i.postimg.cc/mg0HSPxj/202202101955551.png)

3. 该`Ipv4地址`即为服务器IP地址

### 2.图片的具体存储位置？

所有图片均存储于 `解压根目录/pics`

### 3.如何在运行图床服务时不显示终端？

在压缩包根目录下有两个批处理命令 `start.bat` 和 `stop.bat`，双击 `start.bat` 即可运行图床服务而不弹出终端，双击 `stop.bat` 即可关闭图床服务。

