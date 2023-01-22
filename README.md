# misc-r-patch
some r related patch I am working on. update time to time, Currently include 

1 Windows to IANA timezone convertion(done)

2 High DPI patch about R on Windows, Modify graphapp and related r codes( Rgui,package,modules), SystemDPI awareness implemented. 

  Currently windows and dialogs included in RGui and  R base package and  modules modified for DPI awareness. also toolbar and toolbarbuttion modify for DPI awareness. 
 
 Test on two PCs(168 dpi and 192 dpi), Rgui include console,editor,pagers,download, repo related dialogs, preference,and most important plotting windows,all seems work smooth.
 
 please see the two png file in this repo.


3 PerMonitorDPI awareness will be implement use WM_DPICHANGE in future.
