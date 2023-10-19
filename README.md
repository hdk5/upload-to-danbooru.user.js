# upload-to-danbooru.user.js

(Another) userscript for uploading to Danbooru.

## Installation

* Install [Tampermonkey](https://tampermonkey.net/) extension, it's available for Chrome, Microsoft Edge, Safari, Opera Next, and Firefox.
* Download the script: https://github.com/hdk5/upload-to-danbooru.user.js/raw/master/upload-to-danbooru.user.js
* An installation prompt will appear. Accept the installation.

## Why not use the official extension?

Unlike the [browser extension](https://github.com/danbooru/upload-to-danbooru/), which aims to be lightweight and universal, this one does the opposite by supporting only very few sites and including specific hacks for them.

## Supported sites

* Fantia (`post_content_photo` type)
    * Adds the upload button to full-size image page
    * Sends the direct image url with post url as referer
    * Currently _almost_ works with the extension, but danbooru doesn't recognize the referer (at the moment) - which I don't like.
    * The full-size image page still has to be opened manually

* Fantia (`album_image` type)
    * Adds the upload button on the image in the article
    * Sends the direct image url with post url as referer
    * Doen't work (and [never will](https://github.com/danbooru/upload-to-danbooru/issues/8#issuecomment-1769268852)) with the extension

* Fantia (`download` type)
    * Adds the upload button near the download button (e.g. mp4 video)
    * Sends the direct media url with post url as referer
    * Same as the previous, doen't work with the extension

* Misskey
    * Adds the upload button to reactions row on each tweet
    * Works with the extension's address bar action, but each tweet has to be opened in new tab - which I am too lazy to do and just don't like

* Pixiv
    * Adds the upload button on post thumbnails
    * Extension's context menu action uploads only the first image in the set - which I don't like
    * Works with the extension's address bar action, but each post has to be opened in new tab - which I am too lazy to do and just don't like
