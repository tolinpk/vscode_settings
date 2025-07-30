## Keybindings file in vscode
Here is how you add the keybindings:

Open VS Code.
```sh
Press Ctrl+Shift+P (or Cmd+Shift+P on macOS) to open the Command Palette.

Type and select Preferences: Open Keyboard Shortcuts (JSON). This opens the keybindings.json file where user-defined shortcuts are stored.

Paste the keybindings inside the array, or add them if the file is not empty
```

## Settings file in vscode
How to add these settings in VS Code
Open User Settings (JSON):
```shz
Press ```Ctrl+Shift+P``` (or Cmd+Shift+P on macOS) to open the Command Palette.

Type Preferences: ```Open Settings (JSON)``` and select it.

This opens your ```settings.json``` where you can paste the above configuration or add parts of it.

Ensure VS Code Vim Extension is installed if you want the Vim keybindings to work:

Go to Extensions ```(Ctrl+Shift+X),``` search for vscodevim.vim, and install it.

Paste the config into ```settings.json```.

You may want to merge with your existing settings carefully to avoid duplicates or conflicts.

For the custom Vim keybindings arrays ```(vim.normalModeKeyBindingsNonRecursive, vim.visualModeKeyBindings),``` place them under the root level in the JSON file (as in your snippet).

```Save the file;``` changes should take effect immediately.
```

This comprehensive JSON config controls editor appearance, behavior, and Vim keybindings in your VS Code environment through one place: your settings.json.


### Mac cursor continuous movement solution:
```sh 
defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false
```
What does it mean?
On macOS, by default, when you press and hold certain keys (like letters), it triggers the "press and hold" feature that shows a popup menu for accented characters (like holding e shows options for é, è, etc.).

Disabling this with ```ApplePressAndHoldEnabled -bool fals```e means that pressing and holding a key will enable the key to repeat continuously, as is common in most text editors and terminals (like holding down arrow keys to move the cursor continuously).

Applying this setting only for ```com.microsoft.VSCode``` (the VS Code app bundle identifier) means the change only affects VS Code, allowing continuous key repeats when holding keys, which is essential for smooth cursor movement especially when using vim-style navigation keys (h, j, k, l).
