## Special Characters

### `dot( )`
'.' (dot)

```python
from Package.VerbalRegex import VerRe

v = VerRe().dot()
print(v.match('.'))  # match
```

### `anything( )`
Anything (excluding '\n')

```python
from Package.VerbalRegex import VerRe

v = VerRe().anything()
print(v.match('sdsd'))  # match
```