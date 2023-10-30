# upload-to-danbooru.user.js

(Another) userscript for uploading to Danbooru.

## Installation

* Install [Tampermonkey](https://tampermonkey.net/) extension, it's available for Firefox, Safari and Chromium-based browsers.
* Download the [script](https://github.com/hdk5/upload-to-danbooru.user.js/raw/master/upload-to-danbooru.user.js).
* An installation prompt will appear. Accept the installation.

_The userscript is confirmed to work only on latest Firefox + latest Tampermonkey. Other browsers and userscript managers are not tested._

## Why not use the official extension?

The userscript is intended to be used along with - not insted of - the [browser extension](https://github.com/danbooru/upload-to-danbooru/).

Unlike the extension, which aims to be lightweight and universal, this one does the opposite by supporting only very few sites and including specific hacks for them.

## Supported sites

* Pixiv
    * Adds the upload button on post thumbnails
    * Extension's context menu action uploads only the first image in the set
    * Works with the extension's address bar action, but each post has to be opened in new tab

* Twitter
    * Adds the upload button near bookmark button on each tweet
    * Works with the extension's address bar action, but each tweet has to be opened in new tab

* Nijie
    * Adds the upload button on post thumbnails
    * Extension's context menu action uploads only the first image in the set
    * Works with the extension's address bar action, but each post has to be opened in new tab

* Fantia
    * `post_content_photo` type
        * Adds the upload button to full-size image page
        * Sends the direct image url with post url as referer
        * Currently _almost_ works with the extension, but danbooru doesn't recognize the referer (at the moment) - which I don't like.
        * The full-size image page still has to be opened manually

    * `album_image` type
        * Adds the upload button on the image in the article
        * Sends the direct image url with post url as referer
        * Doen't work (and [never will](https://github.com/danbooru/upload-to-danbooru/issues/8#issuecomment-1769268852)) with the extension

    * `download` type
        * Adds the upload button near the download button (e.g. mp4 video)
        * Sends the direct media url with post url as referer
        * Same as the previous, doen't work with the extension

* Misskey
    * Adds the upload button to reactions row on each tweet
    * Works with the extension's address bar action, but each tweet has to be opened in new tab
