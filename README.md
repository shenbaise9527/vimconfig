# vimconfig,基于vim8.1.1
1. 下载http://github.com/VundleVim/Vundle.Vim到~/.vim/bundle中.
2. 把zya_vimrc修改为.vimrc放到home目录下.
3. 针对ycm手动安装,其它插件采用命令:PluginInstall自动安装.
4. 针对vim-go还需要额外执行命令:GoInstallBinaries来自动安装依赖库.
5. 针对ycm的安装,参考官网,命令python3 install.py --clang-completer --go-completer来支持C/C++和Golang
6. ycm支持go,需要先设置好GOPROXY,否则会失败.
7. export GOPROXY=https://mirrors.aliyun.com/goproxy,在.bashrc/.zshrc中添加该项.
