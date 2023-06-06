# README

# DQN在2048游戏中的应用

本项目主要探讨了深度Q网络(DQN)在2048游戏中的应用。开发了一个基于DQN的代理(agent)，使其能自主玩2048游戏并优化策略。

## 安装

Python >=3.8

在运行本项目之前，需要安装一些必要的Python库。可以通过以下命令安装：

```
pip install -r requirements.txt
```

## 使用

本项目有两种使用方式，具体如下：

### 训练自己的模型

1. 首先运行以下命令启动Jupyter notebook：

    ```bash
    jupyter notebook main.ipynb
    ```

2. 在notebook中，按照顺序执行每个cell，其中包括配置环境、定义模型、训练模型、使用模型推理游戏等步骤。
3. 可以修改的部分包括但不限于：超参数部分、Net的结构、DQN类等。
4. 此外，还可以将“初始化环境部分”的如下代码

    ```python
    device = torch.device("cpu")
    ```

    改为

    ```python
    device = torch.device("cuda" if torch.cuda.is_available else "cpu")
    ```

    从而使用GPU来训练模型。

### 使用已经训练好的模型进行测验

1. 如果你不想自己训练模型，也可以直接使用已经训练好的模型进行测试。运行以下命令启动Jupyter notebook：
   
    ```bash
    jupyter notebook main.ipynb
    ```
    
2. 在`main.ipynb` notebook中，按顺序执行每个cell。但请注意，**跳过**名为“开始训练”的cell。这是因为我们已经提供了预训练好的模型文件`2048.pt`，你无需重新训练。

## References：

[1]Dedieu A, Amar J. Deep reinforcement learning for 2048[C]//Conference on Neural Information Processing Systems (NIPS), 31st, Long Beach, CA, USA. 2017.

[2]https://cs.uwaterloo.ca/~mli/zalevine-dqn-2048.pdf

[3]https://bbs.huaweicloud.com/blogs/383829

[4]https://blog.csdn.net/weixin_39891381/article/details/103253968?spm=1001.2014.3001.5506

[5]https://github.com/FelipeMarcelino/2048-Gym

[6]https://github.com/rgal/gym-2048
