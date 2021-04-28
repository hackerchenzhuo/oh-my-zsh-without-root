# oh-my-zsh-forcz

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

