# git submodule learn

## 项目地址
- 本项目 git@github.com:HeCaser/SubmoduleLearn.git
- sm1 git@github.com:HeCaser/Submodule1.git
- sm2 git@github.com:HeCaser/Submodule2.git

## 添加 submodule
 - 进入要放置 sm 的目录
 - 添加已有项目： submodule add git@github.com:HeCaser/Submodule2.git
 
## 当我们修改了 submodule
- 首先需要对 submodule 进行 commit 操作
- commit 完成之后，相当于主工程对应的提交节点有改动，主工程需要更新节点。
- 建议使用 SourceTree， 对 submodule 支持更全面
