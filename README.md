# practise

## git reset

```bash
$ git reset [--soft | --mixed | --hard] [HEAD]
# --mixed 为默认，可以不用带该参数，用于重置暂存区的文件与上一次的提交(commit)保持一致，工作区文件内容保持不变。

$ git reset HEAD^
# 回退到上一个版本

$ git reset 052e
# 回退到指定版本、工作区还有上次的修改内容

# --hard 参数撤销工作区中所有未提交的修改内容，将暂存区与工作区都回到上一次版本，并删除之前的所有信息提交：
$ git reset –hard bae128
# 回退到某个版本回退点之前的所有信息。 
```