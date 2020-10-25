---
title: ConPTY Bypass
layout: titled
---

> This is only relevant when `terminalpp` is used to access Windows Subsystem for Linux (WSL) on Windows. 

With recent versions of Windows 10, the [ConPTY](https://devblogs.microsoft.com/commandline/windows-command-line-introducing-the-windows-pseudo-console-conpty/) has greatly simplified creation of terminal emulators. However, to be compatible with existing Win32 applications, the ConPTY must take a rather complex route to allow escape sequences to be read and written to the terminal as these must be translated to and from Win32 APIs. 

While this makes ConPTY work with both applications using either escape sequences, or Win32 console API calls, for applications outputing escape sequences directly, ConPTY has two major disadvantages:

1. the Win32 API translation takes some time and often is the bottleneck of the terminal's responsiveness

2. perhaps more importantly, an application can only use the escape sequences understood by the translation layer - a reason why very few Windows terminals actually support mouse. 

### `tpp-bypass`

[`tpp-bypass`](https://github.com/terminalpp/terminalpp/tree/master/tpp-bypass) is a small Linux program which opens a Linux pseudoterminal to a specified Linux command and then translates that terminal's input, output and events into a standard in and out streams. 

`terminalpp` can directly execute the bypass and decode the input, output and events without the need for ConPTY. This both increases the speed of `terminalpp` and more importantly allows it to support *any* escape sequence, regardless of its support in ConPTY. 

To make `terminalpp` use the bypass, first the `session.pty` option must be set to `"bypass"` and then the command must execute first the bypass itself, and then the actual process, such as:

    wsl.exe -- ~/.local/bin/tpp-bypass -e bash

(where first the WSL is instructed to execute the bypass, which is then instructed to execute the `bash` shell)

> The bypass can only be used with WSL sessions and cannot work with `cmd.exe`, or powershell.
