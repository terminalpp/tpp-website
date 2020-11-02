---
title: Remote Files
layout: titled
---

When working in a terminal it is often useful to view non-text based files, such as generated images or pdfs. If the session is local, this may not a problem using the default app viewers for the given file. If the session happens on a remote server, this is not possible. 

`terminalpp` introduces special escape sequences that allows it to send any file through the existing connection to the machine that runs the terminal where it is stored in temporary files and can then be viewed by local applications. To use this feature, [`ropen`](https://github.com/terminalpp/terminalpp/tree/master/ropen), the program responsible for sending the file to the terminal, must be installed on the remote server.

<!-- TODO add a video of the feature in action here -->

### Installation

`deb` and `rpm` packages are provided on the [release](https://github.com/terminalpp/terminalpp/releases/latest) page as well as a [snap application](https://snapcraft.io/ropen).

To install `ropen` via snap, simply execute the following:

    sudo snap install ropen --edge --classic

### Usage

To open a remote file, simply type `ropen` followed by a path to the file, such as:

    ropen some_document.pdf

<div class="alert alert-warning">
    Note that the remote opening works only one way and is useful for viewing the remote files locally only. While the remotely opened files can be edited, those changes will not be propagated to the remote.
</div>

If file of same name (relative path on the remote host from the `ropen` command) is downloaded multiple times, the old versions are automatically overwriten if possible, and if opened in viewer that supports refreshes, the file will refresh.  

<!-- TODO another video of the update -->

<div class="alert alert-success">
    Opening remote files works across <code>ssh</code> or even <code>tmux</code> (of course you cannot change sessions or screens during the transfer). 
</div>


### Settings

Remote files are by default stored in a temporary directory, but the [configuration](/features/configuration.html) file may overwrite their location to any existing directory in the `remoteFiles.dir` option.

This has the advantage of having all the remotely opened files easily accessible from the local machine by other programs as well.

