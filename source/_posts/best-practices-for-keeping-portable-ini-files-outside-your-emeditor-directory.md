---
title: Best Practices for Keeping Portable INI Files Outside Your EmEditor Directory
date: 2024-10-17T19:19:24.624Z
updated: 2024-10-20T06:24:42.599Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/452af84849e74b7985a3e6edc7ef7272ddba7eb347d5e3359e01777aab493b95.png
---

## Best Practices for Keeping Portable INI Files Outside Your EmEditor Directory

Viewing 3 posts - 1 through 3 (of 3 total)

* Author  
Posts
* November 17, 2008 at 5:06 pm [#6620](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/d73fc2c7bd494149d303a2b87aa5a6d5?s=80&d=identicon&r=g)dreftymac](https://www.emeditor.com/forums/users/dreftymac/ "View dreftymac's profile")  
Participant  
Suppose I have emeditor using the INI files and that the location of the files is as follows:  
 C:ProgramsEmEditoreeCommon.ini  
 C:ProgramsEmEditoreeConfig.ini  
 C:ProgramsEmEditoreeLM.ini  
 C:ProgramsEmEditoreePlugins.ini  
 C:ProgramsEmEditoreeUseIni.ini  
 Question: Is there a way to keep these files in a \*subdirectory\* instead of inside the EmEditor program root, and still have EmEditor recognize and use the files?  
 The preferred way:  
 C:ProgramsEmEditorinifileseeCommon.ini  
 C:ProgramsEmEditorinifileseeConfig.ini  
 \[… and so on like this … \]  
 The reason for this is my system is setup to avoid backing up files that appear in a “program root” directory in order to save space. If it were possible to put them inside a \*child\* directory of the program root (or some other user configurable place), there would be no problem.  
 Thanks for any answers,  
November 17, 2008 at 5:28 pm [#6621](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
> dreftymac wrote:  
> Suppose I have emeditor using the INI files and that the location of the files is as follows:  
>  
> C:ProgramsEmEditoreeCommon.ini  
> C:ProgramsEmEditoreeConfig.ini  
> C:ProgramsEmEditoreeLM.ini  
> C:ProgramsEmEditoreePlugins.ini  
> C:ProgramsEmEditoreeUseIni.ini  
>  
> Question: Is there a way to keep these files in a \*subdirectory\* instead of inside the EmEditor program root, and still have EmEditor recognize and use the files?  
> The preferred way:  
>  
> C:ProgramsEmEditorinifileseeCommon.ini  
> C:ProgramsEmEditorinifileseeConfig.ini  
> \[… and so on like this … \]  
>  
> The reason for this is my system is setup to avoid backing up files that appear in a “program root” directory in order to save space. If it were possible to put them inside a \*child\* directory of the program root (or some other user configurable place), there would be no problem.  
>  
> Thanks for any answers,  
 I am sorry, there is no way to move those INI files into a subdirecotry. That is the way EmEditor recognizes the INI files without using the Registry settings. If you still need to move INI files into the subdirectory, let me know how you want EmEditor to determine where the INI files are.  
November 17, 2008 at 5:56 pm [#6622](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/d73fc2c7bd494149d303a2b87aa5a6d5?s=80&d=identicon&r=g)dreftymac](https://www.emeditor.com/forums/users/dreftymac/ "View dreftymac's profile")  
Participant  
For this feature to be useful (to me anyway), all that would be needed is for EmEditor to check the “program root” directory for the file:  
 C:\\%root\_directory\_of\_emeditor\_exe\\%eeCommon.ini  
 and if the file is not found there, EmEditor could check:  
 C:\\%root\_directory\_of\_emeditor\_exe\\%settingseeCommon.ini  
 If the file is found in either of these two locations, EmEditor can assume the ini files are being used. If the file is \*not\* found in either of these two locations, EmEditor can assume the Registry. Using this approach would require only the small change to EmEditor that it checks in two places instead of just one.  
 Of course, some windows applications also check in the “Documents and Settings” folder of the currently-logged-in user for windows, but I don’t need anything that fancy. All that’s needed (for me) is just a way to save the ini files in some directory besides the EmEditor program root without breaking the “use INI files” feature. If this directory is “hard coded” into EmEditor, that’s not a problem, just as long as its documented somewhere so I will know where I can put the ini files.  
 Thanks for your reply and for considering this idea, best regards.
* Author  
Posts

Viewing 3 posts - 1 through 3 (of 3 total)

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
<li><a href="https://fox-direct.techidaily.com/updated-2024-approved-audio-aficionados-curated-selection-of-free-lut-links/"><u>[Updated] 2024 Approved Audio Aficionados' Curated Selection of Free LUT Links</u></a></li>
<li><a href="https://tiktok-clips.techidaily.com/2024-approved-learn-how-to-craft-engaging-tiktok-captions-quickly/"><u>2024 Approved Learn How to Craft Engaging TikTok Captions Quickly</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/5asa5yplusw5py65a6j5ywo5a6j6kof6l2v5lu25oyh5y2xic0g5ake5by66ziy5oqk5o6q5pa9/"><u>多台机安全安装软件指南 - 增强防护措施</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/1728504199111-ccleaner/"><u>如何使用CCleaner重新建立完整文件系统：透明、詳盡教學路線</u></a></li>
<li><a href="https://extra-tips.techidaily.com/androids-premier-music-video-experience-6-picks/"><u>Android's Premier Music Video Experience 6 Picks</u></a></li>
<li><a href="https://eaxpv-info.techidaily.com/conversione-libera-online-di-file-jp2-a-jpeg-con-movavi/"><u>Conversione Libera Online Di File JP2 a JPEG Con Movavi</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/detailed-review-and-comparison-with-vlc-successors/"><u>Detailed Review and Comparison with VLC Successors</u></a></li>
<li><a href="https://fake-location.techidaily.com/fixing-foneazy-mockgo-not-working-on-samsung-galaxy-f34-5g-drfone-by-drfone-virtual-android/"><u>Fixing Foneazy MockGo Not Working On Samsung Galaxy F34 5G | Dr.fone</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/guias-iniciais-de-download-gratuito-do-aomei-backupper-em-formato-de-video/"><u>Guias Iniciais De Download Gratuito Do AOMEI Backupper Em Formato De Vídeo</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/how-to-change-your-sim-pin-code-on-your-poco-x5-phone-by-drfone-android/"><u>How To Change Your SIM PIN Code on Your Poco X5 Phone</u></a></li>
<li><a href="https://android-transfer.techidaily.com/in-2024-2-ways-to-transfer-text-messages-from-xiaomi-redmi-note-12t-pro-to-iphone-1514131211x8-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>In 2024, 2 Ways to Transfer Text Messages from Xiaomi Redmi Note 12T Pro to iPhone 15/14/13/12/11/X/8/ | Dr.fone</u></a></li>
<li><a href="https://win-howtos.techidaily.com/is-my-netflix-service-disrupted-solutions-for-common-playback-problems/"><u>Is My Netflix Service Disrupted? Solutions for Common Playback Problems</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/step-by-step-guide-building-secure-unidentifiable-emails-with-malwarefox/"><u>Step-by-Step Guide: Building Secure, Unidentifiable Emails with MalwareFox</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/transferencia-de-imagens-no-windows-tres-tecnicas-simplificadas-para-movimentacao/"><u>Transferência De Imagens No Windows - Três Técnicas Simplificadas Para Movimentação</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/transferencia-de-la-licencia-de-windows-11-al-nuevo-pc-sin-problemas/"><u>Transferencia De La Licencia De Windows 11 Al Nuevo PC Sin Problemas</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/ultimate-guide-beat-the-issue-of-not-being-able-to-sync-videos-with-itunes/"><u>Ultimate Guide: Beat the Issue of Not Being Able to Sync Videos with iTunes</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/1728500307773-windows-10usb/"><u>Windows 10用のUSBへのフォルダー自動バックアップ手段 - 試せてみましょう</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://oneplusfr.sjv.io/c/5597632/1622438/14044" target="_top" id="1622438">
  <img src="//a.impactradius-go.com/display-ad/14044-1622438" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://oneplusfr.sjv.io/i/5597632/1622438/14044" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

