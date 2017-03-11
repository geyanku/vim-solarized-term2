# vim-solarized-iTerm2
在MAC OS X上使用term2终端安装vim和ls的solarized配色方案。  
## 资源下载
终端：[iTerm2官网](http://www.iterm2.com/)    
配色方案：[solarized](https://github.com/altercation/solarized)  
## 步骤
### step 1  
解压下载好的iTerm2文件，并运行其中的可执行文件。检查是否安装成功  
### step 2
下载solarized代码:  

    git clone https://github.com/altercation/solarized.git
进入`solarized/iterm2-colors-solarized`目录，分别双击执行`Solarized Dark.itermcolors`和`Solarized Light.itermcolors`  
此时，`Dark`和`Light`配色方案会导入到iTerm2中。  
### step 3
将`solarized/vim-colors-solarized/colors`下的`solarized.vim`文件拷贝到`~/.vim/colors/`目录下
    mkdir -p ~/.vim/colors
    cp vim-colors-solarized/colors/solarized.vim ~/.vim/colors
### step 4  
编写`~/.vimrc`文件  

    vim ~/.vimrc
    
    // 文件中填写下面内容
    set ts=2
    set nu
    set autoindent
    syntax enable
    set background=dark
    colorscheme solarized
### step 5  
退出`~/.vimrc`编辑模式，`vim`主题添加成功
### step 6
将配色应用到`ls`中  

    vim ~/.bash_profile

    // 在文件中添加下面一行
    export CLICOLOR=1
### step 7
退出输入`ls`查看是否配色生效  
