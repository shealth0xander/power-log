@echo OFF
echo PLEASE PUT IN CAPS DO YOU WANT TO UNLOCK THE PANEL
echo TO (Y) TO UNLOCK OR (N) TO CLOSE
echo OR TYPE IN (AV) TO GET VERSION CHECK
echo OR TYPE IN (T) TO GET IN TO TEST MODE
echo OR TYPE IN (G) TO GET IN TO GAME MODE
set/p "cho=>"
if %cho%==Y goto LOCK
if %cho%==YES goto LOCK
if %cho%==yes goto LOCK
if %cho%==shutdown goto LOCK
if %cho%==y goto LOCK
if %cho%==n goto END
if %cho%==no goto END
if %cho%==N goto END
if %cho%==NO goto END
if %cho%==AV goto APP
if %cho%==av goto APP
if %cho%==admin goto pass-admin
if %cho%==ADMIN goto pass-admin
if %cho%==T goto TEST-MODE
if %cho%==t goto TEST-MODE
if %cho%==G goto GAME-MODE
if %cho%==g goto GAME-MODE
echo Done.
goto CONFIRM
:APP
ren Locker

echo VERSION NUMBER IS
echo X,5,9,0
pause
echo DO YOU WANT TO UPDATE POWER CONTROL PANEL
echo IF YES PUT IN THE RUN PASSWORD
set/p "cho=>"
if %cho%==ADMIN goto apprun
if %cho%==Admin goto apprun
if %cho%==admin goto apprun
echo Done
goto CONFIRM
:GAME-MODE
ren Locker

echo GAME-MODE
echo welcome _____________
pause
echo OPENING FORM
pause
echo Done
goto CONFIRM
:apprun
cls
ren Locker

echo WELCOME UPDATE MODE 
pause
start C:\ProgramData\Microsoft\Windows
echo Done.
goto CONFIRM
:TEST-MODE
cls
ren Locker

