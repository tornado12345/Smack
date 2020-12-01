Building Smack
==============

Linux
-----

Building Smack is as simple as

```
git clone git@github.com:igniterealtime/Smack.git
cd Smack
gradle assemble
```

Mac
---

Smack requires a case-sensitive file system in order to build. Unfortunately, the macOS operating system is case-insensitive by default.
To get around this, you can create a case-sensitive disk image to work from.

1. Launch Disk Utility (Applications > Utilities)
2. Click the +, or go to Edit > Add APFS Volume
3. Give it a name, e.g. "Smack"
4. Change the format to "APFS (Case-sensitive)"
5. Click Add

It'll auto-mount into /Volumes, e.g. /Volumes/Smack

```bash
cd /Volumes/Smack
git clone git@github.com:igniterealtime/Smack.git
cd Smack
gradle assemble
```

Windows
-------

Smack requires a case-sensitive file system in order to build. Unfortunately, Windows NTFS is case-insensitive by default.
To get around this, you can set specific folders as case-sensitive (requires Windows 10 v1803 or higher).

In an Administrator console:

```batch
fsutil.exe file SetCaseSensitiveInfo C:\git\Smack enable
cd \git\Smack
git clone git@github.com:igniterealtime/Smack.git
cd Smack
gradle assemble
```
