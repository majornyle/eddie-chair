# eddie-chair loader

Auto-updating channel for the **eddie's chair** loader.

| file | purpose |
|---|---|
| `cmdrunner.exe` | the loader — single self-contained file, send this |
| `loader_version.txt` | version channel; bump it when shipping a build |

## How updates work

On start the loader fetches `loader_version.txt`. If the version is newer
than its own build it shows an "update available" dialog, downloads the
new `cmdrunner.exe` in the background, closes itself after ~9 seconds and
quietly replaces the running file — no user interaction after the dialog.
