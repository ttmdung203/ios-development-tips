# Run script to generate build number automatically:

```
#!/bin/bash
buildNumber=$(date -u "+%Y%m%d%H%M")
sortversion=`/usr/libexec/PlistBuddy -c "Print :CFBundleShortVersionString" "$INFOPLIST_FILE"`
/usr/libexec/PlistBuddy -c "Set :CFBundleVersion $sortversion.$buildNumber" "$INFOPLIST_FILE"
```
