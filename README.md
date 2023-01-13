# CSFlashPlayer
Adding support for modern browsers to open SWF in Adobe with CSFP.

## How to use:

1. Download this tool from release.
2. Extract it to any location you want.
3. Run CSFP.exe one time, accept user admin control pop out to update registry.
4. Open a flash page that supports CSFlashPlayer, click the "PLAY with CSFlashPlayer" link.

## How to use on all sites:

* We need a user script to add buttons on flash plugin objects (NOT READY!).

1. Install user script browser extension Tampermonkey.  
   Chrome: https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo  
   Firefox: https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/   
2. Click Tampermonkey icon -> Dashboard -> Utilities -> Install from URL, copy and paste this url to install: https://raw.githubusercontent.com/6306/CSFlashPlayer/main/ScriptInjector.user.js

## How to use for Webmaster:

You will need to combine the scheme header with base64 encoded SWF full path as a launch url using the example below.
Example: var url = "csflash://" + base64encode("http://yoursite.com/"+swfpath);

Hints for Webmaster:
* SWFpath does not need a urlencode.
* Modern browsers has built in base64encode function, just: btoa(swfpath) .
* If you open the launch url in a new window, it will leave a blank window, if not, the web page will stop functioning after launch. Solution: Open in a hidden iframe.

## Issue self check list:
<pre>
When you click a "PLAY with CSFlashPlayer" or "CSFlashPlayer" button:
Q1. Nothing happened.
	A11. your CSFlashPlayer was not registered correctly. please run CSFP.exe to register.
		Q111. Nothing happens when I run CSFP.exe
			A111. You need .net Framework 4.6.1 to run this program.
	A12. Your web browser or antivirus blocked the request, check your browser's application setting or try in another web browser.

Q2. a blank window and it's keeps blank forever.
	A21. click file menu, you will see a url on position 1, carefully type and open it in your web browser to test the file is reachable.
		Q211. I saw a browser check or a captcha, or I saw the check a while ago.
			A211: Your network was marked as unsafe by the firewall, you need to download and play offline, or use a proxy.
		Q212. I can download the file but I'm using a proxy.
			A212: You need to proxy the flashplayer.exe also.                                   
</pre>

If your problem is not listed above, create a new issue.








May have taken this from some other source...
