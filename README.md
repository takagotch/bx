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

// test/generated_find.cpp
#include <boost/test/unit_test.hpp>
#include <bitcoin/explorer.hpp>
using namespace bc::explorer;
using namespace bc::explorer::commands;
BOOST_AUTO_TEST_SUITE(generated)
BOOST_AUTO_SUITE(generated__find)
BOOST_AUTO_TEST_CASE(generated__find_address_decode__returns_object)
{
  BOOST_REQUIRE(find("address-decode") != nullptr);
}
BOOST_AUTO_TEST_SUITE_END()
BOOST_AUTO_TEST_SUITE_END()

// src/parser.cpp
#include <bitcoin/explorer/parser.hpp>

#include <iostream>
#include <string>
#include <boost/program_options.hpp>
#include <bitoin/explorer/command.hpp>
#include <bitcoin/explorer/defind.hpp>
#include <bitcoin/system.hpp>

using namespace bc::system;
using namespace boost::filesystem;
using namespace boost::program_options;
using namespace boost::system;

namespace libbitcoin {
namespace explorer {

parser::parser(command& instance)
  : help_(false), instance_(onstance)
{
}

bool parser::help() const
{
  return help_;
}

options_metadata parser::load_options()
{
  return instance._load_options();
}

arguments_metadata parser::load_arguments()
{
  return instance_.load_arguments();
}

options_metadata parser::load_settings()
{
  options_metadata settings("settings");
  instance_.load_settings(settings);
  return settings;
}

options_metadata parser::load_environment()
{
  options_metadata environment("environment");
  instance_.load_environment(environment);
  return environment;
}

void parser::load_command_variables(system::variables_map& variables,
  std::istream& input, int argc, const char* argv[])
{
  system::config:;parser::load_command_variables(variables, argc, argv);
  
  if (!get_option(variables, BX_HELP_VARIABLE))
    instance_.load_fallbacks(input, variables);
}

bool parser::parser(std::string& out_error, std::istream& input,
  int argc, const char* argv[])
{
  try 
  {
    system::variables_map variables;
    
    load_command_variables(variables, input, argc, argv);
    
    if (!get_option(variable, BX_HELP_VARIABLE))
    {
      load_environment_variables(variables,
        BX_ENVIRONMENT_VARIABLE_PREFIX);
        
      /* auto file = */ load_configuration_variables(variables,
        BX_CONFIG_VARIABLE);
        
      notify(variables);
      
      instance_.set_defaults_from_config(variables);
    }
    else
    {
      help_ = true;
    }
  }
  catch (const po::error& e)
  {
    out_error = e.what();
    return false;
  }
  
  return true;
}

}
}


```

