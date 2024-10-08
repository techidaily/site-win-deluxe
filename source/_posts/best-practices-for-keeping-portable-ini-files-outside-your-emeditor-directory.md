---
title: Best Practices for Keeping Portable INI Files Outside Your EmEditor Directory
date: 2024-10-06T18:11:39.061Z
updated: 2024-10-08T18:03:24.727Z
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
<li><a href="https://vp-tips.techidaily.com/new-2024-approved-basic-guide-to-windows-voice-modification-clowns/"><u>[New] 2024 Approved Basic Guide to Windows Voice Modification - Clowns</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/new-in-2024-when-should-you-share-your-insta-story/"><u>[New] In 2024, When Should You Share Your Insta Story?</u></a></li>
<li><a href="https://vp-tips.techidaily.com/updated-2024-approved-transforming-spoken-words-into-written-text-using-in-built-tools-of-office-suite-ms-word/"><u>[Updated] 2024 Approved Transforming Spoken Words Into Written Text Using In-Built Tools of Office Suite - MS Word</u></a></li>
<li><a href="https://techidaily.com/how-to-transfer-whatsapp-from-apple-iphone-11-pro-to-other-iphone-14-pro-devices-drfone-by-drfone-transfer-whatsapp-from-ios-transfer-whatsapp-from-ios/"><u>How To Transfer WhatsApp From Apple iPhone 11 Pro to other iPhone 14 Pro devices? | Dr.fone</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/1726221805438-m4a-vob-movavi/"><u>M4A VOB 영상 전환에 대한 가이드: 좋은 다이빙 서비스는 무료로 액세스하기 - Movavi</u></a></li>
<li><a href="https://fox-that.techidaily.com/master-dictation-features-on-iphone-overcome-common-setbacks-with-these-five-techniques/"><u>Master Dictation Features on iPhone: Overcome Common Setbacks with These Five Techniques</u></a></li>
<li><a href="https://android-unlock.techidaily.com/rootjunky-apk-to-bypass-google-frp-lock-for-lenovo-by-drfone-android/"><u>Rootjunky APK To Bypass Google FRP Lock For Lenovo</u></a></li>
<li><a href="https://location-social.techidaily.com/simple-and-effective-ways-to-change-your-country-on-youtube-app-of-your-motorola-moto-g14-drfone-by-drfone-virtual-android/"><u>Simple and Effective Ways to Change Your Country on YouTube App Of your Motorola Moto G14 | Dr.fone</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/stream-and-keep-how-to-permanently-download-songs-from-iheartradio/"><u>Stream & Keep: How To Permanently Download Songs From iHeartRadio</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/top-replacement-for-internet-download-manager-on-macos-and-windows-discover-allvsoft/"><u>Top Replacement for Internet Download Manager on macOS & Windows: Discover Allvsoft</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/top-tools-for-saving-beeg-videos-cross-platform-solutions-for-windows-and-macos-users/"><u>Top Tools for Saving Beeg Videos: Cross-Platform Solutions for Windows and macOS Users</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/tutorial-how-to-retrieve-and-save-video-content-from-usa-today-across-both-macos-and-windows-platforms/"><u>Tutorial: How to Retrieve and Save Video Content From 'USA Today' Across Both macOS & Windows Platforms</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/ultimate-walkthrough-access-and-enjoy-spotify-with-the-fitbit-versa-watch/"><u>Ultimate Walkthrough: Access and Enjoy Spotify with the Fitbit Versa Watch</u></a></li>
<li><a href="https://windows11.techidaily.com/unblocking-application-could-not-find-qt-plugin/"><u>Unblocking Application Could Not Find Qt Plugin</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2027162/19272" target="_top" id="2027162">
  <img src="//a.impactradius-go.com/display-ad/19272-2027162" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2027162/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

