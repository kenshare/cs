---
layout: post
title:  "Get-WindowsUpdate"
author: adeesha
categories: [Windows]
tags: [ PowerShell,Windows Update ]
image: "https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cov/updatewindows.jpg"

---

වින්ඩෝස් වල අප්ඩේට් කියන්නෙ නං තනිකර වාතයක්. මේක සාමාන්‍ය පරිගණක භාවිතා කරන කෙනෙක් ගෙ ඉඳල පරිගණක භාවිතය ගැන හොඳ දැනුමක් තියන කෙනෙක් දක්වා අතිශය බහුතරයකගේ මතය. ඇත්තටම ඒකට වරදක් කියන්න බෑ. මොකද ඒක වාතයක් ම තමයි.

වින්ඩෝස් අප්ඩේට් වදයක් වෙන එක සෑහෙන තරම් දුරකට අඩු කරගන්න පුළුවන්. හැබැයි ඒ ටර්මිනල් එකේ පොඩි වැඩ ටිකක් දාන්න කැමතිනං විතරයි. අපි බලමු කොහොමද ඒක කරන්නෙ කියල.

ඒ ඔක්කොටම කලින් අපි පොඩි වැඩක් කරන්න ඕනි. ඒ පවර්ශෙල් එකේ ස්ක්‍රිප්ට් රන් කරන්න ඉඩ දෙන විදිහට හදාගන්න එක.

මුලින්ම පවර්ශෙල් එක Administrator privilege එක්ක ඕපන් කරගන්න ඕනි. වින්ඩෝස් කී එක ඔබල powershell කියල සර්ච් කරහම සාමාන්‍යයෙන් පෙන්නනව. ඒක උඩ රයිට් ක්ලික් කරල Run as Administrator කියල දෙන්න ඕනි. එතකොට එන User account control dialog box එකේ Yes කියල ( අම්මප ඔවු කියල ) කියන්නත් ඕනි.

දැන් පවර්ශෙල් එකේ  **Get-ExecutionPolicy -list** කියල ටයිප් කරල එන්ටර් කරන්න. සාමාන්‍ය වින්ඩෝස් PC එකක පහල SS එකේ වගේ තියෙන්න ඕනි.

<img title="" src="https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cont/getexecpol.JPG" alt="Get-ExecutionPolicy" width="654">

ඊට පස්සෙ 

**Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine**

හරි එහෙමත් නැත්තං

**Set-ExecutionPolicy  RemoteSigned**

කියල ටයිප් කරල එන්ටර් කරන්න ඕනි. දැන් කලින් විදිහට Execution Policy චෙක් කරල බැලුවහම LocalMachine එකේ Execution Policy එක RemoteSigned කියල වෙනස් වෙලා තියෙන්න ඕනි.

![Set-ExecutionPolicy](https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cont/setexecpol.JPG)

දැන් අපිට ඉස්සරහට වැඩ ටික කරගන්න පුළුවන්.

## Get-WindowsUpdate

මේක තමයි වින්ඩෝස් මෙහෙයුම් පද්ධතිය සම්බන්ධ යාවත්කාලීන කිරීම් කරන්න උපකාරී වෙන මොඩියුල් එක. පවර්ශෙල් එක හරහා වින්ඩොස් අප්ඩේට් කරන්න ඕනි නං මේ මොඩියුල් එක ඉන්ස්ටෝල් කරගන්න වෙනව.
කරන්න තියෙන්නෙ පොඩි දෙයයි. **Install-Module PSWindowsUpdate** කියල ටයිප් කරල එන්ටර් කරන එකයි ඇත්තටම මේක ඉන්ස්ටෝල් කරන්නම ඕනිද කියල අහපුවහම ඔවු කියන්න Y හරි A හරි ටයිප් කරල එන්ටර් කරන එකයි විතරයි. 

<img src="https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cont/PSWindowsUpdate.JPG" title="" alt="PSWindowsUpdate" width="657">

දැන් අපිට ඕනි කරන මොඩියුල් එක ඉන්ස්ටෝල් වෙලා ඉවරයි. Get-WindowsUpdate කියල ටයිප් කරා එන්ටර් එක එබුව. දැන් අන්තර්ජාල සම්බන්ධතාවය තියනව නං අප්ඩේට් තියද කියල චෙක් කරනව. වින්ඩෝස් මෙහෙයුම් පද්ධතිය සම්බන්ධ අප්ඩේට් එහෙම තියනව නං ලිස්ට් එකම පෙන්නනව.

