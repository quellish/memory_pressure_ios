# memory_pressure_ios

Apple provides the source to the macOS `memory_pressure` command here:
https://opensource.apple.com/source/system_cmds/system_cmds-790.30.1/memory_pressure.tproj/
Apply this patch and build for iOS:

`patch memory_pressure.c < memory_pressure_ios.patch`

You can build the tool using clang:
`xcrun -sdk iphoneos gcc -arch arm64 -o memory_pressure *.c`

Note that this is a comamnd line tool and with some options should be run as a priveledged user. You will need a jailbroken device to use it.