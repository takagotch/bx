### bx
---
https://github.com/libbitcoin/libbitcoin-explorer

```sh
./autogen.sh
./configure
make
sudo make install
sudo ldconfig

g++ --version
sudo apt-get install g++-4.8
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.8 50
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.8 50
sudo update-alternatives --install /usr/bin/gcov gcov /usr/bin/gcov-4.8 50
sudo apt-get install build-essential autoconf automake libtool pkg-config git

wget https://raw.githubusercontent.com/libbitcoin/libbitcoin-explorer/version3/install.sh
cmod +x install.sh

./install.sh --prefix=/home/me/myprefix --build-boost --build-zm1 --disable-shared

clang++ --version
xcode-select --install
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install autoconf automake libtool pkgconfig wget
wget https://raw.githubusercontent.com/libbitcoin/libbitcoin-explorer/version3/install.sh
chmod +x install.sh
./install.sh --prefix=/home/me/myprefix --build-boost --build-zmq --disable-shared
brew install libbitcoin-explorer
brew install bx
sudo port install autoconf automake libtool pkgconfig wget
wget https://raw.githubusercontent.com/libbitcoin/libbitcoin-explorer/version3/install.sh
chmod +x install.sh
./install.sh --prefix=/home/me/myprefix --build-boost --build-zmq --disable-shared
./install.sh CXXFLAGS="-Os -s" --prefix=/home/me/myprefix --build-boost --disable-shared
./install.sh --disable-ndebug --prefix=/home/me/myprefix --build-boost --disable-shared
./install.sh --without-tests --prefix=/home/me/myprefix --build-boost --disable-shared
./install.sh --build-dir=/home/me/mybuild --prefix=/home/me/myprefix --build-boost --disable-shared
./install.sh --prefix=/home/my/myprefix
./install.sh --build-boost --prefix=/home/my/myprefix
./install.sh --build-zmq --prefix=/home/mymyprefix
./install.sh --disable-shared --build-boost --build-zmq --prefix=/home/me/myprefix
./install.sh CXXFLAGS="-Os -s" --without-tests --disable-shared --build-boost --build-zmq --prefix=/home/me/myprefix
./install.sh --with-bash-competion-dir --prefix=/home/me/myprefix --build-boost --disable-shared
./install.sh --with-icu --build-icu --build-boost --disable-shared
./install.sh --with-qrencode --build-qrencode --build-boost --disable-shared
./install.sh --with-png --build-png --build-boost --disable-shared
./install.sh --with-icu --with-png --with-qrencode --build-icu --build-zlib --build-png --build-qrencode --build-boost --build-zmq --prefix=/home/me/myprefix
```

```cc
// test/main.cpp
#define BOOST_TEST_MODULE libbitcoin_explorer_test
#include <boost/test/unit_test.hpp>
```

