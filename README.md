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

## 情景模拟 1
1. 主工程 master 分支，初始化 submodule 提交
` 2309e9f5185321c828fa52268d347cd66dd40801 Submodule1 (heads/main)
  5c5fd09ff36cff1c552e043c56fc78ac82c9eabb Submodule2 (heads/main)
`
2. 主工程新建 dev 分支，submodule 新建 dev 分支
   > 此时 submodule 的节点会指向 heads/dev, 但是 commit 号是不变的。
` 2309e9f5185321c828fa52268d347cd66dd40801 Submodule1 (heads/dev)
  5c5fd09ff36cff1c552e043c56fc78ac82c9eabb Submodule2 (heads/dev)
 `
3.  submodule1 在 dev 分支修改代码,  并提交。
- 主工程会出现新的改动提示： modified:   Submodule1 (new commits)
- 主工程 git submodule 也显示有新的节点。前面显示 +
`+86369512c8ffee91af67e5b8121e5bd085b9bb46 Submodule1 (heads/dev)
  5c5fd09ff36cff1c552e043c56fc78ac82c9eabb Submodule2 (heads/dev)
`
4. 主工程在 dev 分支更新节点: 提交修改的文件（节点）
` 86369512c8ffee91af67e5b8121e5bd085b9bb46 Submodule1 (heads/dev)
  5c5fd09ff36cff1c552e043c56fc78ac82c9eabb Submodule2 (heads/dev)
`
