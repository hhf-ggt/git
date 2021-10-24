# practise

## git reset

```bash
$ git reset [--soft | --mixed | --hard] [HEAD]
# --mixed 为默认，可以不用带该参数，用于重置暂存区的文件与上一次的提交(commit)保持一致，工作区文件内容保持不变。

$ git reset HEAD^
# 回退到上一个版本

$ git reset 052e
# 回退到指定版本 、工作区还有修改的记录

# --hard 参数撤销工作区中所有未提交的修改内容，将暂存区与工作区都回到上一次版本，并删除之前的所有信息提交：
$ git reset –hard bae128
# 回退到某个版本回退点之前的所有信息、删除掉所有提交相关的信息、包括ommit记录
```

## git revert

```bash
# 也是版本回退
# 主要是和git reset 有一些区别
# git reset --hard xx 之后、xx版本之后的提交都会被删掉

# git revert 
# 比如我们有版本1、2、3 然后发现版本2又问题、我们需要回退到版本1、如果使用git reset 的话 版本2 和版本3的提交记录都没有了
# 但是如果使用 git revert 的话、他会重做 生成一个新的版本4、版本2的内容不存在、但是版本3的内容还是存在的
$ git revert -n xxxx
```

eg

```text
比如我三个版本分别提交1.txt 2.txt 3.txt
然后我发现2.txt有问题 不想要了
所以 git revert -n 2.txt的hash
但是重做之后需要重新 git add & git commit -m"" & git push
```