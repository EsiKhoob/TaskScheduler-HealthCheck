TaskScheduler-HealthCheck
=========================
Note:This program is provided AS IS, with no warranty.

This program tries to find the cause of Windows Event log`s ERROR ID: 413 (Task Scheduler service failed to load tasks at service startup. Additional Data: Error Value: 2147942402)
as this link suggests:
https://social.technet.microsoft.com/Forums/windows/en-US/1f677dd3-bdb7-4650-9164-d8e2c66b7708/task-scheduler-error?forum=w7itprogeneral

This program compares 2 limbs of the Windows registry tree where Task information is stored:

    HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\TaskCache\Tree
  & HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\TaskCache\Tasks

The goal, then is to compare the two and expose the differences.  However, it is not ideal:  There are some tasks under \Tree but not under \Tasks, and that is normal and you should not need to delete them.

If you found some registry keys in the last (of three) tests which is in RED color, you should search for those names in the registry and delete them yourself (by using regedit.exe); in my experience, that will resolve the error.

Programmer: Ehsan Abidi Ashtiani
Email: AbidiAshtiani@gmail.com
Programming Language: C# (.NET Framework 4.5)
