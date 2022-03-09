# Geetest Slider Captcha Bypass
[![](https://img.shields.io/badge/Python-Selenium-blue)](https://pypi.org/project/selenium/)
[![](https://img.shields.io/badge/Python-OpenCV-yellow)](https://pypi.org/project/opencv-python/)

Bypass Geetest Slider Captcha using _**Selenium and OpenCV**_

<hr>
To install required dependencies, run this in a shell/terminal

```python
pip install -r requirements.txt
apt install chromium-chromedriver # if running on linux
```

Now import the `GSC_solver` class

```python
from gsc import GSC_solver

gsc = GSC_solver()
search_term = 'bts_official_bighit'
driver = gsc.solve(f'https://www.tiktok.com/@{search_term}')
```

or

```python
. . .

driver = webdriver.Chrome(chrome_driver_path, desired_capabilities=caps, options=chrome_options)
search_term = 'bts_official_bighit'
driver.get(f'https://www.tiktok.com/@{search_term}')

# Solve captcha by passing webdriver object
driver = gsc.solve(driver)

. . .
```

<hr>
<p>
<img src="snapshot/0b8796d53da6cd73610cb336e2cc45da/captcha.gif" width="250" height="180" />
<img src="snapshot/0c2e924a9af52a7a17b90dd7dd2651ad/captcha.gif" width="250" height="180" />
<img src="snapshot/0c3222c9aa061ca1bac3d0af4e440866/captcha.gif" width="250" height="180" />
</p>
<p>
<img src="snapshot/0b8796d53da6cd73610cb336e2cc45da/process.gif" width="250" height="145" />
<img src="snapshot/0c2e924a9af52a7a17b90dd7dd2651ad/process.gif" width="250" height="145" />
<img src="snapshot/0c3222c9aa061ca1bac3d0af4e440866/process.gif" width="250" height="145" />
</p>
<hr>

If you want to save snapshots like these, give location at `snapshot_path` in `solve`

```python
gsc.solve(. . . , snapshot_path = 'enter_path_here')
```
