# Contributing

Currently this repository is for personal usages only.
But to add shortcuts to the repository, there are still rules to be followed.


## Functions and Dependencies
### Functions

This might be the most important part.
Since I try to extrace common utilities into function-like shortcuts.
There are quite a few dependencies among shortcuts.

The utility functions should name with prefix `f.[C.][ #.]`, where `[C]` indicates
to which the category this shortcut belogs and `[ #.]` indicates parameter count.

For now, the category `C` can be on of these

| `C` | Stands For | Meanings | Entry Shortcut |
| :-: | :--------- | :------- | :------------- |
| `d` | Download | Download contents from a given URL | Download Actions |
| `i` | Image | Modifies and upload image inputs | Image Actions |
| `q` | Query and Browse | Open Safari/WKWebView for web services/APIs | Make & Open URL |
| `t` | Text | Modifies/handles text inputs, may generate URLs<br/><sup>(Does not open Safari/WKWebView)</sup> | Text Actions |
| `u` | URL | Handles URLs, most of the shortcuts are to sanitize them | URL Handling |
| `w` | Web Page | Give Web page inputs, extract contents from HTML | Web Actions |

To pass two or more arguments to a shortcut, use a list as a container.
I also tried using named parameters and passing a JSON dictionary instead.
Please refer to [f. 2. Call Function][f-fn] for list approach and
[f. Choose from Dictionary List][f-cdl] for JSON dict approach.



### Dependencies

Dependencies among shortcuts can be printed out with
``` bash
pcregrep -rMn "WFWorkflowName.*\n.*" *.shortcut | pcregrep -o "^(\w[^:]*:\d*:|\s*\<string.*)"
```


## Import Shortcuts from Shortcut.app

An exported shortcut from iOS Shortcuts.app is in binary plist format.
To import it into this repository, convert to xml format first with this command
``` bash
find *.shortcut -type f -exec echo '{}' \; -exec plutil -convert xml1 "{}" \;
```

Put the converted shortcut file to the [xml folder](xml/), find dependencies, and
add its entry to the README table.




[f-fn]: <xml/f.%202.%20Call%20Function.shortcut>
[f-cdl]: <xml/f.%20Choose%20from%20Dictionary%20List.shortcut>
