# Install Tensorflow 

## 1. Install  Tensflow for Win 10

### 1.1 Install Anaconda

使用Anaconda安装Python，参考链接：http://blog.csdn.net/tina_ttl/article/details/53769256。





### 1.2 Install Tensorflow


参考链接：http://blog.csdn.net/goodshot/article/details/61926805

系统：Win10 64位

Anaconda版本：Anaconda3-4.4.0

python版本：3.6

tensorflow版本：1.2.0

    anaconda search -t conda tensorflow
    anaconda show dhirschfeld/tensorflow
    conda install --channel https://conda.anaconda.org/dhirschfeld tensorflow
    conda list

### 1.3 在Win10下启动tensorboard

进入CMD输入：

    d:
    cd D:\Workspace\Tensorflow\mnist_with_summaries
    python full_code.py

执行完full_code.py之后，在当前目录下生成了logs文件夹。

进入CMD输入：

    d:
    cd D:\ProgramFiles\Anaconda3\Lib\site-packages\tensorflow\tensorboard
    python tensorboard.py --logdir=D:\Workspace\Tensorflow\mnist_with_summaries\logs

直接使用tensorboard --logdir=logs的时候在Mac下能够正常运行，但是在Win下则会报错：

    tensorboard Fatal error in launcher: Unable to create process using '"'

## 2 Install Tensorflow for Mac
Mac版本：10.11.6

python版本：Python 2.7.13

    conda create -n tensorflow python=2.7
    source activate tensorflow
    pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/mac/tensorflow-0.8.0rc0-py2-none-any.whl
    source deactivate

讲tensorflow升级到1.2.1

    conda create -n tensorflow python=2.7
    source activate tensorflow
    pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-1.2.1-py2-none-any.whl
    source deactivate


升级anaconda

    conda --v
    conda update conda
    conda update anaconda
    conda --v

查看pip的版本

    pip -V

查看tensorflow版本

    python
    import tensorflow as tf
    tf.__version__

