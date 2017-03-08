ios-cmake
=========

Since the main repo is not maintained anymore, I created this fork with the following changes:
- Fix Policy CMP0054
- Create universal simulator for 32 and 64 bits
- Change gcc to clang and stop forcing compiler
- Add support for bitcode

I tried to use some fork of the main project, but I couldn't find a fork that has everything I need, so I create this fork with some ideas from the following repos.
-  https://github.com/Yangqing/ios-cmake
-  https://github.com/OtherLevels/ios-cmake
-  https://github.com/diegostamigni/ios-cmake

=========

A toolchain file and examples using cmake for iOS development. This is a fork of a similar project found on https://code.google.com/p/ios-cmake/

This version has been tested with xcode 5.1 and iOS SDK 7.1

In order to compile the static library for the iOS simulator 32 bit, change to the folder where the library sources reside, then:

	mkdir build
	cd build
 	cmake .. -DCMAKE_TOOLCHAIN_FILE=../../../toolchain/iOS.cmake -DIOS_PLATFORM=SIMULATOR
 	make
 	make install

 Once the library is compiled and installed, change to the folder where the sample application sources reside, then open XCode with:

 	open hello-app.xcodeproj

Set IOS_PLATFORM to OS to build for Device
