# Write-Bug
README.md叙述了实习期间遇到的问题和解决方案
## 环境配置问题
#### 1. VScode powershell不允许运行脚本解决方案
以管理员打开身份打开powershell，执行`set-ExecutionPolicy RemoteSigned`命令，执行`get-ExecutionPolicy`查看修改结果  
或者  
更改VSCode终端为cmd(默认是powershell)  
![pic1](https://github.com/dafeiq9977/Write-Bug/tree/main/pic/pic1.jpg)
#### 2. 更换npm下载源  
查看当前下载源：`npm config get registry`   // 当前下载源https://registry.npmjs.org/  
替换为淘宝源：`npm config set registry https://registry.npm.taobao.org`  
安装cnmpm：`npm install -g cnpm --registry=https://registry.npm.taobao.org`
## 2. 开发环境常用命令
npm init -y  初始化一个nodejs模块，获得一个默认配置的package.json文件  
npm install <pkg name> --save   下载包，并保存到package.json里的dependencies中  
npm install <pkg name> --save-dev 下载的包保存在dependencies和devDependencies中  
npm install <pkg name>@3.0.0  安装指定版本的包  
node版本规则：  
  3.2.1
  最后一位的.1：微小的修改（bug fix或者其它微小的改动）
  中间一位的.2：增加了新的特性，但是没有对原有的功能进行修改  
  最前一位的.3：新版本与之前的版本不再兼容  
npm uninstall <pkg name>  卸载指定包和这个包的依赖  
npm uninstall --save-dev <pkg name>  卸载devDependencies这个包  

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
## 4. vue2  
## 5. CSS  
#### CSS颜色表示  
    rgb(255, 255, 255)
    rgba(255, 255, 255, 1)
    hsl(120,100%,50%)
    hsla(120,100%,50%,1)  
#### CSS设置网页图标  
    `<link rel="icon" href="../../../static/favicon2.ico" type="image/x-icon" />`
