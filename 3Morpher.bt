@echo off
setlocal enabledelayedexpansion
cls
color E5
title 3Morpherz
mode 60,7
echo.
echo.
echo                  System Interface Acceleration
echo.
timeout /t 3 >nul
goto :tweak
:Tweak
cls
echo Performing system optimization tasks...

REM Registry tweaks for performance optimization
set tweaks=^
    "HKLM\SYSTEM\CurrentControlSet\Services\ServiceName" /v "Start" /t REG_DWORD /d 4 /f
    "HKLM\SYSTEM\CurrentControlSet\Control\FileSystem" /v "NtfsDisableLastAccessUpdate" /t REG_DWORD /d 1 /f
    "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v "TcpAckFrequency" /t REG_DWORD /d 1 /f
    "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\VisualEffects" /v VisualFXSetting /t REG_DWORD /d 2 /f ^&^
    "HKLM\SOFTWARE\Policies\Microsoft\Windows\DataCollection" /v AllowTelemetry /t REG_DWORD /d 0 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Control\PriorityControl" /v Win32PrioritySeparation /t REG_DWORD /d 2 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management" /v DisablePagingExecutive /t REG_DWORD /d 1 /f ^&^
    "HKLM\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU" /v NoAutoUpdate /t REG_DWORD /d 1 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v EnableTCPA /t REG_DWORD /d 0 /f ^&^
    "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v HideFileExt /t REG_DWORD /d 0 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Control\GraphicsDrivers" /v TdrLevel /t REG_DWORD /d 0 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v SystemResponsiveness /t REG_DWORD /d 0 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v "GPU Priority" /t REG_DWORD /d 8 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces" /v TcpAckFrequency /t REG_DWORD /d 1 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows\Windows Error Reporting" /v Disabled /t REG_DWORD /d 1 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System" /v EnableLUA /t REG_DWORD /d 0 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management\PrefetchParameters" /v EnableSuperfetch /t REG_DWORD /d 0 /f ^&^
    "HKLM\SOFTWARE\Policies\Microsoft\Windows\Windows Search" /v AllowCortana /t REG_DWORD /d 0 /f ^&^
    "HKLM\SOFTWARE\Policies\Microsoft\Windows\Windows Search" /v AllowIndexingService /t REG_DWORD /d 0 /f ^&^
    "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender" /v DisableAntiSpyware /t REG_DWORD /d 1 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks\Games" /v KnockbackResistance /t REG_DWORD /d 1 /f ^&^
    "HKCU\System\GameConfigStore" /v GameDVR_Enabled /t REG_DWORD /d 0 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management" /v SecondLevelDataCache /t REG_DWORD /d 2048 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile" /v NetworkThrottlingIndex /t REG_DWORD /d ffffffff /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks" /v Games /t REG_DWORD /d 6 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks" /v ProAudio /t REG_DWORD /d 5 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks" /v BackgroundTasks /t REG_DWORD /d 3 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks" /v Multimedia /t REG_DWORD /d 5 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile\Tasks" /v CpuPriorityClass /t REG_DWORD /d 3 /f ^&^
    "HKCU\Software\Microsoft\Windows\DWM" /v AnimationsShiftKey /t REG_DWORD /d 1 /f ^&^
    "HKCU\Software\Microsoft\Windows\DWM" /v FlashWindowOnActivate /t REG_DWORD /d 0 /f ^&^
    "HKCU\Software\Microsoft\Windows\DWM" /v Animations /t REG_DWORD /d 0 /f ^&^
    "HKCU\Software\Microsoft\Windows\DWM" /v BlurBehind /t REG_DWORD /d 0 /f ^&^
    "HKCU\Software\Microsoft\Windows\DWM" /v Composition /t REG_DWORD /d 0 /f ^&^
    "HKCU\Software\Microsoft\Windows\DWM" /v EnableMachineCheck /t REG_DWORD /d 0 /f ^&^
    "HKCU\Software\Microsoft\Internet Explorer\Main" /v "Start Page" /t REG_SZ /d "about:blank" /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\DriverSearching" /v SearchOrderConfig /t REG_DWORD /d 0 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\DeliveryOptimization" /v SystemSettingsDownloadMode /t REG_DWORD /d 0 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 1 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v DisableTaskOffload /t REG_DWORD /d 1 /f ^&^
    "HKCU\Control Panel\Keyboard" /v KeyboardDelay /t REG_SZ /d 0 /f ^&^
    "HKCU\Control Panel\Keyboard" /v KeyboardSpeed /t REG_SZ /d 31 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Services\LanmanWorkstation\Parameters" /v SizReqBuf /t REG_DWORD /d 4356 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters" /v SizReqBuf /t REG_DWORD /d 4356 /f ^&^
    "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\USB" /v "DisableSelectiveSuspend" /t REG_DWORD /d 1 /f ^&^
    "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\usbflags" /v DisableSelectiveSuspend /t REG_DWORD /d 1 /f ^&^
    "HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer" /v Serialize /t REG_DWORD /d 0 /f ^&^
    "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters" /v DefaultTTL /t REG_DWORD /d 78 /f ^&^
    "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces" /v MTU /t REG_DWORD /d 1400 /f ^&^
    "HKLM\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU" /v NoAutoRebootWithLoggedOnUsers /t REG_DWORD /d 1 /f ^&^
    "HKCU\Control Panel\Desktop" /v MenuShowDelay /t REG_SZ /d 400 /f ^&^
    "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Maintenance" /v MaintenanceDisabled /t REG_DWORD /d 1 /f ^&^
    "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender\Real-Time Protection" /v DisableRealtimeMonitoring /t REG_DWORD /d 1 /f ^&^
    "HKLM\SYSTEM\CurrentControlSet\Control\Remote Assistance" /v fAllowToGetHelp /t REG_DWORD /d 0 /f ^&^
    "HKLM\SOFTWARE\Policies\Microsoft\Windows\Windows Search" /v AllowSearchToUseLocation /t REG_DWORD /d 0 /f ^&^
    "HKLM\SOFTWARE\Policies\Microsoft\Windows\Windows Search" /v DisableWebSearch /t REG_DWORD /d 1 /f ^&^
    "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v DisableNotificationCenter /t REG_DWORD /d 1 /f
    REG ADD "HKLM\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces" /v TcpAckFrequency /t REG_DWORD /d 1 /f
    reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\VisualEffects" /v VisualFXSetting /t REG_DWORD /d 2 /f ^&^
    reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows\DataCollection" /v AllowTelemetry /t REG_DWORD /d 0 /f ^&^

reg add !tweaks! >nul 2>&1
del /q /f %temp%\*.*
del /q /f temp\*.*
sfc /scannow
wmic process where name="java.exe" CALL setpriority "realtime"
cleanmgr /sagerun:1
wmic cpu get loadpercentage
sc config ServiceName start= disabled
for %%i in (standby monitor disk) do (
    powercfg -change -%%i-timeout-ac 0
    powercfg -change -%%i-timeout-dc 0
)
powercfg /change hibernate-timeout-ac 0
powercfg /change hibernate-timeout-dc 0
schtasks /create /tn "Defrag Task" /tr "defrag.exe C:" /sc weekly /d MON /st 03:00
netsh int tcp set global autotuninglevel=disabled
netsh int tcp set global chimney=disabled
netsh int tcp set global rss=disabled   
cls
echo            System optimization tasks completed.
timeout /t 2 >nul
exit /b
