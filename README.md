# oh-my-zsh-forcz

## 第一步：
非root环境下安装zsh：https://blog.csdn.net/TinyJian/article/details/84034812


## 安装好并ncurses和zsh后

 - cd ncurses
 - export CXXFLAGS=" -fPIC"
 - export CFLAGS=" -fPIC"
 - ./configure --prefix=$HOME --enable-shared
 - make
 - make install
 - cd ..
 - cd zsh
 - INSTALLATION_PATH=$HOME
 - export PATH=$INSTALLATION_PATH/bin/:$PATH
 - export LD_LIBRARY_PATH=$INSTALLATION_PATH/lib:$LD_LIBRARY_PATH
 - export CFLAGS=-I$INSTALLATION_PATH/include
 - export CPPFLAGS="-I$INSTALLATION_PATH/include"
 - export LDFLAGS="-L$INSTALLATION_PATH/lib"
 - ./configure --prefix=$HOME --enable-shared
 - make
 - make install
 - cd ..
 - echo 'export PATH="$HOME/bin:$HOME/.local/bin:$PATH"' >> ~/.profile
 - echo '[ -f $HOME/bin/zsh ] && exec $HOME/bin/zsh -l' >> ~/.bash_profile

 - exit
 - touch ~/.zshrc
 - wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh
 - zsh

### myagnoster.zsh-theme 
chenzhuo/.oh-my-zsh/themes

----
### chenzhuo/.oh-my-zsh/custom/plugins
放到上面这个目录或者：

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting



