# Sync Source:-
To sync with full history use:
```bash
repo init --no-repo-verify -u https://github.com/superior-lts/manifest.git -b thirteen --git-lfs -g default,-mips,-darwin,-notdefault
```

To save space, sync without history use:
```bash
repo init --depth=1 --no-repo-verify -u https://github.com/superior-lts/manifest.git -b thirteen --git-lfs -g default,-mips,-darwin,-notdefault
```
Then to sync up:
```bash
repo sync -c --force-sync
```

# Start the build:-

```bash
  . build/envsetup.sh
```
```bash
  lunch superior_<devicecodename>-userdebug
```
```bash
  m bacon -j$(nproc --all)
```
