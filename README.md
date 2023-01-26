# misc-r-patch
some r related patch I am working on. update time to time, Currently include 

1 Windows to IANA timezone convertion (**done**)

2 High DPI patch about R on Windows, **SystemDPI awareness implemented now**. (**done**)

  Currently system high DPI implemention includes **all dialogs and windows (graphapp based ) in R on Windows, RGUI toolbar, plotting windows, repo related dialogs and windows, dialogs in base and utils packages and internet modules.**
 
 Test on three PCs (120 dpi,168 dpi and 192 dpi), **Rgui console,editor,pagers,download, repo related dialogs, preference,and most important plotting windows,all seems work smooth**.
 
please see the three png file in this repo.

**Please attention, PerMonitorDPI awareness may be implement use WM_DPICHANGE in future if really needed, it will take time.**

3 to be determine
