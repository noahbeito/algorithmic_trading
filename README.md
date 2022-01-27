![bot](https://assets.website-files.com/5f9c358b57fa1ea8ea314144/60495194f0b69d52b1a40ee7_The%2016%20Best%20Crypto%20Trading%20Bots_1200x630_1300ppi%20(1)-p-1080.png)
# algorithmic_trading
Using machine learning to create a trading bot and to evaluate its performance.
---
## Technologies
This analysis leverages python 3.7 with the following packages and libraries:
* [pandas](https://github.com/pandas-dev/pandas)
* [numpy](https://github.com/numpy/numpy)
* [hvplot](https://github.com/holoviz/hvplot)
* [pathlib](https://github.com/python/cpython/blob/main/Lib/pathlib.py)
* [scikit-learn](https://github.com/scikit-learn/scikit-learn)
---
## Imports
```python
import pandas as pd
import numpy as np
from pathlib import Path
import hvplot.pandas
import matplotlib.pyplot as plt
from sklearn import svm
from sklearn.preprocessing import StandardScaler
from pandas.tseries.offsets import DateOffset
from sklearn.metrics import classification_report
```
---
## Findings

Our original svc classifier model with short and long SMA windows of 4 and 100 produced a model that beat actual returns:

![trade algo 1](https://user-images.githubusercontent.com/90667844/151292254-925b8846-b1f0-4263-97d0-4ab0f931c3c2.png)

Decreasing the SMA rolling windows decreased the returns of the model:

![- rolling windows](https://user-images.githubusercontent.com/90667844/151292355-c3a767a2-b29d-4d92-8fe5-1a780bb03ca7.png)

Increasing the SMA rolling windows also decreased returns of the model:

![+ rolling windows](https://user-images.githubusercontent.com/90667844/151292301-a9baa81d-a20b-48a2-a507-3402a968c017.png)

The ADA Boost model gave us periods where the returns beat actual returns, however, it performed rather erratically starting in late 2019. This could potentially be explained by the volatility and unusual market conditions caused by COVID. 

![ada boost](https://user-images.githubusercontent.com/90667844/151292961-c65d2195-914c-4b60-86fc-d2c49aa1c990.png)

---
## Contributors
[Noah Beito](https://www.linkedin.com/in/noah-beito/)
---
## License
[MIT](https://github.com/git/git-scm.com/blob/main/MIT-LICENSE.txt)
