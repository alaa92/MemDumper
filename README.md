## MemDumper
Dump Memory Segment From Process Memory and Rebuild So(Elf) Libraries

## Features
- No need of Ptrace
- Bypass Anti Debugging
- Dumping of Lib from Memory of Process
- Auto Dumping With Segment Name
- Manual Dumping With Custom Memory Address
- Fix and Regenerate Elf File
- Support Fast Dumping(May Miss some data)

## How to Build
- Install Android NDK, if not.
- Open Shell in Project Folder
- Use and Execute ndk-build of NDK in Project Folder
- Output will be in libs Folder.
 
## How to use
- Needs Root Access or Virtual Space
- Get Root Shell through Adb or Terminal Apps or Normal Shell into Virtual Space via Terminal Apps
- For Usage Help: memdumper -h
- For General Usage: memdumper -p <packageName> <option(s)> -o <outputPath>

## Commands
```
Help: ./memdumper -h

MemDumper v0.2 <==> Made By KMODs(kp7742)
Usage: memdumper -p <packageName> <option(s)> -o <outputPath>
Dump Memory Segment From Process Memory and Rebuild So(Elf) Libraries
-l for Library Mode, -m for Manual Dumping Mode, By Default Auto Dumping Mode
 Options:
--Auto Dump Args-------------------------------------------------------------------------
  -n --name <segment_name>              Segment Name From proc maps
--Manual Dump Args-----------------------------------------------------------------------
  -m --manual                           Manual Dump Mode for Custom Address
  -n --name <dump_name>                 Dumping File Name
  -s --start <address>                  Starting Address
  -e --end <address>                    Ending Address
--Lib Dump Args-------------------------------------------------------------------------
  -l --lib                              Dump So(Elf) Library from Memory
  -n --name <lib_name>                  Library Name From proc maps
  -r --raw(Optional)                    Output Raw Lib and Not Rebuild It
--Other Args----------------------------------------------------------------------------
  -f --fast(Optional)                   Enable Fast Dumping(May Miss Some Bytes in Dump)
  -p --package <packageName>            Package Name of App
  -o --output <outputPath>              File Output path
  -h --help                             Display this information
  
  
Dump Library: ./memdumper -p com.dts.freefireth -l -n libil2cpp.so -o /sdcard
Process name: com.dts.freefireth, Pid: 27077
Base Address of libil2cpp.so Found At b2dc4000
End Address of libil2cpp.so Found At b60b5000
Lib Size: 53415936
Dumped in 25.414995S
```

## Credits
- [SoFixer](https://github.com/F8LEFT/SoFixer): So(Elf) Rebuilding

## Technlogy Communication
> Email: patel.kuldip91@gmail.com
