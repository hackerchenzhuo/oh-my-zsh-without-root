# oh-my-zsh-without_root

## 第一步：
非root环境下安装zsh：https://blog.csdn.net/TinyJian/article/details/84034812


## 安装好并解压ncurses和zsh后
### 下述已经存在 zsh.sh 中，直接bash zsh.sh即可
```
cd ncurses
export CXXFLAGS=" -fPIC"
export CFLAGS=" -fPIC"
./configure --prefix=$HOME --enable-shared
make
make install
cd ..
cd zsh
INSTALLATION_PATH=$HOME
export PATH=$INSTALLATION_PATH/bin/:$PATH
export LD_LIBRARY_PATH=$INSTALLATION_PATH/lib:$LD_LIBRARY_PATH
export CFLAGS=-I$INSTALLATION_PATH/include
export CPPFLAGS="-I$INSTALLATION_PATH/include"
export LDFLAGS="-L$INSTALLATION_PATH/lib"
./configure --prefix=$HOME --enable-shared
make
make install
cd ..
echo 'export PATH="$HOME/bin:$HOME/.local/bin:$PATH"' >> ~/.profile
echo '[ -f $HOME/bin/zsh ] && exec $HOME/bin/zsh -l' >> ~/.profile
```

### 以下部分需要单独运行
```
exit #退出
#....connect...

touch ~/.zshrc
wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh
zsh
```


## 然后数据拷贝进去：
### chenzhuo/.oh-my-zsh/themes
myagnoster.zsh-theme 

### 替换.zshrc

----
然后
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
### PS： 如果无法联网可以直接上传(github项目解压上传之后直接放下面这个目录)
到这个文件夹：/home/chenzhuo/.oh-my-zsh/custom/plugins

```
git clone git://github.com/joelthelion/autojump.git
./install.py
```
autojump 注意：如果下载不了需要去.zshrc里面删除包含autojump的两行
