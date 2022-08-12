---
layout: post
title:  "winget and Get-WindowsUpdate"
author: adeesha
categories: [Windows]
tags: [ PowerShell,Windows Update ]
image: "https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cov/****.jpg"

---

වින්ඩෝස් වල අප්ඩේට් කියන්නෙ නං තනිකර වාතයක්. මේක සාමාන්‍ය පරිගණක භාවිතා කරන කෙනෙක් ගෙ ඉඳල පරිගණක භාවිතය ගැන හොඳ දැනුමක් තියන කෙනෙක් දක්වා අතිශය බහුතරයකගේ මතය. ඇත්තටම ඒකට වරදක් කියන්න බෑ. මොකද ඒක වාතයක් ම තමයි.

වින්ඩෝස් අප්ඩේට් වදයක් වෙන එක සෑහෙන තරම් දුරකට අඩු කරගන්න පුළුවන්. හැබැයි ඒ ටර්මිනල් එකේ පොඩි වැඩ ටිකක් දාන්න කැමතිනං විතරයි. අපි බලමු කොහොමද ඒක කරන්නෙ කියල.

ඒ ඔක්කොටම කලින් අපි පොඩි වැඩක් කරන්න ඕනි. ඒ පවර්ශෙල් එකේ ස්ක්‍රිප්ට් රන් කරන්න ඉඩ දෙන විදිහට හදාගන්න එක.

මුලින්ම පවර්ශෙල් එක Administrator privilege එක්ක ඕපන් කරගන්න ඕනි. වින්ඩෝස් කී එක ඔබල powershell කියල සර්ච් කරහම සාමාන්‍යයෙන් පෙන්නනව. ඒක උඩ රයිට් ක්ලික් කරල Run as Administrator කියල දෙන්න ඕනි. එතකොට එන User account control dialog box එකේ Yes කියල ( අම්මප ඔවු කියල ) කියන්නත් ඕනි.

දැන් පවර්ශෙල් එකේ  Get-ExecutionPolicy -list කියල ටයිප් කරල එන්ටර් කරන්න. සාමාන්‍ය වින්ඩෝස් PC එකක පහල SS එකේ වගේ තියෙන්න ඕනි.



<img title="" src="https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cont/getexecpol.JPG" alt="Get-ExecutionPolicy" width="654">



ඊට පස්සෙ 

Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine

හරි එහෙමත් නැත්තං

Set-ExecutionPolicy  RemoteSigned

කියල ටයිප් කරල එන්ටර් කරන්න ඕනි. දැන් කලින් විදිහට Execution Policy චෙක් කරල බැලුවහම LocalMachine එකේ Execution Policy එක RemoteSigned කියල වෙනස් වෙලා තියෙන්න ඕනි.



![Set-ExecutionPolicy](https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cont/setexecpol.JPG)



දැන් අපිට ඉස්සරහට වැඩ ටික කරගන්න පුළුවන්.

## Get-WindowsUpdate

මේක තමයි වින්ඩෝස් මෙහෙයුම් පද්ධතිය සම්බන්ධ යාවත්කාලීන කිරීම් කරන්න උපකාරී වෙන මොඩියුල් එක. පවර්ශෙල් එක හරහා වින්ඩොස් අප්ඩේට් කරන්න ඕනි නං මේ මොඩියුල් එක ඉන්ස්ටෝල් කරගන්න වෙනව.
කරන්න තියෙන්නෙ පොඩි දෙයයි. Install-Module PSWindowsUpdate කියල ටයිප් කරල එන්ටර් කරන එකයි  විතරයි.
