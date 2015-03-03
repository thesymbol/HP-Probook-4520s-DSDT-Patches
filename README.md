HP Probook 4520s DSDT Patches
===============
This is a set of patches for the HP Probook 4520s for running OS X
Credit to RehabMan for almost all patches.
You can find RehabMans repository here: https://github.com/RehabMan/Laptop-DSDT-Patch

RehabMan recommend that you use his version of MaciASL for this type of patches: 
https://github.com/RehabMan/OS-X-MaciASL-patchmatic

How to add repository to MaciASL
-------------------------
To add these patches to MaciASL as a repository:
- Run MaciASL
- choose Preferences from the MaciASL menu bar
- select Sources
- click the [+] button
- give it a name (eg. "4520s Patches")
- type the following URL: https://raw.githubusercontent.com/thesymbol/HP-Probook-4520s-DSDT-Patches/master

If you don't have internet access and wish to use a repository locally:
- download the .ZIP of the repository from github (Download ZIP button on right side)
- copy the resulting .ZIP to the laptop (via USB), for example, to your Documents folder
- unzip it in place
- now add the path to the 'sources' in MaciASL Preferences, in the case of this repo, copied to Documents, the URL/path would be file:///Users/YourUserName/Documents/Laptop-DSDT-Patch-master

After that you can use the repo just like a remote repo.

How to apply patches with MaciASL
-------------------------
- run MaciASL
- if you already have a patched DSDT in /Extra, MaciASL will load it 
  (caption will say DSDT.AML)
- if you don't have a patched DSDT yet, caption will show "System DSDT"
- click Compile to verify you have an error free compile
  (only errors matter)
- if it has errors, you must fix them
- there are a few common error patches in the repo (first group)
- ok... back to how to apply a patch...
- click Patch (logical, right)
- select a patch from the repo that appears on the left
- MaciASL will show you a preview of the changes
- click Apply
- when you're done applying patches, click Close

To use your DSDT, you must save it to /Extra/DSDT.aml (or /EFI/CLOVER/ACPI/patched/DSDT.aml if you are using Clover), format: ACPI Machine Language Binary
After saving it, reboot and test. Boot with DSDT=null if there is an issue with your DSDT that prevents you from booting.
