# 卸载
``` go
sudo apt-get remove --purge vi vim-tiny vim vim-runtime gvim vim-common vim-gui-common vim-nox
```

# 删除残余文件
``` go
sudo find / -name "*vim*" > ~/find_vim_result
// 删除时需要注意,一项一项进行比对,不要误删系统文件了
```

# 下载文件
``` go
// 从github上clone最新的.
git clone https://github.com/vim/vim.git

// 从官网上下载.
https://www.vim.org/download.php
```

# 安装依赖
``` go
//在ubuntu上.
sudo apt install libncurses5-dev libgnome2-dev libgnomeui-dev libgtk2.0-dev libatk1.0-dev libbonoboui2-dev libcairo2-dev libx11-dev libxpm-dev libxt-dev python3-dev git
```
# configure vim
``` go
./configure --with-features=huge \
    --enable-multibyte \
    --enable-python3interp=yes \
    --with-python-config-dir=/usr/lib/python3.6/config-3.6m-x86_64-linux-gnu \
    --enable-gui=gtk2 \
    --enable-cscope \
    --prefix=/usr/local
```

# make
``` go
make VIMRUNTIMEDIR=/usr/local/share/vim/vim81
```

# install
``` go 
sudo make install
```

# vim插件
## 安装YCM
``` go
cd ~/.vim/bundle
git clone https://github.com/ycm-core/YouCompleteMe.git
// 依赖
sudo apt install build-essential cmake python3-dev
cd ~/.vim/bundle/YouCompleteMe
// 设置Goproxy,.bashrc/.zshrc
export GOPROXY=https://mirrors.aliyun.com/goproxy
python3 install.py --clang-completer --go-completer
```

## vim-go
``` go
Plugin 'fatih/vim-go'
:GoInstallBinaries
```