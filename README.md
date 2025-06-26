# Auto Custom Recovery Builder

A simple tool to automatically build a TWRP, PBRP, OFRP, or SHRP recovery image for your Android device. 📱

[<img src="https://github.com/user-attachments/assets/f07a9fd8-4e59-481f-a16a-3e81e6f49dba">](https://discord.gg/3zbfaTNN7V)

Compile your first custom recovery via GitHub Actions.

This repo comes from a long chain of forks and finally ended up with a working SHRP and some revamping of the workflow files to work for older android devices (tested with 9.0). 

It uses github noreply account (if you don't know what that is, read the last section in notes).

If there are any issues relating to the build tree info (not the workflow file config entries), feel free to open a pull request.

## 💡 Usage

1. Fork this repository.

2. Go to `Action` tab > `All workflows` > Pick which Build you need (`TWRP` or `PBRP` or `OFRP` or `SHRP`) > `Run workflow`, then pick required information from each drop-down list:
 - Manifest Branch (*12.1, *11.0, *10.0, *9.0, *8.1, *7.1, *6.0, 4.4 only for TWRP, etc.)
 - Device Tree (Your device tree repository link)
 - Device Tree Branch (Your device tree repository branch)
 - Build Target (boot, recovery, vendorboot)


## About LDCHECK

  You can use LDCHECK to get info about dependencies or drivers that are missing for encryption, and help in looking for the drivers that would be needed from your root folders. 
  You can check out the wiki (Currently WIP, planning to add BoardConfig flags based on manifest-branch, ways to debug (like finding .xml files)), where you can add a path to a LDCHECK file, as well as your device, processor info (might make it more specific later)

 - LDCHECK (path to your target binary file, i.e., `system/bin/qseecomd`)
   - If you are building manually/locally and you want to use ldcheck for checking dependencies, visit [THIS](https://github.com/TeamWin/android_device_qcom_twrp-common/tree/android-11#using-ldcheck-to-find-dependencies) for a guide.

## Notes

- If you created your account on GitHub.com after July 18, 2017, your noreply email address for GitHub is an ID number and your username in the form of ID+USERNAME@users.noreply.github.com. If you created your account on GitHub.com prior to July 18, 2017, and enabled Keep my email address private prior to that date, your noreply email address from GitHub is USERNAME@users.noreply.github.com. You can get an ID-based noreply email address for GitHub by selecting (or deselecting and reselecting) Keep my email address private in your email settings.

### Old notes ( Not relevant anymore )

> - Some of PBRP's branches have missing pb_build.sh files (like 9.0), so the build will fail, but you can still flash the recovery.img, and it will be uploaded to releases. For the .zips, you can go to PBRP's vendor utils repo and find them there in PBRP/tools (location may vary).
> - Why Ubuntu-20.04 for some workflows? Because python-is-python2 is replaced with python-is-python3 past 20.04.

## 🤝 Support

If you run into any issues, check out our **[Discord server](https://discord.gg/3zbfaTNN7V)** or open a GitHub issue to let us know!

[<img src="https://github.com/user-attachments/assets/f61046f5-1dc5-4b0c-87f8-4a94d6cbac96">](https://discord.gg/3zbfaTNN7V)

**⭐ If this tool was of any use to you, please consider giving it a Star - it would make my day! ⭐**

## Thanks/Credits
 - [CaptainThrowback](https://github.com/CaptainThrowback)
 - [azwhikaru](https://github.com/azwhikaru)
 - [cd-Crypton](https://github.com/cd-Crypton)
 - [that1](https://github.com/that1)
 - [carlodandan](https://github.com/carlodandan)
 - And to all Contributors in every repository and script I used.
 - [Recovery builder (derived from) and lazycodebuilder](https://github.com/lazycodebuilder/Lazy_Action-Recoverys-Builder)
 - [ZH-XiJun](https://github.com/ZH-XiJun) - android 4.4 support

[<img src="https://img.shields.io/badge/GitHub-Actions-blue?style=for-the-badge&logo=github-actions&logoColor=white">](https://github.com/NoahDomingues/Auto-Custom-Recovery-Builder/actions) [<img src="https://img.shields.io/badge/Discord-%235865F2.svg?style=for-the-badge&logo=discord&logoColor=white">](https://discord.gg/3zbfaTNN7V)


<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer" />
</div>
