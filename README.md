showuptv-node
=============
showuptv-node lets you follow and archive your favorite models' shows on showup.tv

Requirements
============
[RTMPDump(ksv)](https://github.com/BurntSushi/rtmpdump-ksv) used to recording the streams. Must be in directory with main.js or somewhwere in the path.

[Node.js](https://nodejs.org/download/) used to run showuptv-node, hence the name.

Setup
=====
Install requirements, run `npm install` in the same folder as main.js is. Add models you want to record to config.yml file.

Running & Output
================
To start capturing streams you need to run `node main.js` I recommend you do this in [screen](https://www.gnu.org/software/screen/) as that'll keep running if you lose connection to the machine or otherwise close your shell.
