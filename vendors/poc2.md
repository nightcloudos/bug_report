Cross-Site Scripting (XSS) vulnerability in WP Simple Table Manager Plugin <= 1.5.6 at WordPress.

[![pPyHQ8f.png](https://s1.ax1x.com/2023/09/08/pPyHQ8f.png)](https://imgse.com/i/pPyHQ8f)
 - [ ] STEPS:
	1.After installing the plugin, click Simple Table Manager. Then click Export CSV. 	
	Put poc in CSV file name then click Save.
	
	POC：

	```
	"><img src=1 onerror=alert(/xss/)>
	```
[![pPyH1xS.png](https://s1.ax1x.com/2023/09/08/pPyH1xS.png)](https://imgse.com/i/pPyH1xS)
 - [ ] 
	2.Then XSS vulnerability triggered
[![pPyHJbj.png](https://s1.ax1x.com/2023/09/08/pPyHJbj.png)](https://imgse.com/i/pPyHJbj)
[![pPyHU5q.png](https://s1.ax1x.com/2023/09/08/pPyHU5q.png)](https://imgse.com/i/pPyHU5q)