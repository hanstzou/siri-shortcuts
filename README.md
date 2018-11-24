# Siri Shortcut Collection

Here collects some of my frequently used Siri shortcuts.
The table is inspired by [Ticky](https://github.com/ticky/siri-shortcuts/).

Many of these shortcuts are categorized into 6 categories, namely:
  - text actions
  - query (and open in WebView)
  - URL handling actions
  - web actions
  - download actions
  - image actions

Each category has an entry shortcut to run from the share sheet.


| Shortcut<br/> Name & XML | iCloud | Depends On | Description | Category | Action Extension<sup><a href='#act-ext' name='^act-ext'>1</a></sup> | Widget | Source |
| ------------------------ | :----: | ---------- | ----------- | -------- | :-----------------------------------------------------------------: | :----: | ------ |
| [**Debug Input**][dbg] | [Get][dbg-i] | - | Debugging inspect whatever input | - | YES | NO | - |
| [**Copy**][cp] | [Get][cp-i] | - | Copy whatever input | - | YES | NO | - |
| [**Backup/Restore**][bak] | [Get][bak-i] | - | Backup & Restore shortcuts | - | NO | NO | [@brentacPrime][bak-src] |
| [**Trim Screenshot**][trim] | [Get][trim-i] | <ul><li>[x] f.i. Trim Screenshot</li></ul> | Call `f.i. Trim Screenshot` to trim the most current screenshot | `image` | NO | YES | - |
| [**Run Clipboard**][clip] | [Get][clip-i] | - | Fetch whatever on the clipboard and launch the share sheet | - | YES<br/><sup>(but use clipboard content instead)</sup> | YES | - |
| [**MRT Time**][mrt] | [Get][mrt-i] | <ul><li>[x] f. Choose from Dictionary List</li></ul> | Given Taipei Metro station ID and direction, report current time table | - | NO | YES | - |
| [**Safari Viewer**][sf] | [Get][sf-i] | - | Open URLs in an in-app WKWebView | `url` | YES | NO | - |
| [**Get Map Address**][addr] | [Get][addr-i] | - | Get address from contacts, Apple/Google Maps venues | `contacts` | YES | NO | - |
| [**f. Filter List**][f-fltr] | [Get][f-fltr-i] | - | Given list `[e, e, ...]` and regex `r`, output `[e if r.match(e), ...]` | - | NO | NO | - |
| [**f. Hex to Dec**][f-0x] | [Get][f-0x-i] | - | Given hex number, output decimal | - | NO | NO | - |
| [**f. Choose from Dictionary List**][f-cdl] | [Get][f-cdl-i] | - | Given a1 (`[dict, dict, ...]`), a2 (key), a3 (value criteria), output `dict` by chooseing from `dict[a2]` or output the first `dict` if `dict[a2] ~ a3` | - | NO | NO | - |
| [**f. 2. Call Function**][f-fn] | [Get][f-fn-i] | - | Given shortcut and arglist, pass arglist all-at-once (if `m.` in shortcut name) or 1-by-1 (otherwise) to the shortcut | - | NO | NO | - |
| [**f. 3. Select Function**][f-selfn] | [Get][f-selfn-i] | - | Given category, prefix, and usage message, display functions of the prefix for choosing | - | NO | NO | - |
| [**Text Actions**][txt] | [Get][txt-i] | <ul><li>[x] f. 2. Call Function</li><li>[x] f. 3. Select Function</li></ul> | Call `f.t.` functions on input text | `text` | YES | NO | - |
| [**f.t. Suggest**][ft-sug] | [Get][ft-sug-i] | - | Send input text to Google for suggestions | `text` | Indirect | NO | - |
| [**f.t. Look Up**][ft-lkup] | [Get][ft-lkup-i] | <ul><li>[x] p.t. Strip</li><li>[x] p.t. Remove Links</li></ul>| Look up input text in system dictionaries (not very useful) | `text` | Indirect | NO | - |
| [**f.t. PTT IV**][ft-pttiv] | [Get][ft-pttiv-i] | <ul><li>[x] p.t. PTT IV</li><li>[x] f.u. Bit.ly :key:</li></ul>| Transform PTT Alertor messages into Telegram IV in markdown format | `text` | Indirect | NO | - |
| [**f.t. Speak**][ft-spk] | [Get][ft-spk-i] | <ul><li>[x] p.t. Remove Links</li></ul> | Read out input text | `text` | Indirect | NO | - |
| [**p.t. PTT IV**][pt-pttiv] | [Get][pt-pttiv-i] | - | Append PTT url to IV handler | `text` | Support | NO | - |
| [**p.t. Remove Links**][pt-rmln] | [Get][pt-rmln-i] | - | Remove URLs from input text | `text` | Support | NO | - |
| [**p.t. Strip**][pt-strip] | [Get][pt-strip-i] | - | Strip beginning/ending whitespaces | `text` | Support | NO | - |
| [**URL Handling**][url] | [Get][url-i] | <ul><li>[x] f. Filter List</li><li>[x] f. 2. Call Function</li><li>[x] f. 3. Select Function</li></ul> | Call `f.u.` on input URLs to generate new ones | `url` | YES | NO | - |
| [**f.u. Expand URL**][fu-exp] | [Get][fu-exp-i] | - | Try to expand input URL (e.g. bit.ly) | `url` | Indirect | NO | - |
| [**f.u. Decode URL**][fu-dec] | [Get][fu-dec-i] | - | Decode (percent-encoded) input URL | `url` | Indirect | NO | - |
| [**f.u. Bit.ly :key:**][fu-bit] | [Get][fu-bit-i] | - | Shorten input URL with bit.ly <sup>(:warning: Never share this Shortcut with your OAuth token information inside. Remove the token before sharing. Generate your OAuth token [here][bitly-oauth].)</sup> | `url` | Indirect | NO | - |
| [**f.u. Sanitize URL**][fu-san] | [Get][fu-san-i] | <ul><li>[x] p.u.d. Remove UTM-Alike</li></ul> | Clean up input URL by calling all `p.u.` functions | `url` | Indirect | NO | - |
| [**p.u. BBC**][pu-bbc] | [Get][pu-bbc-i] | <ul><li>[x] f.u. Expand URL</li><li>[x] p.u.d. Ensure ?#</li></ul> | Given BBC Zhongwen Simplified URLs, output Zhongwen Traditional version | `url` | Support | NO | - |
| [**p.u.d. Remove UTM-Alike**][pud-noutm] | [Get][pud-noutm-i] | - | Remove tracking queries | `url` | Support Devisions | NO | - |
| [**p.u.d. Ensure ?#**][pud-ensq] | [Get][pud-ensq-i] | - | Ensure URL queries and fragments | `url` | Support Devisions | NO | - |
| [**Web Actions**][web] | [Get][web-i] | <ul><li>[x] f. 2. Call Function</li><li>[x] f. 3. Select Function</li></ul> | Call `f.w` functions on input webpage | `web` | YES | NO | - |
| [**f.w. f.u. Get HTML**][fwfu-htm] | [Get][fwfu-htm-i] | - | Output HTML of a Web page or an URL | `web`</br>`url` | Indirect | NO | - |
| [**p.w. Get IG URL**][pw-ig] | [Get][pw-ig-i] | - | Extract URLs from IG JSON node | `web`<br/>`download` | Support | NO | - |
| [**Download Actions**][dl] | [Get][dl-i] | <ul><li>[x] f. 2. Call Function</li><li>[x] f. 3. Select Function</li></ul> | Call `f.d.` on input URLs to download certain contents | `download` | YES | NO | - |
| [**f.d. App Images**][fd-aimg] | [Get][fd-aimg-i] | - | Given an App's iTunes URL, download its screenshot images | `download` | Indirect | NO | - |
| [**f.w. f.d. Get IG Media**][fwfd-igm] | [Get][fwfd-igm-i] | <ul><li>[x] p.w. Get IG URL</li></ul> | Given IG URLs/Web pages, download media contents | `web`<br/>`download` | NO | NO | - |
| [**Image Actions**][img] | [Get][img-i] | <ul><li>[x] f. 2. Call Function</li><li>[x] f. 3. Select Function</li></ul> | Call `f.i.` functions on input images | `image` | YES | NO | - |
| [**f.i. Trim Screenshot**][fi-trim] | [Get][fi-trim-i] | - | Trim out the status bar from a screenshot | `image` | Indirect | NO | - |
| [**f.i.m. Glue Screenshots**][fim-glue] | [Get][fim-glue-i] | - | Combine multiple screenshots from left to right | `image` | Indirect | NO | - |
| [**f.i. Imgur**][fi-imgur] | [Get][fi-imgur-i] | - | Upload photo to imgur <br/><sup>(:warning: Need an one-time setup for Imgur in Shortcut app)</sup> | `image` | Indirect | NO | - |
| [**f.i. Photo Map Thumbnail v2**][fi-imgmap] | [Get][fi-imgmap-i] | - | Add a coordinate map to a photo | `image` | Indirect | NO | [Reddit @atomicsiren][fi-imgmap-src] <br/><sup>(Modified to integrate into Image Actions)</sup> |

<a href='#^act-ext'>^</a><a name='act-ext'>1</a> __Action Extension:__ Accepts files, URLs or other data from another app's share sheet. <br/>
Indirect means a shortcut will be called by a category entry.<br/>
Support means a short will be called by Indirect shortcuts as a supportive tool.


[bak]: <xml/Backup%3ARestore.shortcut>
[bak-i]: <https://www.icloud.com/shortcuts/ee2fa9e163be4704b061193c444cd124>
[bak-src]: <http://www.brentac.com/blog/2017/3/25/backup-and-restore-your-workflows>
[cp]: <xml/Copy.shortcut>
[cp-i]: <https://www.icloud.com/shortcuts/d12ada588c8c4a428d647f03b3b73277>
[dbg]: <xml/Debug%20Input.shortcut>
[dbg-i]: <https://www.icloud.com/shortcuts/771e4d44f2574d50883e448b96bbba8e>
[trim]: <xml/Trim%20Screenshot.shortcut>
[trim-i]: <https://www.icloud.com/shortcuts/c16437ac859740f3afdb0d197c550667>
[clip]: <xml/Run%20Clipboard.shortcut>
[clip-i]: <https://www.icloud.com/shortcuts/dc005d02c9024647b47d720369b4adcb>
[mrt]: <xml/MRT%20Time.shortcut>
[mrt-i]: <https://www.icloud.com/shortcuts/54cbc09a110947de92231449d2c19792>
[sf]: <xml/Safari%20Viewer.shortcut>
[sf-i]: <https://www.icloud.com/shortcuts/90b0e685b75447ee87ebb4efce87bc88>
[addr]: <xml/Get%20Map%20Address.shortcut>
[addr-i]: <https://www.icloud.com/shortcuts/ee24a5d1362d4fd09fd98de3372b4247>
[f-fltr]: <xml/f.%20Filter%20List.shortcut>
[f-fltr-i]: <https://www.icloud.com/shortcuts/8feb5eb12d02406093d9aaecc4dc3d4d>
[f-0x]: <xml/f.%20Hex%20to%20Dec.shortcut>
[f-0x-i]: <https://www.icloud.com/shortcuts/7ef23c6f8f1d4d56a2d9d61572db2305>
[f-cdl]: <xml/f.%20Choose%20from%20Dictionary%20List.shortcut>
[f-cdl-i]: <https://www.icloud.com/shortcuts/337bb10070994f789afbc22b9b1ca668>
[f-fn]: <xml/f.%202.%20Call%20Function.shortcut>
[f-fn-i]: <https://www.icloud.com/shortcuts/f5b310f99c4a4f2e99440a405b8d97ca>
[f-selfn]: <xml/f.%203.%20Select%20Function.shortcut>
[f-selfn-i]: <https://www.icloud.com/shortcuts/6a3dbb4c49504839942d6a40a9637786>
[txt]: <xml/Text%20Actions.shortcut>
[txt-i]: <https://www.icloud.com/shortcuts/e757c73cdbc84fa1a1a6a32b7e3467a2>
[ft-sug]: <xml/f.t.%20Suggest.shortcut>
[ft-sug-i]: <https://www.icloud.com/shortcuts/ab646250c4c44943b854129917a079da>
[ft-lkup]: <xml/f.t.%20Look%20Up.shortcut>
[ft-lkup-i]: <https://www.icloud.com/shortcuts/1e51b73e47734e0d9a101d77ebbb1dd7>
[ft-pttiv]: <xml/f.t.%20PTT%20IV.shortcut>
[ft-pttiv-i]: <https://www.icloud.com/shortcuts/92f6c5fc8b5b48aeba690e9d99ddfd3b>
[ft-spk]: <xml/f.t.%20Speak.shortcut>
[ft-spk-i]: <https://www.icloud.com/shortcuts/3bdf1da1f690458684e0c5136d17adbe>
[pt-pttiv]: <xml/p.t.%20PTT%20IV.shortcut>
[pt-pttiv-i]: <https://www.icloud.com/shortcuts/b866fbaaac134c8187528770ad56b4d1>
[pt-rmln]: <xml/p.t.%20Remove%20Links.shortcut>
[pt-rmln-i]: <https://www.icloud.com/shortcuts/1ca1e52743f243749ee96ac7668eb77b>
[pt-strip]: <xml/p.t.%20Strip.shortcut>
[pt-strip-i]: <https://www.icloud.com/shortcuts/5eaca52aa3304b06a4cd05b5ea3fed58>
[url]: <xml/URL%20Handling.shortcut>
[url-i]: <https://www.icloud.com/shortcuts/2534eae229b94b0fbe409df8d3683e45>
[fu-exp]: <xml/f.u.%20Expand%20URL.shortcut>
[fu-exp-i]: <https://www.icloud.com/shortcuts/303b66d2cd624fe8a0fff1dd0a96d22d>
[fu-dec]: <xml/f.u.%20Decode%20URL.shortcut>
[fu-dec-i]: <https://www.icloud.com/shortcuts/315acfdd64134385aa41bc2cc67645f0>
[fu-bit]: <xml/f.u.%20Bit.ly%20%F0%9F%94%91.shortcut>
[fu-bit-i]: <https://www.icloud.com/shortcuts/a64622a8f4694b21955490fd3c052c7d>
[bitly-oauth]: <https://app.bitly.com/performance/?actions=accountMain&actions=settings&actions=advancedSettings>
[fu-san]: <xml/f.u.%20Sanitize%20URL.shortcut>
[fu-san-i]: <https://www.icloud.com/shortcuts/3f72a36967044af39a220daeeb497253>
[pu-bbc]:<xml/p.u.%20BBC.shortcut>
[pu-bbc-i]: <https://www.icloud.com/shortcuts/69ad9de923964fab936d81964fc8cd4c>
[pud-noutm]: <xml/p.u.d.%20Remove%20UTM-Alike.shortcut>
[pud-noutm-i]: <https://www.icloud.com/shortcuts/d2b72d4725e0494f9bd352b5ea02b32d>
[pud-ensq]: <xml/p.u.d.%20Ensure%20%3F%23.shortcut>
[pud-ensq-i]: <https://www.icloud.com/shortcuts/23d293aab2c6417eb8a54a94ac515a2f>
[web]: <xml/Web%20Actions.shortcut>
[web-i]: <https://www.icloud.com/shortcuts/cff2a6f1a9f14c4691ded49d418f5e17>
[fwfu-htm]: <xml/f.w.%20f.u.%20Get%20HTML.shortcut>
[fwfu-htm-i]: <https://www.icloud.com/shortcuts/14faa19d7cff44968887cfb1c36c3a72>
[pw-ig]: <xml/p.w.%20Get%20IG%20URL.shortcut>
[pw-ig-i]: <https://www.icloud.com/shortcuts/ec2c9dae558844f0a4766d7d7d69f660>
[dl]: <xml/Download%20Actions.shortcut>
[dl-i]: <https://www.icloud.com/shortcuts/3f624d9ca1db40b9a19623559760f4cd>
[fd-aimg]: <xml/f.d.%20App%20Images.shortcut>
[fd-aimg-i]: <https://www.icloud.com/shortcuts/f2686716696e4f1fa299c719ea416fa1>
[fwfd-igm]: <xml/f.w.%20f.d.%20Get%20IG%20Media.shortcut>
[fwfd-igm-i]: <https://www.icloud.com/shortcuts/8ec71bfb74674194a116fb22c34e46eb>
[img]: <xml/Image%20Actions.shortcut>
[img-i]: <https://www.icloud.com/shortcuts/53e178455baf4e03b9c573a5f2b0850f>
[fi-trim]: <xml/f.i.%20Trim%20Screenshot.shortcut>
[fi-trim-i]: <https://www.icloud.com/shortcuts/5b7b4bdff09745e7b2dcebf57b42c678>
[fim-glue]: <xml/f.i.m.%20Glue%20Screenshots.shortcut>
[fim-glue-i]: <https://www.icloud.com/shortcuts/f29b93a9c638477b9859c7cfd857fdb9>
[fi-imgur]: <xml/f.i.%20Imgur.shortcut>
[fi-imgur-i]: <https://www.icloud.com/shortcuts/b9a28aab4a854b29bbf63c11d5813d01>
[fi-imgmap]: <xml/f.i.%20Photo%20Map%20Thumbnail%20v2.shortcut>
[fi-imgmap-i]: <https://www.icloud.com/shortcuts/38e72001cb7142339ccb2e2a5d86640a>
[fi-imgmap-src]: <https://reddit.com/r/shortcuts/comments/9qyh6y/add_thumbnail_map_to_photo/>
