# heimdall-exp


https://wiki.cyanogenmod.org/w/Install_and_compile_Heimdall#Generic_Linux_Instructions

sudo yum groupinstall "Development Tools"
sudo yum install libusb1-devel qt-devel libtool
sudo yum install epel-release
sudo yum -y install --enablerepo="epel" qt5-qtbase-devel

git clone git://github.com/Benjamin-Dobell/Heimdall.git
mkdir -p Heimdall/build
cd Heimdall/build
cmake -DCMAKE_BUILD_TYPE=Release ..
make

[vagrant@localhost build]$ make
Scanning dependencies of target pit
[  3%] Building CXX object libpit/CMakeFiles/pit.dir/source/libpit.cpp.o
Linking CXX static library libpit.a
[  3%] Built target pit
Scanning dependencies of target heimdall
[  7%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/Arguments.cpp.o
[ 11%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/BridgeManager.cpp.o
[ 14%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/ClosePcScreenAction.cpp.o
[ 18%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/DetectAction.cpp.o
[ 22%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/DownloadPitAction.cpp.o
[ 25%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/FlashAction.cpp.o
[ 29%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/HelpAction.cpp.o
[ 33%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/InfoAction.cpp.o
[ 37%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/Interface.cpp.o
[ 40%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/main.cpp.o
[ 44%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/PrintPitAction.cpp.o
[ 48%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/Utility.cpp.o
[ 51%] Building CXX object heimdall/CMakeFiles/heimdall.dir/source/VersionAction.cpp.o
Linking CXX executable ../bin/heimdall
/usr/bin/ld: cannot find -lPRIVATE
/usr/bin/ld: cannot find -lPRIVATE
collect2: error: ld returned 1 exit status
make[2]: *** [bin/heimdall] Error 1
make[1]: *** [heimdall/CMakeFiles/heimdall.dir/all] Error 2
make: *** [all] Error 2



sudo cp bin/* /usr/local/bin
