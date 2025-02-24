pfsense-wg-restart

Restart pfSense WireGuard service on WAN IP change.
Background

This patch restarts the WireGuard service after the package reload in rc.newwanip. I created it to fix an issue I was having with pfSense and gateway groups where it didn't go back to the tier 1 gateway on recovery. Feel free to use it if you're having the same problem but you're on your own if you have issues.

Installation

    Install the System Patches package in pfSense if you haven't already.
    Go to System > Patches
    Click the green Add New Patch button near the top
    Enter whatever you want in Description
    Either paste the github URL for wg_restart.patch in the URL box or copy the contents of the file into the Patch Contents box
    Set Path Strip Count to 2
    Leave Base Directory as /
    Uncheck Ignore Whitespace
    Check Auto Apply if you want
    Click Save
    Click Apply to the right of the patch description
