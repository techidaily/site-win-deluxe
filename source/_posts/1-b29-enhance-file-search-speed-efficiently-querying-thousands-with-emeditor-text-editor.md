---
title: "1. [B29] Enhance File Search Speed: Efficiently Querying Thousands with EmEditor Text Editor"
date: 2024-10-14T10:06:04.513Z
updated: 2024-10-20T03:21:06.275Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/d7ebc6506ee84717282a71bf655d8ecabd8e6c4fafa92ca86d15ca1c4deb0528.jpg
---

## 1. [B29] Enhance File Search Speed: Efficiently Querying Thousands with EmEditor Text Editor

Viewing 14 posts - 1 through 14 (of 14 total)

* Author  
Posts
* November 7, 2007 at 8:11 pm [#4957](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/d6369e8a8a3a00e79bba94ce88d22503?s=80&d=identicon&r=g)tungwaiyip](https://www.emeditor.com/forums/users/tungwaiyip/ "View tungwaiyip's profile")  
Member  
I’m searching for a string among 2500 files spreading over a directory tree. The performance number:  
 Another program: 2 seconds  
 EmEditor: 9 minutes  
 This translates to 4.6 files per second for EmEditor v.s. 1250 files per second for the other program.  
 Another interesting observation. There are two types of files, one with .rst extension and one with .html extension. The search seems to go much faster with .html files. It takes 65 second to search through 1000 .html files. This translates to 15 files per second. Not great, but much better than average. The total files size of the .html files actually make up 75\\% of the original search.  
November 7, 2007 at 8:27 pm [#4959](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
Thanks for descriptions, but it might be more helpful if you can write which encodings those files are written with, and whether you use regular expressions, or escape sequences including new lines. A possible reason for the delay is that EmEditor internally works in Unicode, and it support Unicode-aware regular expressions. You can write exactly what you search for, and what the files are like, and you can email me sample files and more descriptions at [tech@emurasoft.com](https://tools.techidaily.com/emeditor/products/)  
 Thanks!  
November 7, 2007 at 8:33 pm [#4960](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
Also, make sure you write which options (such as Regular Expressions, Match Catch, etc.) you checked in the Find in Files dialog box. Using different options can make significant difference in search speed. Thanks!  
November 7, 2007 at 9:16 pm [#4961](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/d6369e8a8a3a00e79bba94ce88d22503?s=80&d=identicon&r=g)tungwaiyip](https://www.emeditor.com/forums/users/tungwaiyip/ "View tungwaiyip's profile")  
Member  
I’ve figured it out. The problem is in the “Encoding” listbox. The default “Configured Encoding” is the slowest. Choosing anything other than “Configured Encoding”, even if you pick something random like Korean, will give you good performance.  
 The other options I have set is “Look in subfolder” and “Use Escape Sequence”. Unfortunately I cannot post my data file. But this is irrelevant. I repeat the search over 1000 files from an open source project and the result is the same.  
November 8, 2007 at 5:27 pm [#4965](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
When “Configured Encoding” is selected in “Find in Files” dialog box, EmEditor uses the encoding configured in the File tab of the configuration properties assiciated with the file extension you are searching. In default, Text configuration uses “System Default” encoding with UTF-8 and Unicode signature detection. The UTF-8 detection can make search slower. If the “Detect All” is also checked in the File tab of the configuration properties, it may become even more slower. Please let me know which options are checked in the File tab of associated Configuration Properties.  
 Also, in what encoding do those files you search are encoded? UTF-8 or Western European (CP:1252) or any other?  
November 8, 2007 at 6:58 pm [#4966](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/d6369e8a8a3a00e79bba94ce88d22503?s=80&d=identicon&r=g)tungwaiyip](https://www.emeditor.com/forums/users/tungwaiyip/ "View tungwaiyip's profile")  
Member  
In the File tab I have these options selected:  
 \* Prompt if null char found  
 \* Prompt if invalid char  
 \* show file name w/full path  
 \* Detect BOM  
 \* Detect UTF-8  
 \* Prompt at inconsistent returns  
 \* Opening Encoding: UTF-8  
 The files I have searched should be all Ascii files.  
 Even if EmEditor is doing more detection, it just doesn’t sound right to me that one program can search all files in 2 seconds but it takes EmEditor 9 minutes. Also if I select any encoding, says UTF-8, the performance goes up dramatically to a few seconds.  
 Of course now I have a workaround as stated in my previous sentence :-)  
November 8, 2007 at 7:27 pm [#4967](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
You should change the Opening Encoding in the File tab of the configuration properties from “UTF-8” to “System Default Encoding”. That should solve this issue.  
November 9, 2007 at 1:39 am [#4968](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/acd7b53acdac566781d920744da2bbaa?s=80&d=identicon&r=g)shaohao](https://www.emeditor.com/forums/users/shaohao/ "View shaohao's profile")  
Member  
You’d better use register mode — save all settings in register, not the INI file mode — save all settings in .ini files.  
 The INI file mode will slow down the searching in files.  
November 9, 2007 at 5:53 pm [#4977](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/d6369e8a8a3a00e79bba94ce88d22503?s=80&d=identicon&r=g)tungwaiyip](https://www.emeditor.com/forums/users/tungwaiyip/ "View tungwaiyip's profile")  
Member  
This surely is a bug isn’t it? There is no explanation why it would take so long for certain combination of encoding setting.  
 Besides I tried you recommendation. It doesn’t help. Picking “utf-8” or any other encoding in the Find in File dialog however does solve the problem.  
 Is it true that choosing .ini for configuration slow things down? This is one thing to make me love EmEditor 7.  
November 9, 2007 at 6:10 pm [#4978](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
Please try beta 32, and you should find better performance. Thanks!  
November 15, 2007 at 7:33 pm [#4998](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/d6369e8a8a3a00e79bba94ce88d22503?s=80&d=identicon&r=g)tungwaiyip](https://www.emeditor.com/forums/users/tungwaiyip/ "View tungwaiyip's profile")  
Member  
Upgraded to b32 and found the same issue.  
November 15, 2007 at 10:01 pm [#4999](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
You should have seen at least some improbements. Can you please describe more details that might help me to reproduce your issue? Without descriptions, I won’t be able to reproduce your issue. Thanks!  
November 15, 2007 at 10:18 pm [#5000](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/d6369e8a8a3a00e79bba94ce88d22503?s=80&d=identicon&r=g)tungwaiyip](https://www.emeditor.com/forums/users/tungwaiyip/ "View tungwaiyip's profile")  
Member  
The procedure is the same as what has been posted in this thread. I see no difference between b29 and b32.  
 One more data point. I’m using the “exported to USB drive” version. If I just run the version installed in “C:program files” it does not seems to have this problem.  
November 15, 2007 at 11:35 pm [#5001](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
EmEditor is optimized for the Registry usage, and the USB install will slow down. If the speed is a top priority, please consider using the Registry (without INI files). I will optimize a little more for INI files, but it won’t become as fast as the Registry version.
* Author  
Posts

Viewing 14 posts - 1 through 14 (of 14 total)

* You must be logged in to reply to this topic.

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://fox-info.techidaily.com/updated-2024-approved-12-hacks-to-find-and-download-the-best-free-stock-photography/"><u>[Updated] 2024 Approved 12 Hacks to Find and Download the Best Free Stock Photography</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/2024-approved-essential-insights-for-asmr-aficionados/"><u>2024 Approved Essential Insights for ASMR Aficionados</u></a></li>
<li><a href="https://youtube-stream.techidaily.com/2024-approved-get-hd-quality-quickly-enable-av1-in-youtube-settings/"><u>2024 Approved Get HD Quality Quickly Enable AV1 in YouTube Settings</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/2024-approved-pictorial-chuckles-kapwings-memetic-composer/"><u>2024 Approved Pictorial Chuckles Kapwing’s Memetic Composer</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/beat-windows-getting-ready-error-in-windows-a-comprehensive-guide-with-9-fixes-for-windows-1187/"><u>Beat 'Windows Getting Ready' Error in WINDOWS: A Comprehensive Guide with 9 Fixes for Windows 11/8/7</u></a></li>
<li><a href="https://tech-revival.techidaily.com/chatbot-conversation-replication-techniques/"><u>Chatbot Conversation Replication Techniques</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/comment-resoudre-un-dysfonctionnement-de-ssd-m2-a-travers-le-bios-3-solutions-efficaces/"><u>Comment Résoudre Un Dysfonctionnement De SSD M.2 À Travers Le BIOS: 3 Solutions Efficaces</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/depannage-rapide-pourquoi-votre-disque-dur-nest-pas-detecte-suite-au-formatage/"><u>Dépannage Rapide : Pourquoi Votre Disque Dur N'est Pas Détecté Suite Au Formatage</u></a></li>
<li><a href="https://buynow-info.techidaily.com/determining-mobile-device-turnover-timing/"><u>Determining Mobile Device Turnover Timing</u></a></li>
<li><a href="https://extra-resources.techidaily.com/face-to-face-factor-dissecting-apples-x-and-samsungs-identification-methods/"><u>Face-to-Face Factor Dissecting Apple’s X and Samsung’s Identification Methods</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/facilita-di-ripristino-dei-tuoi-dati-cloud-in-pochi-passaggi-un-tutorial-rapido-ed-efficiente/"><u>Facilità Di Ripristino Dei Tuoi Dati Cloud in Pochi Passaggi: Un Tutorial Rapido Ed Efficiente</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/free-vs-paid-antivirus-software-which-offers-better-security/"><u>Free Vs. Paid Antivirus Software: Which Offers Better Security?</u></a></li>
<li><a href="https://screen-mirror.techidaily.com/full-guide-on-mirroring-your-meizu-21-pro-to-your-pcmac-drfone-by-drfone-android/"><u>Full Guide on Mirroring Your Meizu 21 Pro to Your PC/Mac | Dr.fone</u></a></li>
<li><a href="https://hardware-updates.techidaily.com/how-to-get-acers-wi-fi-driver-software-quickly-with-a-complimentary-download/"><u>How to Get Acer's Wi-Fi Driver Software Quickly with a Complimentary Download</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/microsoft-synctoy-ersatz-gunstige-und-kostenfreie-optionen-fur-dateisynchronisation/"><u>Microsoft SyncToy Ersatz - Günstige Und Kostenfreie Optionen Für Dateisynchronisation</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/refreshening-your-storage-device-with-quick-batal-formatting-techniques-a-step-by-step-guide-for-indonesian-users/"><u>Refreshening Your Storage Device with Quick BATAL Formatting Techniques: A Step-by-Step Guide for Indonesian Users</u></a></li>
<li><a href="https://facebook-video-recording.techidaily.com/stumble-upon-these-hidden-meme-page-treasures-for-2024/"><u>Stumble Upon These Hidden Meme Page Treasures for 2024</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/1728484565977-windows-7windows-11/"><u>Windows 7からWindows 11への無償アップグレード：すべてのデータを保護します</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/zastosowanie-serwera-windows-2019-na-przecietnosc-metali-golej-dopolnikowe-zakresy-kopiowania-zapasowego-i-reanimacji/"><u>Zastosowanie Serwera Windows 2019 Na Przeciętność Metali Gołej: Dopólnikowe Zakresy Kopiowania Zapasowego I Reanimacji</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://review-au.sjv.io/c/5597632/2135315/14409" target="_top" id="2135315">
  <img src="//a.impactradius-go.com/display-ad/14409-2135315" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://review-au.sjv.io/i/5597632/2135315/14409" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

