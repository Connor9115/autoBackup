# Description
autoBackup is a backup script (who would have thought) that allows the user the ability to backup on certain days/times. It uses cronjobs to acomplish this. It is written in BASH and designed for *nix.

**WARNING:** After autoBackup creates its cronjobs, DO NOT PUT ANY UNDER IT, instead put your cronjobs above the comments.

## Running the script and setup notes
To run the setup simply run the script called "autoBackup" (without quotes). To do this follow the proceeding steps:
1. Enter the directory with the autoBackup scripts and all its modules
2. Use the following command to run it 

./autoBackup

The autoBackupSetup script should NOT be run manually, you will be prompted to run it if you run the autoBackup script.
If the user opts to not run the setup script when prompted the main script will still function, but will fallback on backing up the user's home directory.

## Code Comments
Please forgive the awful comments, this script was meant to be read by people without much knowledge of shell scripting.

## Version info
All the script's modules have version info attached. This can be accessed by using the command. "autoBackup -v" for the version number or "autoBackup -vV" for the version number plus release notes.

## OptArgs
The script only uses three optargs, they are the following:
+ -v
..* Prints the version number to stdout
+ -V
..* Currently can only be used with -v to display version number and release notes
+ -p
..* Requires an integer argument after it. This can be used to bypass the main menu and get to the option you actually want by inputting the number that corrisponds with the menu option you want, an example of this follows:

./autoBackup -p 99

The above example will open then immediately exit the script.

## Multiple instances
The script will not allow more then one instance of itself at a time.
