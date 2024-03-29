---
layout: post
title:  "Ransomware - after the encryption"
author: adeesha
categories: [Cyber Security]
tags: [ Cyber Attacks,Cyber Defence,Ransomware ]
image: "https://raw.githubusercontent.com/kenshare/cs/master/assets/images/posts/ajp/cov/ransomw.jpg"

---

මේ වෙද්දි පරිගණක පාවිච්චි කරන හැම කෙනෙක්ම වගේ දන්න, බය වෙන දෙයක් තමයි ransomware කියන්නෙ. ඇයි ransomware වලට මෙච්චර බය. ප්‍රධානම හේතුව තමයි අපේ සියලු දත්ත ලේසියකට ආයෙ ගන්න බැරි වෙන්නම වෙනස් කරන එක. එහෙම නැත්තන් encrypt කරන එක. මෙහෙම encrypt කරපු දත්ත ආපහු ගන්න එක නං ලේසි වැඩක් නෙවෙයි. මේ ලිපියෙන් කියන්නෙ Ransomware වලින් බේරෙන්නෙ කොහොමද කියන එක නෙවෙයි ransomware එකකට අහුඋනාට පස්සෙ මොකද කරන්නෙ කියල.

සාමාන්‍යයෙන් ransomware එකක් අපේ පරිගණකයට එන්නෙ දෙපාරකට. පළවෙනියට එන්නෙ බොහොම පොඩි payload එකක්. මේක අපේ පරිගණකයේ පිළියම් නොකරපු දුර්වලතාවයක් පාවිච්චි කරල ස්ථාපනය වෙනව. ඊළඟට මෙයා ශේප් එකේ එයාගෙ C2 නෙට්වර්ක් එක (command and control) හරහා එයාට අවශ්‍ය උපදෙස් දෙන සර්වර් වලට සම්බන්ධ වෙනව. ඊට පස්සෙ හෙමින් හෙමින් ransomware එකේ ප්‍රධාන payload එක පරිගණකයේ ස්ථාපනය කරනව. අදාළ ransomware එක ස්ථාපනය උනාට පස්සෙ එයා ආරක්‍ෂිත සම්බන්ධතාවයක් හරහා එයාගෙ සර්වර් එකකින් encryption key එකක් ලබාගන්නව. මෙන්න මේ key එක පාවිච්චි කරල අපේ දත්ත encrypt කරනව. ගොඩක් වෙලාවට මෙයාල පාවිච්චි කරන්නෙ AES කියන එන්ක්රිප්ෂන් මෙතඩ් එක. AES වලින් පුළුවන් ඉතාම වේගවත්ව එන්ක්‍රිප්ට් කරන්න. ඒ වගේම මේක ඉතා ආරක්ෂිතයි. 256 bit AES key එකක් පාවිච්චිකරනව කියන්නෙ ලොවෙත් ඒ එන්ක්රිප්ෂන් එක කඩන්න බෑ. ඉතිං මේ එන්ක්‍රිප්ට් කරපු කී එක තියෙන්නෙ අර ransomware එක හදපු සෙට් එක ළඟ නිසා උන්ට ගානක් දීල දත්ත ටික ආයෙ ඩික්‍රිප්ට් කරගන්න වෙනව. හැබැයි මේ වැඩේ කොහොමත් හොඳ වැඩක් නෙවෙයි. මොකද උන් ඒ සල්ලි වලින් ආයෙ කරන්නෙත් ඔය බලු වැඩේම තමයි.

ඉතිං දැන් ransomware එකකින් ෂොට් එක හම්බඋනාට පස්සෙ අපි මොනවද කරන්න ඕනි.

- Ransomware එකෙන් දෙන note එකේ ෆොටෝ එකක් ගහගන්න. මේක වැදගත් වෙනව මොකක්ද ransomware එකේ වර්ගය කියල බලාගන්න.
- නිතරම පාවිච්චි කරන ෆයිල් වර්ග කිහිපයකින් සාම්පල් ෆයිල් ටිකක් හදාගන්න. මේ වැඩේ වයිරස් නැති කම්පියුටර් එකකින් කරගන්න. ඊට පස්සෙ වෙන දත්ත නැති පෙන් එකකට මේ ෆයිල් ටික දාන්න. ඔරිජිනල් ෆයිල් ටික පරිස්සමින් තියාගන්න. දැන් අර ෆයිල් දාපු පෙන් එක ransomware එක තියන මැෂින් ඒකට ගහල ඒ ෆයිල් encrypt වෙන්න ඉඩ අරින්න. ඒ encrypt වෙච්ච ෆයිල් ටිකත් පරිස්සමින් තියාගන්න. Ransomware වලින් එන්ක්‍රිප්ට් කරපු දත්ත ආපහු ගන්න උදවු කරන සමහර සේවාවන් වලට මේ encrypt වෙච්ච ෆයිල් සහ ඒවගේ ඔරිජිනල් ෆයිල් ඕනි වෙනව අදාළ ransomware එක හරියටම අඳුනගන ඒකට ගැලපෙන decryption key එක හොයල දෙන්න.
- Kaspersky rescue disk වගේ මෘදුකාංගයක් පාවිච්චි කරල ransomware එකෙන් ෂොට් එක හම්බවෙච්ච මැෂින් එක ක්ලීන් කරගන්න. Kaspersky rescue disk එක තමයි දැනට ගොඩක් දෙනා පිළිගන්න හොඳම එක. මේක CD එකකට ගහල ඒකෙන් මැෂින් එක ස්කෑන් කරහම ඔක්කොම වගේ malware අල්ලල ක්ලීන් කරනව. 100%ක් නොමිළේ දෙන මෘදුකාංගයක්. මැෂින් එකකට අලුතින් වයිරස් ගාඩ් එකක් දානවනං ඊට කලින් මේක පාවිච්චි කරල මැෂින් එක ක්ලීන් කරගන්න කියල තමයි තතු දත්තෝ කියන්නෙ.
- දැන් ඔයාගෙ එන්ක්‍රිප්ට් වෙලා තියන දත්ත වලින් වැදගත් දත්ත පරිස්සමින් අරගන තියාගන්න. මොකද පස්සෙ කාලෙක decryption key එක ආපු කාලෙක ෆයිල් ටික ආපහු ගන්න පුළුවන්. ඒ වගේම මේ decryption key නොමිලේම ප්‍රසිද්ධ කරනව. අලුත්ම ransomware එකක් නං key එක එන්න ටිකක් කල් යයි.
- අන්තිමට මැෂින් එක ෆුල් ෆෝමැට් කරල හරිහමන් වයිරස් ගාඩ් එකක් දාගන්න.

> **Ransomware එකක් ආවට පස්සෙ නටනවට වඩා නොඑන තැනට වැඩ කරන එක වටිනව.**

**Image Credits**

[Cover Image](https://securityintelligence.com/)