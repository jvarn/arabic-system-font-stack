# arabic-system-font-stack
CSS font stack for Arabic system fonts

## Serif


| System Font                        | OS                                          |
|------------------------------------|---------------------------------------------|
| Geeza Pro                          | iOS Safari, macOS Safari, macOS Firefox     |
| Noto Naskh Arabic                  | Gnome, KDE                                  |
| Droid Serif                        | Android, Chrome OS                          |
| Times New Roman                    | Windows                                     |
| sans-serif                         | Fallback                                    |

## Sans-serif

| System Font                        | OS                                          |
|------------------------------------|---------------------------------------------|
| -apple-system                      | iOS Safari, macOS Safari, macOS Firefox     |
| system-ui                          | macOS Chrome, Windows Chrome (new versions) |
| BlinkMacSystemFont                 | macOS Chrome                                |
| Dubai                              | Windows 10 and newer                        |
| Segoe UI                           | Windows Vista and newer                     |
| Tahoma                             | Windows XP and newer                        |
| Noto Sans Arabic UI                | Android, Chrome OS                          |
| Dejavu Sans                        | Gnome, KDE                                  |
| Arial                              | All                                         |
| sans-serif                         | Fallback                                    |

## Discussion
### Mac OS

#### -apple-system, BlinkMacSystemFont

The former vendor prefix works in Safari on Mac OS and iOS, while the latter works on Chrome on Mac OS and iOS. On newer versions of Mac OS, they are an alias for the San Francisco sans-serif typeface, which is used throughout the OS interface and has a consistent look in Arabic and English. On older Mac OS X versions they are an alias for Helvetica Neue or Lucida Grande.

#### system-ui

system-ui should be sufficient without -apple-system and BlinkMacSystemFont, but I’ve kept them for backwards compatibility.

If you wish to remove them, then the following order is currently used by Bootstrap:

`system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", "Liberation Sans", sans-serif`

We can modify this for Arabic as follows:

`system-ui, -apple-system, Dubai, "Segoe UI", Tahoma, "Noto Sans Arabic UI", "Dejavu Sans", Arial, sans-serif`
