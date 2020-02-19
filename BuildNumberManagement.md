# Version & Build:

### Version number & Build version:
```
Version: 1.0
Build Version: 1.0.202002190539 // [version-number].yyyymmddHHMM
```


### RunScript to generate build version:

```
#!/bin/bash
buildNumber=$(date -u "+%Y%m%d%H%M")
sortversion=`/usr/libexec/PlistBuddy -c "Print :CFBundleShortVersionString" "$INFOPLIST_FILE"`
/usr/libexec/PlistBuddy -c "Set :CFBundleVersion $sortversion.$buildNumber" "$INFOPLIST_FILE"
```
