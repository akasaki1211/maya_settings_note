## Evaluation

![Evaluation](./images/Evaluation.png)

### 01) Modes
```python
from maya import cmds, mel, utils

# Evaluation Mode
cmds.evaluationManager(mode='parallel')
""" 
    mode (string):
        off      : DG
        serial   : serial
        parallel : parallel
"""

# GPU Override
#  On
mel.eval('turnOnOpenCLEvaluatorActive')
#  Off
mel.eval('turnOffOpenCLEvaluatorActive')

#  *To execute in usersetup.py, use maya.utils.executeDeferred().
def turnOff_GPUOverride(*args):
    mel.eval('turnOffOpenCLEvaluatorActive')
utils.executeDeferred(turnOff_GPUOverride)
```

## command references
* [evaluationManager](https://help.autodesk.com/cloudhelp/2023/ENU/Maya-Tech-Docs/CommandsPython/evaluationManager.html)