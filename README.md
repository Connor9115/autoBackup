# EDIT
Excuse me, one day I was eating spaghetti and a bit of it got on my code. I initially made this for a class when we were told to "give recommendations of an backup manager" so my smartass cooked up this in 15 minutes. Over time however it got a bit out of hand and turned into what you see here. I have since become a better speghetti cook with only small amounts of it leaking into my code.

## Original README
# Description
autoBackup is a backup script (who would have thought) that allows the user the ability to backup on certain days/times. It uses cronjobs to acomplish this. It is written in BASH and designed for *nix.

**WARNING:** After autoBackup creates its cronjobs, DO NOT PUT ANY UNDER IT, instead put your cronjobs above the comments.

## Dependencies
+ tar
+ bc
+ cronie

## Running the script and setup notes
To run the setup simply run the script called "autoBackup" (without quotes). To do this follow the proceeding steps:
1. Enter the directory with the autoBackup scripts and all its modules
2. Use the following command to run it 

./autoBackup

The autoBackupSetup script should NOT be run manually, you will be prompted to run it if you run the autoBackup script.
If the user opts to not run the setup script when prompted the main script will still function, but will fallback on backing up the user's home directory.

## Interface
autoBackup is controlled by a CLI in a way that has been made as simple as possible to learn.

## Multiple instances
The script will not allow more then one instance of itself at a time.

## Code Comments
Please forgive the awful comments, this script was meant to be read by people without much knowledge of shell scripting.

## Version info
All the script's modules have version info attached. This can be accessed by using the command 

./autoBackup -v

or

./autoBackup -vV

for the version number plus release notes.

## OptArgs
The script only uses three optargs, they are the following:
+ -v
  + Prints the version number to stdout
+ -V
  + Currently can only be used with -v to display version number and release notes
+ -p
  + Requires an integer argument after it. This can be used to bypass the main menu and get to the option you actually want by inputting the number that corrisponds with the menu option you want, an example follows:

./autoBackup -p 99

The above example will open then immediately exit the script.

## Bug reports / Feature requests etc.
Please read the feature_request.md and bug_report.md files, these can be found in the following directory:

.github/ISSUE_TEMPLATE

**FYI:** 
+ Spelling/grammer errors are considered a mid-level (2) issue
+ Problems/features affecting or improving ease-of-use should be described as such in the report
