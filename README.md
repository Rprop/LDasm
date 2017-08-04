# LDasm
Lightweight x86 and x64 instructions disassembler, extracted from [libsplice](https://github.com/vol4ok/libsplice) project.

# Usage
```C++
#include <LDasm.h>
unsigned char *pfunc = static_cast<unsigned char *>(evaluate_jmp(__$func__));
uint_fast32_t l = 0;
ldasm_data ld;
do 
{
	l += ldasm(pfunc + l, &ld);
} while (l < __$size__);
```
