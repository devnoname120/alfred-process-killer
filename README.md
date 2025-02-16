# Description
Kill Process is an Alfred 5 workflow that makes it easy to kill misbehaving processes. It is, in essence, a way to easily find processes by name and kill them using `kill -SIGKILL`.

# Features
* Autocompletes process names
* Supports argument filtering (`process:arg`)
* Learns and prioritizes processes you kill frequently
* Shows icons when possible
* Shows CPU usage
* Shows process paths
* Ignores case
* Kills all processes with matching names on <kbd>cmd</kbd>+<kbd>return</kbd>
* Auto-update mechanism

![screenshot: `kill it`](screenshot1.png)
![screenshot: `kill chr:type=pp`](screenshot2.png)

# Usage
1. Type `kill` or `killall` into Alfred followed by a space.
2. Begin typing the name of the process you want to kill.
3. When you see the process you want to kill, select it from the list as usual.
4. Press <kbd>return</kbd> to kill the selected process (or all the processes if invoked with `killall`).  
Alternatively, press <kbd>cmd</kbd>+<kbd>return</kbd> to kill all processes with the same name as the selected one.

To filter by argument, add a colon and the argument you want to target (or a snippet of it) after your processes name (see the [second screenshot](screenshot2.png)).

# Installation
Download the [latest version](https://github.com/devnoname120/alfred-process-killer/releaes/latest). Open `Kill Process.alfredworkflow` and Alfred will walk you through the installation process. No configuration is necessary.

# Making Changes
## Editing the Script
The ruby script that powers Kill Process is `script.rb`. For testing, add a value for `theQuery` in the first line. Be sure that the subsequent `theQuery = "{query}"` is commented out. This allows you to hard-code a search query instead of taking what the user has typed from Alfred. See the comments in the script for more info.

## Applying Changes to the Workflow
1. Be sure that the first line in the script setting `theQuery` is commented out and that the second line (`theQuery = "{query}"`) is not commented out.
2. Open the Workflows tab of Alfred's Preferences.
3. Right-click on the Kill Process workflow on the left.
4. Click on 'Open in Finder'.
5. Replace the Ruby script with the new one.
6. Right-click again on the Kill Process workflows on the left.
7. Click on 'Export...'.
8. Adjust the version and the other metadata and then click on 'Export'.

# License
[WTFPL](http://www.wtfpl.net/about/), of course.
