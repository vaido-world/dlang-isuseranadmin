# dlang-isuseranadmin
https://stackoverflow.com/questions/29939648/windows-8-1-isuseranadmin-returns-false-even-though-uac-is-off-and-the-user-a  
https://docs.microsoft.com/en-us/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin?redirectedfrom=MSDN  
https://forum.dlang.org/post/kbg1r4$1ae3$1@digitalmars.com
```

import core.stdc.stdio;
import core.sys.windows.windows;

extern (Windows) BOOL IsUserAnAdmin();

int main(string[] args) {
        return IsUserAnAdmin();
}
```

```
dmd test2.d shell32.lib
```

```
@ECHO OFF
cd %~dp0
test2.exe
echo %ERRORLEVEL%
ECHO 0 if not admin
ECHO 1 if admin

pause
```
