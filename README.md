# rsync-checker-win

A small Windows system tray app that indicates if an instance of [rsync.exe] is running

![rsync-is-not-running]
![rsync-is-running]

## Huh?

I use [rsync] (via [Windows Subsystem for Linux]) on my home server to back up my PC, but previously I was unable to see when a backup was running.

Now I use this small Python app to display an icon in Windows 10's system tray that changes if a running instance of rsync is detected, and then returns to normal when a running instance of rsync is no longer detected.

## Installation

1. Ensure [Python 3 for Windows] is installed
2. Ensure the required Python module [infi.systray] is installed (most easily done using the package installer [pip])

    ```
    C:\> pip install infi.systray
    ```

3. Run `rsync-checker.py` using your locally installed version of Python 3.

### Run on Startup

1. Locate your Windows user's `Startup` folder by entering

    ```
    shell:startup
    ```

    into a Windows Run dialog.
    The path of this folder will likely resemble the following:

    ```
    %USERPROFILE%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup
    ```

2. Copy a shortcut to `rsync-checker.py` to the `Startup` folder located in Step 1.

## Credits

The [infi.systray] Python module enabling Windows system tray functionality was created by [Infinidat].

The icons ([arrow-circle-up], [check-circle]) used in this script are [licensed] by [Font Awesome].

[rsync.exe]: https://rsync.samba.org
[rsync-is-not-running]: img/rsync-is-not-running.png
[rsync-is-running]: img/rsync-is-running.png
[rsync]: https://rsync.samba.org
[Windows Subsystem for Linux]: https://docs.microsoft.com/en-us/windows/wsl/about
[Python 3 for Windows]: https://www.python.org/downloads/release/python-374/
[infi.systray]: https://github.com/Infinidat/infi.systray
[pip]: https://pypi.org/project/pip/
[Infinidat]: https://github.com/Infinidat
[arrow-circle-up]: https://fontawesome.com/icons/arrow-circle-up?style=solid
[check-circle]: https://fontawesome.com/icons/check-circle?style=solid
[licensed]: https://fontawesome.com/license/free
[Font Awesome]: https://fontawesome.com