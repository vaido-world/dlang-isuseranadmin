# dlang-isuseranadmin

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

