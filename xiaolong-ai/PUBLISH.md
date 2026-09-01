# 发布到 GitHub 指引（小龙智脑 / XiaoLong Brain）

> 当前 WorkBuddy 的 GitHub 连接器处于断开状态，无推送凭证，因此由你本地执行以下命令即可完成发布。

## 方案 A：只发布「原创项目」（推荐）

`xiaolong-ai/` 目录是**完全原创、打「小龙」标、MIT 授权**的干净仓库，**本地已 `git init` 并完成首次提交（commit `09cd403`，纳入 41 个文件）**。你只需补上远程地址并推送：

```bash
cd xiaolong-ai
# 在 GitHub 新建空仓库后，把下面地址换成你的仓库 URL：
git remote add origin https://github.com/<你的用户名>/xiaolong-ai.git
git branch -M main
git push -u origin main
```

## 方案 B：连同源下载的参考项目一起发布

`doc/reference/transformers` 是从 GitHub 克隆的 **HuggingFace Transformers（第三方，版权归原作者，LICENSE 已保留）**，仅作本地学习参考。如需一并托管（镜像需遵守其 Apache-2.0 协议、保留版权声明）：

```bash
cd ../reference/transformers
git remote set-url origin https://github.com/<你的用户名>/transformers-mirror.git
git push -u origin main
```

## 重新生成全部源码

如需修改后重新生成所有文件：

```bash
python generate_project.py
```

## 说明

- 原创代码版权人：**小龙 (XiaoLong)**，License：MIT。
- 参考项目（Transformers）版权归 HuggingFace 及贡献者，保留其原始 LICENSE，请勿将作者信息替换为「小龙」。
