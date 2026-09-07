# SE-2026
[课程网站](https://linliulab.github.io/SE-2026/)

本项目为清华大学2026年秋季学期《软件工程》课程网站，采用 `mkdocs` 编写

## 撰写

本站点内容使用 Markdown 进行编写。具体可查看 [mkdocs](https://www.mkdocs.org/) 和 [mkdocs-material](https://squidfunk.github.io/mkdocs-material/extensions/pymdown/) 文档。

如果创建了新页面，需要插入到 `mkdocs.yml` 的 `nav` 部分，否则将不会出现在编译结果中。

## 编译

首先安装依赖，而后编译即可：

```bash
python3 -m pip install --user -r requirements.txt # 安装 Python 依赖包
mkdocs serve # 直接在本地 serve，或者：
mkdocs build --clean # 生成于 site/ 文件夹中
```

## 发布

课程网站：https://linliulab.github.io/SE-2026/

沿用 MkDocs + GitHub Pages 的发布方式：源码保存在 `main` 分支，生成的网站发布到 `gh-pages` 分支。

在仓库根目录执行：

```bash
python -m mkdocs build --clean
python -m mkdocs gh-deploy --remote-name origin --remote-branch gh-pages
```

GitHub 仓库的 Settings → Pages 应选择 `Deploy from a branch`，分支为 `gh-pages`，目录为 `/(root)`。
