TaskScheduler-HealthCheck
=========================
Note:This program is AS IS ,without no waranty.

This program tries to find the cause of Windows Event log`s ERROR ID: 413 (Task Scheduler service failed to load tasks at service startup. Additional Data: Error Value: 2147942402)
as this link suggests:
https://social.technet.microsoft.com/Forums/windows/en-US/1f677dd3-bdb7-4650-9164-d8e2c66b7708/task-scheduler-error?forum=w7itprogeneral

This program compare 2 places of Windows registry where Task`s information is stored ,but do not change anything.

HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\TaskCache\Tree

VS

HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\TaskCache\Tasks

Hope we can figure out the problem with looking at the difference of these 2 places.
Be informed that if there are some Task under \Tree but not under \Tasks, It`s normal and you do not need to delete them.

If you found some registry keys under last title with red color, you should search it`s name all over the registry and delete them to resolve the error.(as far as I experienced)

Programmer: Ehsan Abidi Ashtiani
Email: AbidiAshtiani@gmail.com
Programming Language: C# (.NET Framework 4.5)
