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
#### 自定义快捷键
  修改preset-gfm插件的gfm变量  
  修改方法：  
  ```
  import { 快捷键行为 } from '@milkdown/preset-gfm';
  gfm.configure(快捷键对应的行为, {  
        keymap: {  
            [SupportedKeys.Bold]: ['Mod-g', 'Mod-b'],  
        }  
      })  // 返回设置后的gfm，用这个返回值use
  ```
  快捷键行为有：  
  1. blockquote 块引用  
  2. bulletList 变成修饰符是·的列表  
  3. codeFence 代码块  
  4. codeInline 行内代码  
  5. orderedList 变成有序列表  
  6. em 斜体  
  7. strong 粗体  
  8. H1~H2 变成对应大小的标题  
  9. 
