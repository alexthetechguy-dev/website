---
layout: post
title:  "Installing Linux again... bootloader...pain"
date:   2025-06-30 22:10:18 +0100
categories: [linux]
---
I can't believe how hard it was to install a Linux Distro without the bootloader showing the dreaded *"Minimal BASH Like Line Editing is Supported GRUB".*

To get to towards a solution I had to install debian not once, twice but thrice over the weekend. 

After installation, I tried [https://www.geeksforgeeks.org/how-to-fix-minimal-bash-like-line-editing-is-supported-grub-error-in-linux](https://www.geeksforgeeks.org/how-to-fix-minimal-bash-like-line-editing-is-supported-grub-error-in-linux/) articles to boot into Debian but to no avail. I then said, f***it lets try another distro and decided on Linux Mint Debian Edition (LMDE) image for fun instead. I like their community and for my personal pc its good enough.

Like previous debian install, I was using the manual partition scheme. The reason for doing this over guided one because i felt guided partition does not give good defaults in my opinion and was super simple to create partitions manually. EFI, swap, root, simple.

After doing all the installation, i restarted my machine and... no, the same annoying message as before. Then I'm thinking if both distros didn't complain then it must be BIOS related, so i went to my fancy point and click UEFI Bios and to boot section and found this boot BBS priorites list containing

- Ubuntu (with drive info in name)
- Debian (with drive info in name)
- Debian

interestingly i pick the first Debian (with drive info in name), still no luck and then decided to go for next one and then this i get the lovely mint bootloader (maybe based on grub not sure) shows up, a worthwhile install, loving it!

![Grub2-Mint.png](/assets/grub2-mint.png)

What's next I need to learn how to clear the old BBS versions, i don't know where it creates it whether in ROM or on disk, i don't really care.

I also disabled secure boot to get an install. i shall re-enable in a bit.

Good night

```txt

      _____|~~\_____      _____________
  _-~               \    |    \
  _-    | )     \    |__/   \   \
  _-         )   |   |  |     \  \
  _-    | )     /    |--|      |  |
 __-_______________ /__/_______|  |_________
(                |----         |  |
 `---------------'--\\\\      .`--'
                              `||||
```