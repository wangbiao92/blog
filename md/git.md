git的使用 
====================

- 新建一个仓库，或者下载一个
      
      # 初始化仓库
      git init
      # clone仓库
      git clone xxx.com

- 跟踪文件tracked，并提交到暂存区
      
      # 指定文件
      git add filename
      # 本地文件覆盖到服务器（包括文件的删除，新建,修改）
      git add -A
      # 只有文件的修改以及新建
      git add .
      
- 代码提交(未同步到服务器)

      # 提交暂存区的文件
      git commit -m "message"
      # 提交指定文件
      git commit filename -m "message"
      # 提交已跟踪未暂存的文件
      # git commit -am "message"

- 代码同步
      # git push
      
      
