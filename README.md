# mp4decrypt_mod_win

Modded version of mp4decrypt from:
 - https://github.com/NanDesuKa-FR/mp4decrypt_mod_linux
 - https://www.bento4.com/

## **CHANGELOGS**:
## [1.5] | 2021-12-29
- Changed progressbar
- Removed initial info and output info (Just show progressbar so we can use custom info)
- Removed `--show-progress` arg (Just show the progress by default)
- Added `--silent` arg (Don't show any progress)
- Added `info` to append at the begninning of progressbar
    - e.g. (**--key 123:123 enc.mp4 dec.mp4 "[INFO]: "**)
        
        [INFO]: [■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■] 100%
- You can build and modified as well if you want.
---

## Compile:
    mkdir cmakebuild
    cd cmakebuild
    cmake -DCMAKE_BUILD_TYPE=Release ..

    Then build the Visual Studio Project.
---
## Usage

```cmd
usage: mp4decrypt [options] <input> <output> <info>
Options are:
  info: append to the beginning of the progressbar
  --silent : Don't show progress bar
  --key <id>:<k>
      <id> is either a track ID in decimal or a 128-bit KID in hex,
      <k> is a 128-bit key in hex
      (several --key options can be used, one for each track or KID)
      note: for dcf files, use 1 as the track index
      note: for Marlin IPMP/ACGK, use 0 as the track ID
      note: KIDs are only applicable to some encryption methods like MPEG-CENC
  --fragments-info <filename>
      Decrypt the fragments read from <input>, with track info read
      from <filename>.
```

# Demo
![](https://i.imgur.com/DLbkBgh.gif)

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Credit
All credits go to Bento4 (owner and creator of this software) and to GO3/NanDesuKa-FR for its modded version 
