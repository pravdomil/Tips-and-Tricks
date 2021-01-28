<div align="center">

# Tips and Tricks

</div>

## Miscellaneous

- [Adobe After Effects Cheat sheet](res/ae/ae.pdf)
- [Adobe Illustrator Cheat sheet](res/ai/ai.pdf)
- [MongoDB Cheat Sheet](res/mongo.md)
- [AVR Instruction Set](res/avr.md)
- [Booklet Flow](res/bookletflow.png)

## macOS

**Defaults**

Inspiration goes from [kevinSuttle](https://github.com/kevinSuttle/OSXDefaults/blob/master/.osx).

- Do not use iCloud to login, you can't change login password otherwise.
- Trackpad: Use all gestures and set speed to 100%.
- Accessibility - Mouse & Trackpad: Enable three finger drag.
- Sharing: Rename your Mac.
- Finder: Create folder called "home" in user directory and use it as default one. Favorites are: Home, User, Downloads.
- Finder Preferences: Enable "Show Path", "Show Status Bar", "Keep folders on top", "Remove items from the Trash after 30 days" and do not show things on the desktop.
- Screen Saver: Set left top hot corner to "Put Display to Sleep".
- Sound: Turn off alert volume and show volume in menu bar?
- Security & Privacy: Set require password after "5 seconds". Set show a message when the screen locked to your contact information.
- Keyboard: Turn off keyboard backlight after 1 minute? Turn off smart quotes and autocorrecting.
- Install [Pravdomil keyboard](https://github.com/pravdomil/keyboard#readme).
- [Keep Preview from auto-resizing print output](https://apple.stackexchange.com/questions/2931/keep-preview-from-autoresizing-print-output).

**Tips**

- [How to properly use drag and drop](http://apple.stackexchange.com/questions/42429/how-to-properly-use-drag-and-drop-with-macbook-pro-on-os-x-10-7).
- Use ⌥drag to set default Finder column width.
- Software:
  [VLC](http://www.videolan.org/vlc/download-macosx.html),
  [Keka](http://www.kekaosx.com/en/),
  [Retinizer](http://retinizer.mikelpr.com/),
  [GrandPerspective](http://sourceforge.net/projects/grandperspectiv/files/latest/download),
  [AppCleaner](http://www.freemacsoft.net/appcleaner/),
  [Find Any File](http://apps.tempel.org/FindAnyFile/),
  [SetResX](https://www.sendspace.com/file/mef6sk).

## Electronics

- [Falstad Circuit Simulator](http://www.falstad.com/circuit/)
- [Led Resistor Calculator](http://www.hebeiltd.com.cn/?p=zz.led.resistor.calculator)
- [6 Band Resistor Calculator](https://www.eeweb.com/toolbox/6-band-resistor-calculator/)
- [Ohm Calc](http://www.elektro-energetika.cz/calculations/ohm_zak.php)
- [Ohm's Law Analogy](http://dc226.4shared.com/img/p8u2UKlcce/s24/147267bf278/ohms-law-illustrated)
- [Ohm's Law Chart](https://cdn.shopify.com/s/files/1/0792/1843/files/misthub-ohms-law-chart1.png)

## Programming

**Tools**

- [Domain Generator](https://www.dotomator.com/web20.html)
- [Dead Link Checker](http://www.deadlinkchecker.com/)
- [What's My DNS](https://www.whatsmydns.net)
- [Regex101.com](https://www.regex101.com)
- [Can I use](http://caniuse.com/)
- [Package.json](http://browsenpm.org/package.json)
- [Nearest named color](http://www.yellowbearjourneys.com/color_themes/color_closest.html)

**Resources**

- [HTML5.diff](https://www.w3.org/TR/html5-diff/)
- [Command line args formatting](http://docopt.org/)
- [Snakes, Neural Networks and Genetic Algorithms](https://www.youtube.com/watch?v=BBLJFYr7zB8)
- [Receiving and modifying key presses on macOS](http://osxbook.com/book/bonus/chapter2/alterkeys/)
- [Node.js image processing](https://github.com/lovell/sharp)
- [Fast, simple I/O library for Arduino](https://github.com/mmarchetti/DirectIO)
- [SpeakingURL](https://github.com/pid/speakingurl)
- [WordPress Cheat Sheet](https://www.rarst.net/images/query_functions.png)
- [České služby pro WooCommerce](https://github.com/pavelevap/ceske-sluzby)
- [Polyfill.io](https://polyfill.io/v2/docs)
- [Mongo indexing on object arrays vs objects](https://stackoverflow.com/questions/9589856/mongo-indexing-on-object-arrays-vs-objects)
- [Child-Parent Communication in Elm: OutMsg vs Translator vs NoMap](https://medium.com/@_rchaves_/child-parent-communication-in-elm-outmsg-vs-translator-vs-nomap-patterns-f51b2a25ecb1)

**Server Setup**

```
ssh‑copy‑id root@$IP
ssh root@$IP
update‑locale LC_ALL=en_US.UTF‑8 LANG=en_US.UTF‑8
logout
ssh root@$IP
apt update
apt upgrade
reboot
```

SSH tunnel  
`ssh -L LOCAL_PORT:DEST:DEST_PORT TUNNEL_USER@TUNNEL_SERVER -p PORT`

Create symlink  
`ln -s SOURCE SYMLINK`
