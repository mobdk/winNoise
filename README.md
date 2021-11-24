# winNoise
This PoC Execute embedded Mimikatz 

Compile to exe: C:\Windows\Microsoft.NET\Framework64\v4.0.30319\csc.exe /platform:x64 /target:exe /unsafe winNoise.cs
Compile to dll: https://github.com/mobdk/compilecs

Changing the source code, remember to update the int idx = 0x4afed; use hex editor.

EngineVal obfuscate syscall in an semi dynamic way, createing random Int32 values passed to CPU registers, version 2 will be fully dinamic. Syscall ID is added
1000 and passed to EngineVal.

Process injection both the local process or remote, to test remote start cmd prompt like this:

cmd version

and then from another cmd execute rundll32 winNoise.dll,DllMain

