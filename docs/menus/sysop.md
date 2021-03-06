# //SYSOP Menu
***

These commands can be run while logged-on to the WWIV BBS. You will be prompted to enter the System Password when you use //SYSOP to access the SysOp Tools.

```
[A]       Allow Editor               [B]       Sub Editor
[C]       Chain Editor               [D]       Dir Editor
[E]       Events Editor              [G]       Bulletin Editor
[I]       Instance Editor            [J]       Conference Editor
[M]       Menu Editor                [T]       Text Editor
[U]       User Editor                [V]       Voting Editor
[K]       Print Votes                [Q]       Quit               
```

### [A] Allow Editor  
This option applies to registered sysops only and is
associate with the OPT_FAST_Search setup.  A program is
provided called WWSORT.EXE which should be run first.

This program creates your original ALLOW.DAT file which
will permit a fast search for duplicate file names.  The
ALLOWEDIT option gives the sysop the ability to add or
remove file names from the binary file.  A sysop might
want to add the name of a non-existant file if he did
not care to have that file uploaded to him.  For example,
sysops frequently get a "scam" uploaded to them called
FASTCASH.  This "scam" is like a chain letter for BBSes.
Putting FASTCASH as a file name would prevent someone's
uploading a file by that name.  By the same token, if
the sysop needs to remove a filename from the binary
list, he has the option to do so by using the ALLOWEDIT
option.                                                       

### [C] Chain Editor  
Brings up the [Chain \ Door Editor Menu](doors)
### [E] Events Editor  
Bring up the Events editor. Events are scheduled Jobs run on a schedule or after other system events.
### [I] Instance Editor  
Allows the SysOp to see the status of all instances. Shutdown individual instances or all instances.
### [M] Menu Editor  
Menu commands are called by there name and a number of options parameters.  
The following forms are valid syntax  

    command without parameters : menucmd
    command with one parameter : menucmd "xyz"
    command with two parameters : menucmd 123, "abc def"
    command with two parameters : menucmd(456,"abc")

You can stack multiple menu commands by seperating them with the ~ key.
The following code ...
'menucmd1 ~ menucmd2("abc") ~ menucmd3 "abc", 123'
... will execute menucmd1 (without any parameters), menucmd2 with abc as a
parameter, and finally, menucmd3 with "abc" and 123 as parameters.
Most menu commands run without any parameters at all, and most are taken
straight from the main and xfer menus. Additional commands are added to
manage the menu system as well as a few commands which will help you to
emulate other BBSes.

