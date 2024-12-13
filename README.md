# appxpackaging_mod

## Introduction

MakeAppx.exe installed on the directories such as `C:\Program Files (x86)\Windows Kits\10\bin\10.0.22621.0\x64` has a problem that it could not process ST component on the publisher field.

This makes it almost impossible to use code signing certificates that has such subject:

```
C=JP, ST=Tokyo, L=Tokyo, O=Open Source Developer, CN="Open Source Developer, Takashi Kawasaki"
```

The project is patching appxpackaging.dll to work with ST component.
