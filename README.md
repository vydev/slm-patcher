# Sublime Merge Patcher

slm.py is a [python script](https://github.com/bousqi/slm-patcher) based on [deyixtan script](https://github.com/deyixtan/slt-patcher) that patches software updates and license checks on Sublime Merge Editors.

## SCRIPT COMPATIBILITY

|         Builds Supported         | Operating System |
| -------------------------------- | ---------------- |
| 1055 onwards (up to 1070)        | Windows 64-bit   |
| 1055 onwards (up to 1070)        | Linux 64-bit     |

Thanks to @tostercx that pointed out the problem and offered a solution for dark theme.

## USAGE

> python slm.py <"sublime merge executable file path">

## PATCHING

### Replacing Executable

1. Back up your original Sublime Merge Editor executable file. 
2. Download the desired patched executable from the "patched_executables" folder.
3. Copy the downloaded file into your own Sublime Merge directory.
4. Run the executable file.

<br>

# Manual Patching (Hex Editor)
## Build 1070
### Windows 64-bit
| Name                     |  Offset  | Original | Patched |
| ------------------------ | -------- | -------- | ------- |
| Initial License Check    | 0x2262E  | 0x38     | 0x08    |
|                          | 0x2262F  | 0x00     | 0x01    |
| Persistent License Check | 0x2852D  | 0x00     | 0x01    |
| Theme Check              | 0x21911  | 0x00     | 0x01    |
### Linux 64-bit
| Name                     |  Offset  | Original | Patched |
| ------------------------ | -------- | -------- | ------- |
| Initial License Check    | 0x296A6B | 0x38     | 0x08    |
|                          | 0x296A6C | 0x00     | 0x01    |
| Persistent License Check | 0x2992C7 | 0x00     | 0x01    |
| Theme Check              | 0x295CEA | 0x00     | 0x01    |
## Build 1065
### Windows 64-bit
| Name                     |  Offset  | Original | Patched |
| ------------------------ | -------- | -------- | ------- |
| Persistent License Check | 0x2780D  | 0x00     | 0x01    |
| Initial License Check    | 0x21914  | 0x38     | 0x08    |
|                          | 0x21915  | 0x00     | 0x01    |
### Linux 64-bit
TO BE FILLED
## Build 1061
### Windows 64-bit
| Name                     |  Offset  | Original | Patched |
| ------------------------ | -------- | -------- | ------- |
| Persistent License Check | 0x27735  | 0x00     | 0x01    |
| Initial License Check    | 0x2183C  | 0x38     | 0x08    |
|                          | 0x2183D  | 0x00     | 0x01    |
### Linux 64-bit
TO BE FILLED
## Build 1058
### Windows 64-bit
| Name                     |  Offset  | Original | Patched |
| ------------------------ | -------- | -------- | ------- |
| Persistent License Check | 0x2774D  | 0x00     | 0x01    |
| Initial License Check    | 0x21852  | 0x38     | 0x08    |
|                          | 0x21853  | 0x00     | 0x01    |
### Linux 64-bit
| Name                     |  Offset  | Original | Patched |
| ------------------------ | -------- | -------- | ------- |
| Persistent License Check | 0x28F65B | 0x00     | 0x01    |
| Initial License Check    | 0x28CE03 | 0x38     | 0x08    |
|                          | 0x28CE04 | 0x00     | 0x01    |
## Build 1055
### Windows 64-bit
| Name                     |  Offset  | Original | Patched |
| ------------------------ | -------- | -------- | ------- |
| Persistent License Check | 0x2774D  | 0x00     | 0x01    |
| Initial License Check    | 0x2184E  | 0x38     | 0x08    |
|                          | 0x2184F  | 0x00     | 0x01    |
### Linux 64-bit
| Name                     |  Offset  | Original | Patched |
| ------------------------ | -------- | -------- | ------- |
| Persistent License Check | 0x28F66F | 0x00     | 0x01    |
| Initial License Check    | 0x28CE13 | 0x38     | 0x08    |
|                          | 0x28CE14 | 0x00     | 0x01    |
<br>
