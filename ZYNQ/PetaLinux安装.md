## 选择版本
PetaLinux版本与Vivado、Vitis版本一致

## 安装依赖库

1. 正常安装
    ```
    sudo apt install xterm autoconf libtool texinfo zlib1g-dev gcc-multilib build-essential
    ```

2. 替换
    在ubuntun系统（目前使用Ubuntu 18.04）
    - zlib无法安装，使用zlib1g代替：` sudo apt install zlib1g `
    - ncurses无法安装，使用libncurses5-dev代替：`sudo apt install libncurses5-dev`
    - zlib1g:i386无法直接安装
    ```
    sudo dpkg --add-architecture i386
    sudo apt-get update
    sudo apt install zlib1g:i386
    ```
## 安装
安装PetaLinux: `./petalinux-v2022.1-04191534-installer.run -d <PetaLinux安装路径>`

- 注意不能使用管理员安装（不能使用sudo）

## 激活环境变量

```
source <PetaLinux安装路径>/settings.sh
```

# 安装完成

