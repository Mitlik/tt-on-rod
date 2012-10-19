About
=====
This project is to reimplement my MUD scripts so they aren't so embarrassing to
share with friends. With that in mind I need to give some credits. At some
point during the 1.x releases of Tintin++ I was referencing the scripts from
the [website]<http://tintin.sourceforge.net/scripts/> that Scandum has made
public domain. My own work is available under the
[WTFPL]<http://sam.zoy.org/wtfpl/COPYING>.

Notes
=====
*   The "Logs" directory will need to exist in order for various logging
    functions to write correctly. So the directory will be under version
    control, so git clone can pull it.  

*   **BEWARE** older releases do not have Utilities/worlds.dat in .gitignore
    and it is possible to commit it with sensitive data.

Getting Started
===============
The simplest way to get started while documentation is back burner to
functionality is to head into the project directory and run:

    grep -r "ALIAS" . && grep -r "FUNCTION" .

Project Structure
=================
The basic layout should be something like:
    +-PROJECT_HOME: the head project directory
      +-Characters: where character specific files go
      +-Logs: this is the default folders should write logs to
      +-Modules: where RoD specific scripts are stored
      +-Utilities: where generic scripts are stored (i.e. scripts that only deal with Tintin)
      +-main.tin: this one file should read in everything you need in #gts and to load up your characters
      +-modules.conf: this turns modules on and off, and may define variables for those modules

Types of files:
     .tin | Contain aliases, functions, actions, etc.
     .dat | Contain only data for use in another script (e.g. character listing or equipment damage listing)
    .conf | Setup variables that a user might change

Road Map
========
Subject to change. Part of sharing is hoping that another mind can come up with
some neat ideas to include.

Version 1
---------
Milestone goal: Help make tintin easier to use for logging in and offer some neat features
[X] Simplified connect with stored character data
[ ] Simple speed walk with storage: check vs built-in speedwalk
[ ] Basic MSDP
[ ] Basic battle scripts
    [ ] Disarm
    [ ] Cure blind if true sight < gouge/blind

Version 2
---------
Milestone goal: Improve scripts to be more useful
[ ] Have option to encrypt character passwords
[ ] Search data for certain criterion
    [ ] Characters
    [ ] Speedwalks/Areas
[ ] Unfailing spell bots
[ ] Alexian compatible auction logging
    [ ] bash script to merge log into db source and pick out obvious repeats

Version 3
---------
Milestone goal: Add some features that might be considered ridiculous
[ ] Auto-CR (spam visit deities only)
[ ] Auto-Fight

