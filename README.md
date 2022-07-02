# project describtion
 This project is use to make qt5 to embedded platftom(ssd202) and fix some qt question

## catalog
 Qt source and Lisence
 How to build

## Qt source and Lisence
 Download qt src code from : http://download.qt.io/
 Lisence: LGPL_v3　and other licenses that Qt need to comply with
 reference: https://github.com/aaron201912/Qt5.15_example/blob/master/README.md
## How to buile
- Qt 5交叉编译
  - 设置环境变量
    - vim /etc/profile 添加toolchain路径：
    - export PATH=your_toolchain_path:$PATH
    　
- 安装perl，python：
  - sudo apt-get install perl Python2.7


- 安装git工具：
  - sudo apt-get install git

- 下载tslib：
  - *git clone https://github.com/libts/tslib.git

- 编译tslib：
  - sudo apt-get install automake
  - sudo apt-get install autogen  
  - sudo apt-get install libtool
  - ./autogen.sh 
  - ./configure --prefix=/home/..../arm_tslib --host=arm-linux ac_cv_func_malloc_0_nonnull=yes CC=arm-linux-gnueabihf-gcc  
    - prefix为tslib导出的头文件和lib存放路径。
  - make –j4  
  - make install  

- 编译qt5
  - make –j4
  - make install

