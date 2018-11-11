# Siri Shortcut Collection

Some of my daily used Siri shortcuts.
The table is inspired by [Ticky](https://github.com/ticky/siri-shortcuts/).

Many of these shortcuts are categorized into 5 categories, namely:
  - text actions
  - URL handling actions
  - web actions
  - download actions
  - image actions

Each category has an entry shortcut to run from the share sheet.


| Shortcut<br/> Name & XML | iCloud | Description | Category | Action Extension<sup><a href='#act-ext' name='^act-ext'>1</a></sup> | Widget | Depends On | Source |
| ------------------------ | :----: | ----------- | -------- | :-----------------------------------------------------------------: | :----: | ---------- | ------ |
| [**Debug Input**][dbg] | [Get][dbg-i] | Debugging inspect whatever input | - | YES | NO | - | - |
| [**Copy**][cp] | [Get][cp-i] | Copy whatever input | - | YES | NO | - | - |
| [**Backup/Restore**][bak] | [Get][bak-i] | Backup & Restore shortcuts | - | NO | NO | - | [@brentacPrime][bak-src] |
| [**Trim Screenshot**][trim] | [Get][trim-i] | Call `f.i. Trim Screenshot` to trim the most current screenshot | `image` | NO | YES | <ul><li>[x] f.i. Trim Screenshot</li></ul> | - |
| [**Run Clipboard**][clip] | [Get][clip-i] | Fetch whatever on the clipboard and launch the share sheet | - | YES<br/><sup>(but use clipboard content instead)</sup> | YES | - | - |
| [**MRT Time**][mrt] | [Get][mrt-i] | Given Taipei Metro station ID and direction, report current time table | - | NO | YES | <ul><li>[x] f. Choose from Dictionary List</li></ul> | - |
| [**Safari Viewer**][sf] | [Get][sf-i] | Open URLs in an in-app WKWebView | `url` | YES | NO | - | - |
| [**Get Map Address**][addr] | [Get][addr-i] | Get address from contacts, Apple/Google Maps venues | `contacts` | YES | NO | - | - |
| [**f. Filter List**][f-fltr] | [Get][f-fltr-i] | Given list `[e, e, ...]` and regex `r`, output `[e if r.match(e), ...]` | - | NO | NO | - | - |
| [**f. Hex to Dec**][f-0x] | [Get][f-0x-i] | Given hex number, output decimal | - | NO | NO | - | - |
| [**f. Choose from Dictionary List**][f-cdl] | [Get][f-cdl-i] | Given a1 (`[dict, dict, ...]`), a2 (key), a3 (value criteria), output `dict` by chooseing from `dict[a2]` or output the first `dict` if `dict[a2] ~ a3` | - | NO | NO | - | - |
| [**f. 2. Call Function**][f-fn] | [Get][f-fn-i] | Given shortcut and arglist, pass arglist all-at-once (if `m.` in shortcut name) or 1-by-1 (otherwise) to the shortcut | - | NO | NO | - | - |
| [**f. 3. Select Function.shortcut**][f-selfn] | [Get][f-selfn-i] | Given category, prefix, and usage message, display functions of the prefix for choosing | - | NO | NO | - | - |
| [**f.i. Trim Screenshot**][fi-trim] | [Get][fi-trim-i] | Trim out the status bar from a screenshot | `image` | Auto | NO | - | - |

<a href='#^act-ext'>^</a><a name='act-ext'>1</a> __Action Extension:__ Accepts files, URLs or other data from another app's share sheet.


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
[fi-trim]: <xml/f.i.%20Trim%20Screenshot.shortcut>
[fi-trim-i]: <https://www.icloud.com/shortcuts/5b7b4bdff09745e7b2dcebf57b42c678>
