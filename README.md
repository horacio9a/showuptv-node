showuptv-node
=============
showuptv-node lets you follow and archive your favorite models' shows on showup.tv

Requirements
============
[RTMPDump(ksv)](https://github.com/K-S-V/Scripts/releases) used to capture the streams.
[Node.js](https://nodejs.org/download/) used to run capturebate-node, hence the name.

Setup
=====
1. Get a [showup.tv account](https://showup.tv).
2. Install [Node.js](https://nodejs.org/download/release/) (tested with `7.9.0` and `8.1.3`).
3. Download and unpack the [code](https://codeload.github.com/horacio9a/showuptv-node/zip/master).
4. Open console and go into the directory where you unpacked the files.
5. Install requirements by running `npm install` in the same directory as `main.js` is.
6. Edit `config.yml` file and set desirable values for `username`, `password`, `captureDirectory`, `dateFormat` and `modelScanInterval`.

Running & Output
================
Be mindful when capturing many streams at once to have plenty of space on disk and the bandwidth available or you'll end up dropping a lot of frames and the files will be useless.
Before you can start capturing streams you first need to add models to your "favourite list", the number of favorites is limited. Once you've done this you're ready to start showuptv-node by running `node main.js`.
> Note: Showup.tv allows you to create only one stream per model. You can watch several models simultaneously, but you will not be able to watch one model in two browser's tabs or record and watch in the browser simultaneously.

For advanced users
==================
There are several special URLs that allow implementing some operations with a "favourite list" which you can get using this link:

[favourite list](https://showup.tv/site/favorites/)

You need to copy a 'csrf' number (something like sessionID) and you can easily edit your "favourite list" like on this example:

- add to "favourite list" http://showup.tv/site/favorites/add/1281189?csrf=839a1c53c0a3de0b90cbef86310f3e9f
- remove from "favourite list" http://showup.tv/site/favorites/remove/1281189?csrf=839a1c53c0a3de0b90cbef86310f3e9f

Number before '?csrf' is 'model UID' which you can see at the top of the "favourite list" in front of the model name.
