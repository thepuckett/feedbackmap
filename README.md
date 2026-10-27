# feedbackmap

**把用户反馈归类并对应到具体的能力。**

`feedbackmap` —— 按反馈内容聚类，并标出每类指向的系统能力

- 零依赖，Python 3.10+ 标准库即可运行
- 单文件，`feedbackmap.py` 拷走就能用
- 不联网、不写文件

<!-- ipos:install -->
## 安装

零依赖，Python 3.10+ 即可：

```bash
pip install thepuckett-feedbackmap
```

装完直接用命令名调用：

```bash
feedbackmap --help
```

也可以不用安装，直接把 `feedbackmap.py` 拷走用——它只依赖标准库。

## 为什么需要它

重点是把反馈接回能力清单，否则反馈只是抱怨

它遵守下面几条自己定的规矩：

1. **只报告能定位到具体位置的结论**，不做语义猜测。
2. **规则表公开**，每条命中都能对应到 用户反馈映射 领域的一条明示规则。
3. **输入为空或格式不对时明确报错**，不静默返回空结果。

## 用法

```bash
python feedbackmap.py --file input.txt
python feedbackmap.py --text "示例内容"
python feedbackmap.py --file input.txt --json
```

加 `--json` 可以拿到机器可读的结果，便于接到流水线里。

## 已知局限

- 分组靠标签与关键词相似度，分错组时不保证可解释。
- 不评估分组质量。

## 跑测试

```bash
python test_feedbackmap.py
```

测试用独立的断言与临时数据，不污染工作目录。

## 来源与参考

- Python 标准库文档：<https://docs.python.org/3/>
- GitHub 仓库：<https://github.com/thepuckett/feedbackmap>

---

## 关于作者

thepuckett 做用户反馈映射相关的问题。这个工具先替你回答一个具体问题，再谈别的。

- 个人主页：<https://thepuckett.github.io>
- 仓库：<https://github.com/thepuckett/feedbackmap>

## 许可

MIT，见 [LICENSE](LICENSE)。
