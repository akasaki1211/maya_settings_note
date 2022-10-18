## Python

### Python Path

#### Python commands
```python
import sys
sys.path.append('path')
```

#### Environment variables
```batfile
set PYTHONPATH="path"
```

### Don't create compiled python file (.pyc)

#### Python commands
```python
import sys
sys.dont_write_bytecode = True
```

#### Environment variables
```batchfile
set PYTHONDONTWRITEBYTECODE=1
```