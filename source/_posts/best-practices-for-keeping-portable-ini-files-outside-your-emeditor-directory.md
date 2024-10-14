---
title: Best Practices for Keeping Portable INI Files Outside Your EmEditor Directory
date: 2024-10-11T17:44:45.036Z
updated: 2024-10-14T17:59:15.089Z
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
<li><a href="https://facebook-record-videos.techidaily.com/new-2024-approved-beyond-boundaries-channel-youtube-for-exciting-green-screens/"><u>[New] 2024 Approved Beyond Boundaries Channel Youtube for Exciting Green Screens</u></a></li>
<li><a href="https://remote-screen-capture.techidaily.com/new-engaging-oratorics-assessment-version-8-for-2024/"><u>[New] Engaging Oratorics Assessment, Version 8 for 2024</u></a></li>
<li><a href="https://extra-skills.techidaily.com/new-kids-and-newbies-rejoice-our-10-easiest-to-fly-drones/"><u>[New] Kids & Newbies Rejoice! Our 10 Easiest-to-Fly Drones</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/updated-2024-approved-ultimate-tips-for-instagram-video-reverse-playback/"><u>[Updated] 2024 Approved Ultimate Tips for Instagram Video Reverse Playback</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/updated-master-the-craft-three-secrets-to-perfectly-saving-streamed-discords-for-2024/"><u>[Updated] Master the Craft Three Secrets to Perfectly Saving Streamed Discords for 2024</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/1-b29-enhance-file-search-speed-efficiently-querying-thousands-with-emeditor-text-editor/"><u>1. [B29] Enhance File Search Speed: Efficiently Querying Thousands with EmEditor Text Editor</u></a></li>
<li><a href="https://fox-access.techidaily.com/2024-approved-listenleap-escaping-dacasts-grip/"><u>2024 Approved ListenLeap Escaping DaCast's Grip</u></a></li>
<li><a href="https://vp-tips.techidaily.com/2022-dvd-3/"><u>如何在2022年保存 DVD 到電腦的最佳3種方法</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/advanced-text-editing-with-emeditor-pro-version-10-beta-8-v9908/"><u>Advanced Text Editing with EmEditor Pro Version 10 Beta 8 (V9.90.8)</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/can-you-save-and-open-file-groups-as-tabs-using-emeditor-text-processing-tool/"><u>Can You Save & Open File Groups as Tabs Using EmEditor - Text Processing Tool</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/efficient-text-editing-with-erase-workspace-a-comprehensive-guide-to-using-the-emeditor/"><u>Efficient Text Editing with Erase Workspace: A Comprehensive Guide to Using the EmEditor</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/emeditor-advanced-text-editing-software-your-ultimate-programming-companion/"><u>EmEditor - Advanced Text Editing Software: Your Ultimate Programming Companion</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/emeditor-text-editor-features-macro-recording-using-prompt-based-templates/"><u>EmEditor Text Editor Features Macro Recording Using Prompt-Based Templates</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/investigating-competitors-to-manycam-better-choices/"><u>Investigating Competitors to ManyCam Better Choices?</u></a></li>
<li><a href="https://win11.techidaily.com/minimizing-multitasking-back-end-load-in-windows/"><u>Minimizing Multitasking Back-End Load in Windows</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/new-release-alert-emeditor-pro-version-13-beta-n-latest-text-editing-software/"><u>New Release Alert: EmEditor Pro Version 13 Beta N - Latest Text Editing Software</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/understanding-emeditors-inbuilt-character-encoding-in-version-10/"><u>Understanding EmEditor's Inbuilt Character Encoding in Version 10</u></a></li>
<li><a href="https://win-deluxe.techidaily.com/unveiling-emeditors-latest-release-beta-version-800-professional-text-editor-insights/"><u>Unveiling EmEditor's Latest Release: Beta Version 8.00 - Professional Text Editor Insights</u></a></li>
<li><a href="https://article-posts.techidaily.com/visual-wit-composition-kapwings-meme-workshop/"><u>Visual Wit Composition Kapwing’s Meme Workshop</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://25home.pxf.io/c/5597632/2148639/16836" target="_top" id="2148639">
  <img src="//a.impactradius-go.com/display-ad/16836-2148639" border="0" alt="https://techidaily.com" width="180" height="90"/>
</a>
<img height="0" width="0" src="https://25home.pxf.io/i/5597632/2148639/16836" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