Command | Description
--------|------------
MENU | Loads up and starts running a new menu set, where equals the name of the menu to load.
ReturnFromMenu | Unloads the current menu and goes back to the menu that loaded the current one. If you try to return from the very first menu, it will just be reloaded.
EditMenuSet | This command will take you into the menu editor. Keep careful to keep this command tied down as anyone with access to the menu editor will have 100% access to your system.
DLFreeFile <dirfname> <filename> | This will download a file, but not check ratios or charge a download charge. You must specify the dirfilename, which is the name of the data file in the transfer editor. filename is the name of the file being downloaded.
DLFile | This will download a file, with a check for ratios and will update the kb downloaded and number of files  downloaded. You must specify the dirfilename, which is the name of the data file in the transfer editor. filename is the name of the file being downloaded.
RunDoor <doorname> | Runs a door (chain) with doorname matching, exactly, the description you have given the door in //CHEDIT
RunDoorFree <doorname> | Runs a door (chain) with doorname matching, exactly, the description you have given the door in //CHEDIT, but this function bypasses the check to see if the user is allowed to run the door.
RunDoorNumber <door#> | Like RunDoor, but you must specify the #1 in //CHEDIT instead of the description.
RunDoorNumberFree | Like RunDoorFree, but you must specify the #1 in //CHEDIT instead of the description.
PrintFile <filename> | Prints a file, first checking to see if you specified an absolute path, then the language dir, then the gfilesdir. It will use the usual checks to determine .ANS, or .MSG if not specified.
PrintFileNA <filename> | Just like PrintFile, but the user can not abort it with the space bar.
SetSubNumber <key> | Equivalent to typing in a number at the main menu, it sets the current sub number.
SetDirNumber <key> | Equivalent to typing in a number at the xfer menu, it sets the current dir number.
SetMsgConf <key> | Sets the subboards conference to key
SetDirConf <key> | Sets the xfer section conference to key
EnableConf | Turns conferencing on
DisableConf | Turns conferencing off
Pause | Pauses the screen, like 'pausescr()' in C code
ConfigUserMenuSet | Takes the user into the user menu config so they can select which menuset they want to use, etc...
DisplayHelp <filename> | Prints the 'novice menus' for the current menu set, or if one doesn't exist, it will generate one using the menu definitions.
SelectSub |  his will prompt the user to enter a sub to change to. However, it does not first show the subs (like Renegade). However, you can stack a sublist and then this command to mimic the action.
SelectDir | Like SelectSub, but for the xfer section.
SubList | List the subs available
UpSubConf | Increment ()) to the previous conference number
DownSubConf | Decrement ({) to the next sub conference
UpSub | Increment the current sub# (+)
DownSub | Decrement the current sub number (-)
ValidateUser | Validate a new users. I think this '!'
Doors | Enter the doors, or chains section. Like '.'
TimeBank | Enter the time bank
AutoMessage | Read the auto message
BBSList | Read the bbslist
RequestChat | Request chat from the sysop
Defaults | Enter the normal 'defaults' section
SendEMail | Enter and send email 'E' from the main menu
Feedback | Leave feedback to the syosp. 'F'
Bulletins | Enter the bulletins (or 'gfiles') section. 'G'
HopSub | Hop to another sub. 'H'
SystemInfo | View the system info
JumpSubConf | Jump to another sub conference.
KillEMail | Kill email that you have sent 'K'
LastCallers | View the last few callers
ReadEMail | Read your email
NewMessageScan | Do a new message scan
Goodbye | Normal logoff 'O'
PostMessage | Post a message in the current sub
NewMsgScanCurSub | Scan new messages in the current message sub
RemovePost | Remove a post
TitleScan | Scan the titles of the messages in the current sub
ListUsers | List users who have access to the current sub
Vote | Enter the voting both
ToggleExpert | Turn 'X'pert mode on or off (toggle)
YourInfo | Display the yourinfo screen
ExpressScan | I think this will scan all new messages without pausing.
WWIVVer | Get the wwiv version
InstanceEdit | Sysop command to edit the instances
ConferenceEdit | Sysop command ot edit the conferences
SubEdit | Sysop command to edit the subboards
ChainEdit | Sysop command to edit the doors or chains
ToggleAvailable | Toggle the sysop availability for chat
ChangeUser | Sysop command equal to //CHUSER, to change into another users
CLOUT | Who knows, sopposed to do a callout
Debug | Who knows, some debug mode
DirEdit | Sysop command to edit the directory records
ShellDOS | Sysop command to shell to dos
Edit | Sysop command to edit a text file
BulletinEdit | Sysop command to edit the bulletins 'gfiles'
LoadText | Sysop command to load a text file that will be edited in the text editor
ReadAllMail | Sysop command to read all mail
Reboot | Sysop command to reboot the machine
ReloadMenus | This is probably obsolete.
ResetUserIndex | Rebuild the user index. //RESETF if I am not mistaken
ResetQScan | Set all messages to read (I think)
MemStat | Show memory stats. //STAT
PackMsgs | Pack message bases.
VoteEdit | Sysop command to edit the voting both
Log | Syosp command to view the log file
NetLog | Sysop command to view the network log
Pending | Shows which net files are ready to be sent
Status | Who knows...
TextEdit | Edit a text file
UserEdit | Sysop command to edit users
VotePrint | Show the voting statistics
YLog | View yesterdays log
ZLog | View the ZLog
ViewNetDataLog | View the net data logs
UploadPost | Allow a user to upload a post that will be posted
CLS | Clear the screen
NetListing | Show networks
WHO | Show who else is online
NewMsgsAllConfs | Do a new message scan for all subs in all conferences '/A'
MultiEMail | Send multi-email
NewMsgScanFromHere | Read new messages starting from the current sub
ValidatePosts | Sysop command to validate unvalidated posts
ChatRoom | Go into the multiuser chat room
DownloadPosts | Download all new posts in a text file
DownloadFileList | Download the file list in a text file
ClearQScan | Makes all message unread???
FastGoodBye | Logoff fast '/O'
NewFilesAllConfs | New file scan in all directories in all conferences
ReadIDZ | Sysop command to read the file_id.diz and add it to the extended description
UploadAllDirs | Syosp command to add any files sitting in the directories, but not in the file database to wwiv's file database 
UploadCurDir | Sysop command to scan the current directory for any files that are not in wwiv's file database and adds them to it.
RenameFiles | Sysop command to edit and rename files
MoveFiles | Sysop command to move files
SortDirs | Sort the directory by date or name
ReverseSortDirs | Sort the directory by date or name, backwards.
AllowEdit | Sysop command to enter the 'ALLOW.DAT' editor.
ReadINI | Re-read the INI files
UploadFilesBBS | Import a files.bbs (probably a CD) into the wwiv's file database
DirList | List the directory names in the xfer section
UpDirConf | Go to the next directory conference '}'
UpDir | Go to the next directory number '+'
DownDirConf | Go to the prior directory conference '{'
DownDir | Go to the prior directory number '-'
ListUsersDL | List users with access to the current xfer sub
PrintDSZLog | View the DSZ log
PrintDevices | Show the 'devices'. I have no idea why.
ViewArchive | List an archive's contents
BatchMenu | Enter the batch menu 'B'
Download | Download a file 'D'
TempExtract | Extract an archive to the temp directory
FindDescription | Search for a file by description
ArchiveMenu | Enter the archive menu
HopDir | Hop to another directory number 'H'
JumpDirConf | Jump to another directory conference 'J'
ListFiles | List the file in the current directory
NewFileScan | List files that are new since your 'New Scan Date (usually last call)' 'N'
SetNewFileScanDate | Set the 'New Scan Data' to a new date
RemoveFiles | Remove a file you uploaded
SearchAllFiles | Search all files???
XferDefaults | Enter the xfer section defaults
Upload | User upload a file
YourInfoDL | Prints user info for downloads
UploadToSysop | Upload a file into dir#0, the sysop dir.
ReadAutoMessage | Read the auto message
SetNewScanMsg | Enter the menu so that a user can set which subs he want to scan when doing a new message scan
ReadMessages | Read messages in the current sub
RUN | In a future version, this will run a script file
EventEdit | Sysop command to enter the event editor
LoadTextFile | Looks like a duplicate to 'LoadText'
GuestApply | Allows a guest to apply for access
ConfigFileList | Enter the List+ configurator so the user can set it up to look like he wants

### [U] User Editor  
The User editor allows you to change the account information, SL, DSL, etc. and other user settings.

### [K] Print Votes  
Lists the voting questions.

### [?] Display Help  
Displays the //SYSOP command menu

### [B] Sub Editor  
The SUB Editor allows you to add\remove\edit SUBs or Boards.
### [D] Dir Editor  
The DIR Editor allows you to add\remove\edit Directories in the Transfer section of the BBS
### [G] Bulletin Editor  
The Bulletin editor allows you add\remove\edit Directories in the G-Files section of the BBS
### [J] Conference Editor  
Conferences are groupings of SUBs. This option lets you add\remove\modify Conferences.
### [T] Text Editor  
TEDIT - Edit a text file located in the GFILES directory only

**NOTE:** This command functions basically the same as E from WFC.  
EDIT - Runs the SysOp editor (or full screen editor if selected); allows the text files to be located any- where on the hard disk, instead of just in the GFILES directory as with TEDIT.
                                                                    
### [V] Voting Editor  
The voting editor allows you to add\remove and modify the polls on your BBS. Polls allow
you to ask your users for feedback, collect opinions on current events. Any sort of multiple
choice\yes|no question you want.

### [Q] Quit  
That one's pretty obvious.

