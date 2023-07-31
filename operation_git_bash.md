生成个人token的操作：
进入GitHub
点击头像，进入setting，进入developer setting，进入personal access tokens，进入tokens，点击 generate new token 

第一步：
    初始化：
        方法一：
            使用git bash：git init(假如是第一次需要输入用户名和用户邮箱 命令分别是 git config --user.name "MOS" git config --user.email"2661558082@qq.com")
            使用TortoiseGit：  直接在文件夹创建新的版本仓库
        方法二：
            先在github上建立一个新的仓库在直接克隆到本地 
            git bash: git clone https... 
            TortoiseGit：直接点clone 然后粘贴远端链接
            

第二步：
与远端仓库关联
    git bash: 用git remote add <name> <url>来添加远端仓库,添加完毕后再push当前本地仓库内容

第三步：
将远程仓库的内容更新到本地仓库  
    git bash: git fetch 将远程仓库的内容拉到本地版本库，本地文件暂时不会发生变化
              git diff <远程仓库名/分支名> 可以对比本地版本库与当前工作区的区别
              git pull 将远程仓库完全整合到本地工作区
              git log  查看版本历史
    git bash完整工作流 先用 git fetch将远程仓库内容同步到本地版本库，再用git diff查看本地版本库与工作区的区别，最终确认无误后用git pull将远端仓库同步到本地
    一个小问题：注意到，git pull后似乎并不会把所有文件都覆盖 --这是自动合并 auto merge



vscode中使用git
点击文件的<+>即为git bash中的 git add 
在输入框输入提交信息后提交 对应 git commit
同步更改即为git pull

忽略文件 .gitignore
.<文件夹名称> 直接忽略整个文件夹
/.<文件类型>  递归忽略.gitignore所在目录以下的该类型文件
.<文件类型>   忽略.gitignore所在目录的该类型文件  

推荐建立本地仓库的方式是先在GitHub上建立仓库，再从远端仓库clone过来后，再进行修改再进行提交

将文件提交到缓存区 git add <文件名.后缀>   将文件提交到本地仓库git commit -m"提交文件的备忘录"

注意：进入vim编辑器后用 <:wq>退出 

git冲突与自动合并
当前远程仓库代码版本为A 有两个工作人员协助开发该仓库代码，当工作人员甲对代码修改完毕，他的本地仓库为B，推送到远程仓库，此时远程仓库版本更新为B
当工作人员乙想要提交他修改完成的本地仓库C时，git将不允许工作人员乙直接将C推送到远程仓库（B）。
工作人员乙必须将远端仓库（B）重新pull过来，在此基础上修改才能push到远程仓库
在工作人员乙将远端仓库(B)pull过来的时候，如果B和C没有冲突，git会自动将他们没有冲突的部分进行修改，并保留C进行的修改
如果发生冲突git将会报错，并提示需要手动解决冲突


git的分支：

