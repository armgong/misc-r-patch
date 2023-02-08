# misc-r-patch
some r related patch I am working on. update time to time, Currently include 

1 Windows to IANA timezone convertion (**done**)

2 High DPI patch about R on Windows, **SystemDPI awareness implemented now**. (**done**)

  Currently system high DPI implemention includes **all dialogs and windows (graphapp based ) in R on Windows, RGUI toolbar, plotting window, repo related dialogs. dialogs in base and utils packages and internet modules.**
 
 Test on three PCs (120 dpi,168 dpi and 192 dpi), **Rgui console,editor,pagers,download, repo related dialogs, preference,and most important plotting windows,all seems work smooth**.
 
 high DPI implemention is kind of diffcult,but it doable. grapheapp windows and controls are dpi unaware, but grapheapp font and font related draw text code are dpi aware. Half dpi unaware and half dpi aware in grapheapp, this means there no simple way to implement high dpi (the ideal way is only mod grapheapp code). 
 
 In R windows GUI,  there are three scenarios of dpi aware of dialog and windows in  R GUI.
  
 1 Some dialogs are fixed size, we can scaling them directly, for example preference dialog, data editor, toolbar and toolbar button . 
  
 2 Some dialogs or windows size is decide dynamicly by font width or height plus fixed padding.  the former is dpi aware, while the latter is dpi unware. we need  scaling only fixed padding manually in R code(not in grapheapp). for example repo related dialogs and libcurl and download dialogs , their size are  dynamicly cacluate use font height width and fix padding.
 
 3 Some dialogs or windows size is decide dynamicly by font width or height plus scrollbar or toolbar, both the former and the latter is dpi aware (if manifest is set to dpi aware), there are no need to modify them. for exmple Rgui console,editor,pagers,plotting windows.
 
 
This patch implement the first and second scenarios.
 
 
please see the three png file in this repo.

**Please attention, PerMonitorDPI awareness may be implement use WM_DPICHANGE in future if really needed, it will take time.**

3 to be determine
