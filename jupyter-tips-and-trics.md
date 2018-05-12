# Jupyter tips and trics

1. Create Jupyter cell and copy your snippet:

```python
import os
import re
import sys
import shutil
import random
import itertools 
import matplotlib

import numpy as np
import pandas as pd 
import matplotlib.pyplot as plt

from tqdm import tqdm_notebook
from glob import glob
from shutil import copyfile
from sklearn.model_selection import train_test_split
from sklearn.metrics import confusion_matrix

%matplotlib inline
%load_ext autoreload
%autoreload 2
```

2. Run cell and remember cell excecution number.
3. Generate the macro: `%macro -q __imp ${execution_number}`.
4. Store the macro: `%store __imp`. 
5. Make the macro auto-loadable. Edit `~/.ipython/profile_default/ipython_config.py`:

```python
c = get_config()
c.StoreMagics.autorestore = True
```
