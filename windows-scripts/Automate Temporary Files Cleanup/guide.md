# Automate temporary files cleanup
A simple PowerShell script that **magically** clears temporary files every time your PC boots up. Because who wants to do that manually?  

## How it works?
This script wipes out everything inside `%TEMP%` every time your PC starts. No more bloated temp folders!

## Installation (Set It & Forget It)
1. Save the script
    - Copy the script inside ClearTempFiles.ps1 into a text editor. (You can use Neovim but Notepad is the easiest)
    - Save the file as `ClearTempFiles.ps1`
2. Automate it using Task Scheduler
    - Open Task Scheduler (Win + R → taskschd.msc)
    - Click Create Basic Task
    - Name it something like "Auto Clear Temp"
    - Set the trigger to "When I log on"
    - Under "Action," choose "Start a program" → Browse & select powershell.exe
    - In the "Add arguments" box, type: `-ExecutionPolicy Bypass -File "C:\path\to\ClearTemp.ps1"`
    - Save & exit. That’s it!
