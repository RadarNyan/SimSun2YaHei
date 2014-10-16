SimSun2YaHei
============

A Chromium extension made for Chinese Windows users.

Get rid of the most used yet ugly Chinese font "SimSun" which is unfortunately the default fallback font used by Chromium on Windows by replacing it with the new Chinese font intruduced in Windows Vista - "Microsoft YaHei"

Tested on Opera 25.0.1614.50 (Chrome/38.0.2125.101)

### How it works

1. First, this extension restores the user style sheet function which is removed in Chromium 33+ 

2. Now we have the ability to use some custom style sheet on any webpage, so we can use the @font-face function introduced in css3 to define some "web fonts" using the name as "SimSun", since web fonts have higher priority, the System font would be ignored, therefor we have the nice outline font "Microsoft YaHei" instead of the old ugly pixlated "SimSun"

3. Unfortunately, the above trick doesn't work when it comes to font fallback, a number of common used font would still fallback to system "SimSun" instead of our web font, so we have to define those font as web fonts as well. For example: "arial".

4. Some fonts do not exist in Windows (eg: "STHeiTi") but some web designers still love to use it, so I treated them the same as "SimSun"

### How to use

1. Just download this repo, if you downloaded it as a zip please extract it.

2. Head to your browser's extension page, hit "enable developer mode"

3. Click "Load unpacked extension…" then select the extension folder

4. Enable the extension and you're good to go!

### Changelog

v3.1

- First release on GitHub. I've been using this for quiet a while so don't be surprised by the version number starts with v3.1.
- Rebuild from scratch (v3) with some fixes (v3.1)
- Use [LESS](http://lesscss.org) to generate map.css (Please note, this project does NOT contain any tools to build map.css from map.less, any change to map.less will not affect the extension until you rebuild map.css AND don't forget to update devtools.css if you want to change the monospace font)
- Replace Developer tools code font (To make this work, you need to enable "Enable Developer Tools experiments" in about:flags, restart your browser, head to Developer Tools Settings, enable "Allow custom UI themes" under "Experiments" category)