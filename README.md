# Introduction_to_ai
introduction to artificial intelligence
#### 1. Windows 上安装 TensorFlow 流程
对于有英文基础的朋友，建议直接阅读官网[安装教程](https://www.tensorflow.org/install/pip?lang=python3)。本答案翻译自 TensorFlow 官网。
系统环境要求：
 - Windows 7（64位) 以上版本
 - Python 3.4, 3.5 或 3.6
Windows 上安装 TensorFlow 步骤：
1. 安装 Python 开发环境
检查系统是否已安装 Python 开发环境。如果已安装，则跳过该步骤。
```shell
python3 --version
pip3 --version
virtualenv --version
```
> 1) 独立安装 Microsoft Visual C   2015 Redistributable Update 3 或安装完整的 Visual Studio 2015：
> - 进入 Visual Studio [下载页](https://visualstudio.microsoft.com/vs/older-downloads/)
> - 选择 **Redistributables and Build Tools**
> - 下载和安装 Microsoft Visual C   2015 Redistributable Update 3
> 2) 安装 Windows 上 [64位的 Python 3 发布版](https://www.python.org/downloads/windows/)
>  3) 安装 **pip** 和 **virtualenv**
>  ```shell
>  pip3 install -U pip virtualenv
>  ```
2. 创建 Python 虚拟环境
```shell
virtualenv --system-site-packages -p python3 ./venv
.\venv\Scripts\activate
pip install --upgrade pip
pip list  # 展示 venv 中已安装的软件包
deactivate  # 使用完 TensorFlow 后，方可推出 venv 虚拟环境
```
3. 安装 TensorFlow pip 包
```shell
pip install --upgrade tensorflow
python -c "import tensorflow as tf; tf.enable_eager_execution(); print(tf.reduce_sum(tf.random_normal([1000, 1000])))"
```
