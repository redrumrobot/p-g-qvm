!flag is an incredibly flexible admin command. It allows you to change the various per-user flags, without having to open up admin.dat. This is very useful if you want to give someone perm designation, or some other command.

## Overview ##
  * **Admin.dat Flag**: f
  * Commands of !flag and !unflag
  * Can't change own flags
  * Can't change flags you don't have access to
  * Can't change flags of higher level admins
  * Rcon can use any flag

## Usage ##
### !flag ###
The basic usage of !flag is relatively simple. This command is very powerful. The syntax and usage is as follows:

`!flag` **<admin #>** _(modifier) {flag}_

Admin # is the number displayed in !listadmins
Modifiers are values that affect the of flag (-)
#### !flag # ####
Running !flag with only a # will display all the custom user flags for that user
#### !flag # $ ####
Running flag in the basic syntax, replacing `$` with the flag in choice and replacing `#` with the admin number, will add that flag to a users name.
#### !flag # -$ ####
Running flag with the deny syntax, this will deny flag `$` to admin `#`, regardless of other settings
### !unflag ###
Unflag removes a flag from an admins registered name, without adding a -
The syntax is:
`!unflag` **<admin #>** _(flag)_

Admin 3 is the number in !listadmins

## Notes ##
From any admin !flag # 