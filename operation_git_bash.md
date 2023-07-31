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
            

第二部：
与远端仓库关联
    git bash: 用git remote add <name> <url>来添加远端仓库,添加完毕后再push当前本地仓库内容


推荐建立本地仓库的方式是先在GitHub上建立仓库，再从远端仓库clone过来后，再进行修改再进行提交

将文件提交到缓存区 git add <文件名.后缀>   将文件提交到本地仓库git commit -m"提交文件的备忘录"
