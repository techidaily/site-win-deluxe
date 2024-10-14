---
title: "1. [B29] Enhance File Search Speed: Efficiently Querying Thousands with EmEditor Text Editor"
date: 2024-10-10T18:29:15.168Z
updated: 2024-10-14T18:42:08.953Z
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
<li><a href="https://instagram-video-files.techidaily.com/updated-2024-approved-master-the-mix-combining-youtube-links-in-stories/"><u>[Updated] 2024 Approved Master the Mix Combining YouTube Links in Stories</u></a></li>
<li><a href="https://fox-glue.techidaily.com/updated-harmonizing-songs-and-visuals-adding-youtube-music-to-videos/"><u>[Updated] Harmonizing Songs and Visuals Adding YouTube Music to Videos</u></a></li>
<li><a href="https://some-approaches.techidaily.com/updated-utilizing-snapchats-prominent-personalities-highlight/"><u>[Updated] Utilizing Snapchat's Prominent Personalities Highlight</u></a></li>
<li><a href="https://extra-information.techidaily.com/comprehensive-kinetic-study-2023/"><u>Comprehensive Kinetic Study 2023</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/efficient-text-editing-with-erase-workspace-a-comprehensive-guide-to-using-the-emeditor/"><u>Efficient Text Editing with Erase Workspace: A Comprehensive Guide to Using the EmEditor</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/emeditor-text-editor-features-macro-recording-using-prompt-based-templates/"><u>EmEditor Text Editor Features Macro Recording Using Prompt-Based Templates</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/how-to-manage-plugin-buttons-for-automated-scripting-in-emeditor-text-editor/"><u>How to Manage Plugin Buttons for Automated Scripting in EmEditor Text Editor</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-how-to-change-your-infinix-hot-40i-location-on-twitter-drfone-by-drfone-virtual-android/"><u>In 2024, How to Change your Infinix Hot 40i Location on Twitter | Dr.fone</u></a></li>
<li><a href="https://meme-emoji.techidaily.com/new-in-2024-10-best-memes-right-now-include-image-gifvideo/"><u>New In 2024, 10 Best Memes Right Now (Include Image/ GIF/Video)</u></a></li>
<li><a href="https://win-bits.techidaily.com/step-by-step-tutorial-restoring-deleted-files-quickly-on-your-windows-eon-device/"><u>Step-by-Step Tutorial: Restoring Deleted Files Quickly on Your Windows Eon Device</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/troubleshooting-file-save-issues-in-emeditor-how-to-handle-big-data/"><u>Troubleshooting File Save Issues in EmEditor: How to Handle Big Data</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/understanding-emeditors-inbuilt-character-encoding-in-version-10/"><u>Understanding EmEditor's Inbuilt Character Encoding in Version 10</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/unleashing-creativity-how-to-master-io-screen-capture-for-2024/"><u>Unleashing Creativity How to Master IO Screen Capture for 2024</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/unveiling-emeditors-latest-release-beta-version-800-professional-text-editor-insights/"><u>Unveiling EmEditor's Latest Release: Beta Version 8.00 - Professional Text Editor Insights</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2137413/7443" target="_top" id="2137413">
  <img src="//a.impactradius-go.com/display-ad/7443-2137413" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2137413/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