ඒ ලිස්ට් එකේ අප්ඩේට් එකේ KB Article ID එක, අප්ඩේට් එක මොකක්ද කියල විස්තරයක් වගේම අප්ඩේට් එකේ සයිස් එකත් තියනව. හැබැයි මෙතන පෙන්නන සයිස් එක ඇත්තටම ඩවුන්ලෝඩ් වෙන්නෙ නෑ. උදාහරණයක් හැටියට වින්ඩෝස් ඩිෆෙන්ඩර් අප්ඩේට් එක මෙගාබයිට් 875ක් කියල පෙන්නුවට ඩවුන්ලෝඩ් වෙන්නෙ අලුත්ම අප්ඩේට් ඒකට අදාළ සුළු ප්‍රමාණයක් විතරයි. හැබැයි වින්ඩෝස් ඩිෆෙන්ඩර් එක අවුරුදු ගානකින් අප්ඩේට් කරල නැත්තං සයිස් එක සෑහෙන්න ලොකු වෙන්නත් පුළුවන්. දිනපතා අප්ඩේට් කරනව නං මෙගාබයිට් එකකටත් අඩුවෙන් තමයි ඩවුන්ලෝඩ් වෙන්නෙ. හැබැයි කර්නල් අප්ඩේට් වගේ යනව නං පෙන්නන ප්‍රමාණයම ඩවුන්ලෝඩ් වෙන්න ඉඩ තියනව. අප්ඩේට් එක ගැන වැඩි විස්තර KB Article ID එක පාවිච්චි කරල ගූගල් එකේ සර්ච් කරහම හොයාගන්න පුළුවන්.

මේ ක්‍රමයේ තියන විශේෂත්වය තමයි අපි ඕනි නං ඔක්කොම අප්ඩේට් එක පාරමත් එහෙම නැත්තන් අපිට ඕනිකරන අප්ඩේට් විතරක් තෝරල තනි තනියෙනුත් ඉන්ස්ටෝල් කරන්න පුළුවන් වීම.

ඔක්කොම අප්ඩේට් ටික එකපාර ඉන්ස්ටෝල් කරන්න ඕනි නං, 
**Install-WindowsUpdate** කියල දෙන්න ඕනි.

අප්ඩේට් තියද කියල චෙක් කරල, ඔක්කොම ටික ඉන්ස්ටෝල් කරල, ඔටෝ රී ස්ටාර්ට් වෙන්නත් ඕනි නං,

**Get-WindowsUpdate -AcceptAll -Install -AutoReboot** කියල දෙන්න ඕනි.

අපිට ඕනි අප්ඩේට් එකින් එක ඉන්ස්ටෝල් කරන්න නං,

**Get-WindowsUpdate -install -kbarticleid** KB2267602 කියල දෙන්න ඕනි. මෙතන KB2267602 කියල කියන්නෙ අදාළ අප්ඩේට් එකේ KB Article ID එක. මේක අප්ඩේට් එකෙන් අප්ඩේට් එකට වෙනස් වෙනව. KB5016616 එක කියන්නෙ 2022 අගෝස්තු 9 ආපු අප්ඩේට් එක.

![WindowsUpdate All](https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cont/winupdate0.JPG)

පහල ඉමේජ් දෙකෙන් පෙන්නන්නෙ වින්ඩොස් ඩිෆෙන්ඩර් අප්ඩේට් එක ඉන්ස්ටෝල් කරන්න කලින් සහ ඉන්ස්ටෝල් කරාට පස්සෙ අවස්ථා දෙක.

![Before Update](https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cont/winupdate1.JPG)

![After Update](https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cont/winupdate2.JPG)

ඔන්න ඔය විදිහට ලේසියටත් පහසුවටත් "**හිච්චි සිස්ටම් ඇඩ්මින්**" කෙනෙක් විදිහටත් වින්ඩෝස් අප්ඩේට් කරන්න පුළුවන්.



#### **Image Credits**

[Cover Image](https://itsfoss.com/10-funny-jokes-pictures-windows-mac-linux/)
