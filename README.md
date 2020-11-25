## Kata介绍

1. 通过文本文件向应用程序提供输入数据 testData.txt (`resource/testData.txt`)。
2. 在 `main.py` 中**集成**你自己所写的代码，并将结果赋值给 `receipt` 变量。
    * `testDataFile` 为 `/resource` 文件夹下的测试数据文件名，例如传入的值为 "testData.txt"。
    * 你写的程序将把 `testDataFile` 作为参数加载此文件并读取文件内的测试数据，并对每条测试数据计算结果。
    * 将所有计费结果拼接并使用 `\n` 分割，然后保存到 receipt 变量中。
3. 请按照提示把你的的代码逻辑写在 `fizzbuzz` 模块之中，测试代码写在 `tests` 目录下，充分做好单元测试。
4. 不得修改 `requirements.json` 文件和 `.pylintrc` 等配置文件。
5. 考试环境使用 Python 3.x 版本。

### 详细描述：
#### FizzBuzz需求

这是一个简单的猜数字游戏。

想象你是个小学5年级的学生，现在还有5分钟就要下课，数学老师带全班同学玩一个小游戏。他会用手指挨个指向每个学生，被指着的学生就要依次报数:第一个被指着的学生说“1”，第二个被指着的学生说“2”，以此类推。

呃......并不完全“以此类推”......如果一个学生被指着的时候，应该报的数是3的倍数，那么他就不能说这个数，而是要说“Fizz”。同样的道理，5的倍数也不能被说出来，而是要说“Buzz”。

于是游戏开始了，老师的手指向一个同学，他们开心地喊 着:“1!”，“2!”，“Fizz!”，“4!”，“Buzz!”......终于，老师指向了你，时间仿佛静止，你的嘴发干，你的掌心在出汗，你仔细计算，然后终于喊出“Fizz!”。运气不错，你躲过了一劫，游戏继续进行。

为了避免在自己这儿失败，我们想了一个作弊的法子: 最好能提前把整个列表打印出来，这样就知道到我这儿的时候该说什么了。全班有33个同学，游戏可能会玩2到3轮。现在，赶紧去写代码吧!

任务: 写一个程序，打印出从1到100的数字，将其中3的倍数替换成“Fizz”，5的倍数替换成“Buzz”。既能被3整除、又能被5整除的数则替换成“FizzBuzz”。

#### 测试数据

\n为文件中的不可见的换行字符

```
1\n
2\n
3\n
4\n
5\n
6\n
7\n
8\n
9\n
10\n
11\n
12\n
13\n
14\n
15\n
16
```

#### 期望输出

\n为console输出中的不可见的换行字符

```
1\n
2\n
Fizz\n
4\n
Buzz\n
Fizz\n
7\n
8\n
Fizz\n
Buzz\n
11\n
Fizz\n
13\n
14\n
FizzBuzz\n
16\n
```

### 开始考试

1. 点击`开始考试`。
2. 下载考题模板并解压，重命名为`tdd-fizzbuzz-py`。
3. `cd tdd-fizzbuzz-py`。
4. `git init`。
5. `git remote add origin <github自有仓库>`。
6. `git add .`。
7. `git commit -m "Initial commit"`。
8. `git push -u origin master`。
9. 接着答题，使用 `python -m pytest --cov=fizzbuzz tests --cov-branch --cov-fail-under=100` 和 `python -m pylint fizzbuzz`验证本地结果。
    * `pylint` 与 `pytest` 工具需要安装第三方依赖，使用命令 `pip install -r requirements.txt` 进行安装
    * 考试题目基于 python3，请根据自己环境更改上述所有 python 实际命令
10. 本地验证无误后，push到远程仓库，并将git地址提交到科举。
11. 提交之后等待科举出考试结果。

### 考试通过的标准

1. 通过 checkstyle 规则(配置文件见 `.pylintrc` )：
    * 单个 Python 文件不得超过50行。
    * 单行代码长度不得超过80个字符。
    * 单个方法长度不得超过10行。
    * 单个方法的圈复杂度不得超过4。
    * 单个方法参数个数不得超过3。
    * 友好的方法命名。
2. 在规定考试时间内完成答题，并完成所有需求。
3. 测试覆盖率100%，没有严重的Sonar问题。
4. 采用TDD开发模式。
