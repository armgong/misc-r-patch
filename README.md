# misc-r-patch
some r related patch I am working on. update time to time, Currently include 

1 Windows to IANA timezone convertion(done)

2 High DPI patch about R on Windows, Modify graphapp and related r codes( Rgui,package,modules), SystemDPI awareness implemented. 

  currently the modify  windows and dialogs included in RGui and utils package and internet module. now toolbar and toolbarbuttion  also modify for DPI awareness. 
 
  Test on two PCs(168 dpi and 192 dpi), RGui include console,editor,pagers,download, package related dialog,preference,and most important plotting windows,all seems work !!
  


3 PerMonitorDPI awareness will be implement use WM_DPICHANGE in future.