echo WELCOME TEST MODE 
pause
echo PROGRAMME MODE IS DISABLED ON THIS PC 
echo PROGRAMME MODE IS ONLY ENABLE ON PROGRAMME`S PC 
pause
echo Done.
goto CONFIRM
:pass-admin
cls
ren Locker

echo PLEASE PUT IN YOUR Master PASSWORD
set/p "cho=>"
if %cho%==ADMIN goto admin-unlock
if %cho%==Admin goto admin-unlock
if %cho%==admin goto admin-unlock
echo Done.
goto CONFIRM
:admin-unlock
cls
ren Locker

echo PLEASE PUT IN YOUR NAME DO YOU WANT TO UNLOCK THE ADMIN PANEL
echo HINT IT USERS OR ADMIN OR ONEDRIVE
set/p "cho=>"
if %cho%==OneDrive goto WK
if %cho%==ONEDRIVE goto WK
if %cho%==onedrive goto WK
if %cho%==USERS goto WD
if %cho%==Users goto WD
if %cho%==users goto WD
if %cho%==ADMIN goto WA
if %cho%==Admin goto WA
if %cho%==admin goto WA
echo Done.
:WK
cls
ren Locker

echo WELCOME OneDrive
echo PLEASE PUT IN YOUR PASSWORD Craft
echo FOR A HINT PUT (H) 
echo BUT YOU HAVE TO START ALL OVER AGAIN
set/p "cho=>"
if %cho%==craft goto admin
if %cho%==Craft goto admin
if %cho%==CRAFT goto admin
if %cho%==H goto HINT
if %cho%==h goto HINT
if %cho%==STOP goto STOP
echo Done.
:WD
cls
ren Locker

echo WELCOME Users
echo PLEASE PUT IN YOUR PASSWORD PADDLE
echo FOR A HINT PUT (H) 
echo BUT YOU HAVE TO START ALL OVER AGAIN
set/p "cho=>"
if %cho%==PADDLE goto admin
if %cho%==Paddle goto admin
if %cho%==paddle goto admin
if %cho%==H goto HINT
if %cho%==h goto HINT
if %cho%==STOP goto STOP
echo Done.
:WA
cls
ren Locker

echo WELCOME Admin
echo PLEASE PUT IN YOUR PASSWORD Ag10
echo FOR A HINT PUT (H) 
echo BUT YOU HAVE TO START ALL OVER AGAIN
set/p "cho=>"
if %cho%==AG10 goto admin
if %cho%==Ag10 goto admin
if %cho%==ag10 goto admin
if %cho%==H goto HINT
if %cho%==h goto HINT
if %cho%==STOP goto STOP
echo Done.
:HINT
ren Locker

echo YOUR HINT IS 1 OF 20
echo DOB
echo HOBY
echo NICKNAME
echo ROOM NUMBER
echo BEST PHONE
echo BEST CAR COMPANY
echo 6 NUMBERS
echo BEST SHOP
echo BEST TV
echo BEST WORD
echo BEST TECHER
pause
echo Done.
goto CONFIRM
:LOCK
cls
ren Locker

ECHO "Choose an option .."
ECHO "1 = Logoff"
ECHO "2 = Reboot"
ECHO "3 = Hibernate"
ECHO "4 = Shutdown"
ECHO "5 = Stop"


SET /p option=Choose one option-

IF %option%==1 SHUTDOWN /l
IF %option%==2 SHUTDOWN -r -t 10
IF %option%==3 SHUTDOWN /h
IF %option%==4 SHUTDOWN /s /f /t 0
IF %option%==5 END
echo Done.
goto CONFIRM
:admin
cls
ren Locker

echo PLEASE PUT IN WHAT PAGE YOU WANT
echo page 1
echo page 2 Coming Soon
echo page 3 Coming Soon
set/p "cho=>"
if %cho%==1 goto admin1p
if %cho%==2 goto admin-next
if %cho%==3 goto ERROR-NOT-MADE

echo Done.
goto CONFIRM
:admin1p
ren Locker

ECHO "Choose an option .."
ECHO "1 = Control"
ECHO "2 = Microsoft Family"
ECHO "3 = Task Manager
ECHO "4 = System Information"
ECHO "5 = Reboot"
ECHO "6 = Local Security Policy"
ECHO "7 = Start Menu"
ECHO "8 = WINDOWS CHECK CODE"
ECHO "8 = Blank"
ECHO "9 = Blank"

SET /p option=Choose one option-

IF %option%==1 %windir%\System32\Control.exe
IF %option%==2 start "" https://account.microsoft.com/family/
IF %option%==3 %windir%\system32\taskmgr.exe /7
IF %option%==4 %windir%\system32\msinfo32.exe
IF %option%==5 SHUTDOWN -r -t 10
IF %option%==6 %windir%\system32\secpol.msc /s
IF %option%==7 start C:\ProgramData\Microsoft\Windows
IF %option%==8 goto WINDOWS-CHECK
IF %option%==9 Blank
if not exist "Blank" goto ERROR-Blank

echo Done.
goto CONFIRM
:WINDOWS-CHECK
ren Locker

echo GET A PEN NOW OR PUT ON NOTEPAD
pause
wmic path softwarelicensingservice get OA3xOriginalProductKey
pause
echo Done.
goto CONFIRM
:admin-next
ren Locker

ECHO "Choose an option .."
ECHO "1 = Blank"
ECHO "2 = Blank"
ECHO "3 = Blank"
ECHO "4 = Blank"
ECHO "5 = Blank""
ECHO "6 = Blank"
ECHO "7 = Blank"
ECHO "8 = Blank"
ECHO "8 = Blank"
ECHO "9 = Blank"

SET /p option=Choose one option-

IF %option%==1 Blank
IF %option%==2 Blank
IF %option%==3 Blank
IF %option%==4 Blank
IF %option%==5 Blank
IF %option%==6 Blank
IF %option%==7 Blank
IF %option%==8 Blank
IF %option%==9 Blank
if not exist "Blank" goto ERROR-Blank

:ERROR-NOT-MADE
echo Unable to locate folder containing FTP script, aborting
echo ERROR – folder not present >> Code ERROR-NOT-MADE
echo ERROR – coming soon 

:ERROR-Blank
echo Unable to locate folder containing FTP script, aborting
echo ERROR – Option not present >> Code ERROR-NOT-FIND
echo ERROR – coming soon 

echo Done.
cls
goto admin
