---
title: Clipboard
layout: titled
---

On Linux `terminalpp` supports the default behavior for both clipboard and selection buffers, including the paste of selection buffer with middle mouse button. This functionality is emulated within `terminalpp` windows on other platform as well, i.e. while the selection buffer does not work across applications, it works inside `terminalpp` window itself. 

To select text, hold down mouse button and select the area. To copy, press the right mouse button. To paste clipboard into the terminal, press `C-S-v`. 

### Paste Confirmation

A well known vulnerability of terminal applications is the possibility that malicious website can inject invisible text when contents is copied from them (as discussed [here](https://thejh.net/misc/website-terminal-copy-paste)).

Note that this is problem even with bracketed paste mode and the only proper way to mitigate such attacks is to preview the pasted contents. To this end `terminalpp` supports paste confirmation, in which the text to be pasted is previewed first in its entirety so that you can inspect if there are any unwanted characters. 

![Paste Confirmation Screenshot](/resources/screenshots/paste-confirmation.png){: .mx-auto .d-block }

The [configuration](/features/configuration.html) option for this is the `session.confirmPaste`, which can take the following values:

- `"never"` which means that the confirmation dialog will never be displayed
- `"always"` which means that any paste into the terminal window must be confirmed by the user
- `"multiline"` meaning that only when multi-line text is being pasted, its confirmation is required. The rationale behind this option is that if there are no line ending characters in the text, then there will be time to inspect the text itself in the terminal before submitting it for possible execution. This is the default option. 


When the confirmation dialog appears, pressing the paste shortcut (`C-S-v`) again performs the paste, while pressing `Esc` cancells the operation. 