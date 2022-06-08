| 第二届计图热身赛

# Jittor 计图挑战热身赛
| 计图挑战热身赛要求:

本赛题将会提供数字图片数据集 MNIST，参赛选手需要训练一个将随机噪声和类别标签映射为数字图片的Conditional GAN模型，并生成注册时绑定的手机号。



｜最终结果（马赛克处理后）

![生成结果](https://images.cnblogs.com/cnblogs_com/illlioo/2172366/o_220608025727_result.png)

## 安装 
| 基本的硬件需求、运行环境、依赖安装方法

本项目在个人笔记本电脑（GPU:NVIDIA 960M）上完成，训练时间约为 0.5 小时。

#### 运行环境
- Win 10
- python >= 3.8
- jittor

#### 安装依赖
执行以下命令安装 python 依赖
```
conda create -n xxx(your env name) python=3.8
conda activate xxx
conda install pywin32
python -m pip install jittor
pip install -r requirements.txt
```

## 训练
｜ 介绍模型训练的方法

缺失代码添加：

```
# TODO: 添加最后一个线性层，最终输出为一个实数
nn.Linear(512,opt.n_classes)
# TODO: 将d_in输入到模型中并返回计算结果
output = self.model(d_in)
# TODO: 计算真实类别的损失函数
d_real_loss = adversarial_loss(validity_real,valid)
# TODO: 计算虚假类别的损失函数
d_fake_loss = adversarial_loss(validity_fake,fake)
# 生成你的手机号
number = '17xxxxxxxxx'
```

训练可运行以下命令：
```
python CGAN.py
```

## 致谢
感谢Jittor

