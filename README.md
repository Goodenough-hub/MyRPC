# MyRPC

## 环境配置
- linux系统
- 安装boost库 [参考链接](https://blog.csdn.net/qq_41854911/article/details/119454212)
  - 验证boost是否安装成功[链接](https://blog.csdn.net/weixin_43910370/article/details/121371181)
- 安装muduo网络库
- 安装cmake环境`apt-get install cmake`
- 安装Protobuf
  1. 解压`protobuf-master.zip`
  2. `cd protobuf-master`
  3. `sudo apt-get install autoconf automake libtool curl make g++ unzip`
  4. `./autogen.sh`
  5. `./configure`
  6. `make`
  7. `sudo make install`
  8. 刷新动态库`sudo ldconfig`
- 安装`zookeeper`
  1. `cd conf`
  2. `vim zoo.cfg`
  3. 修改znode节点存放的路径，`dataDir=/yourpath/`
  4. `cd bin`
  5. `./zkServer.sh start`
  6. `ps -ef | grep zookeeper`
   > zookeeper是java开发的，需要有java的环境：`sudo apt update`、`sudo apt install openjdk-11-jdk`
   > Linux: `sudo apt-get install libzookeeper-mt-dev`