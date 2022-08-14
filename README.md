# Write-Bug
README.md叙述了实习期间遇到的问题和解决方案
## 1. VScode powershell不允许运行脚本解决方案
以管理员打开身份打开powershell，执行`set-ExecutionPolicy RemoteSigned`命令，执行`get-ExecutionPolicy`查看修改结果  
或者  
更改VSCode终端为cmd(默认是powershell)  
![pic1](https://github.com/dafeiq9977/Write-Bug/tree/main/pic/pic1.jpg)
## 2. 开发环境常用命令
npm install <pkg name> --save   下载包，并保存到package.json中  
tsc --init  生成tsconfig.json文件  
## 3. milkdown  
1. 指定编辑器生成于哪个HTML节点下
2. 指定编辑器初始值为某个字符串  或  HTML某个节点的里的内容  
3. 添加监听器 编辑器内容改变时获取编辑器内的字符串内容  
4. 设置编辑器为只读  
5. 通过Editor类的action函数，获取编辑器的各种上下文，对编辑器进行操作（获取编辑器里的内容，插入新的文本）
