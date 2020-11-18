# WebbyP – Overview

During a recent design side project project, my wife was asked to provide web optimised images (usually handled by the devs in her team). It being 2020, when she asked me about it, I suggested sharing [WebP images](https://caniuse.com/webp), as well as some optimised PNGs for desktop Safari users (IMO, the most irritating browser since Internet Explorer).

I wasn't aware of any off-the-shelf batch converters – other than [webpify](https://github.com/Chrico/webpify), which isn't very designer friendly and has a homebrew and Java as dependencies 🤢 – so I chose to use Google's [cwebp](https://developers.google.com/speed/webp/docs/cwebp) utility with a bash script and a [macOS folder action](https://developer.apple.com/library/archive/documentation/LanguagesUtilities/Conceptual/MacAutomationScriptingGuide/WatchFolders.html) in [Automator](https://support.apple.com/en-gb/guide/automator/welcome/mac).

![Demonstration of installation and usage](https://github.com/jrmedd/webbyp/raw/master/webbyp.gif)

## Installation

* Download and unzip this repo
* You can go ahead and delete the **README.md** and **webbyp.gif** files, unless you want to keep them.
* Double click the **WebbyP** workflow file in the resulting **webbyp** folder 
* Ensure the *Folder Action will be attached to:* has **webbyp** (this directory) selected and click *Install* and *Done*. The workflow file will now disappear.
* Right-click or Ctrl+click the **webbyp** folder and click *Folder Actions Setup*.
* Click *Run Service*, if prompted.
* In the right-hand column of the *Folder Actions Setup* window, click the *+* icon underneath and select **WebbyP** from the list of scripts, click the *Attach* button to confirm this.
* Close the *Folder Actions Setup* window and the installation is complete.

## Usage

* Drag and drop PNGs into the *webbyp* folder.
* On your first use, **png** and **webp** folders will appear.
* The folder action will move your PNGs into the **png** folder, and resulting WebP images will appear in the **webp** folder.
* At the time of writing, any files with the same name will be overwritten without warning, so be careful.

## To do

- [x] Simple webp conversion
- [ ] Optimised PNG conversion
- [ ] WebM/GIF support
- [ ] JPG support (maybe)
- [ ] Prompt to alter compression quality
- [ ] Ability to globally install `cwebp` for installation on other directories
- [ ] Warnings for overwrites
- [ ] Markup generator for `picture`/`srcset`