Windows DDK 7.1 Samples/network/trans/ddproxy

根据 DDK 中 makefile 文件在 codeblocks 中新建 native 工程

在编译器选项中增加额外选项 /GS- 禁止 Security Check 并增加 __stdcall calling convention [/Gz]

增加 makefile 文件中的宏并增加 /D_X86_

在连接器中增加额外选项 /entry:DriverEntry

右键安装驱动

卸载驱动命令
RUNDLL32.EXE SETUPAPI.DLL,InstallHinfSection DefaultUninstall 132 path-to-uninstall-dir\infname.inf

使用 cdb 进行调试时需要配置环境变量 _NT_SYMBOL_PATH=C:\Symbols*http://msdl.microsoft.com/download/symbols
