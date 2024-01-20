## Repeat command
### `repeatPrevious(repeat count)`
- Parameter: value (number of repetitions) - int type

The previous pattern must be repeated (number of repetitions).
```python
from VerbalRegex import VerRe

v = VerRe().find('a').repeatPrevious(3)
print(v.match('aaa')) # match
v2 = VerRe().find('ab').repeatPrevious(3)
print(v2.match('ababab')) # match
```

### `repeatPreviousOver1( )`
The previous pattern must be repeated at least once.
```python
from VerbalRegex import VerRe

v = VerRe().find('a').repeatPreviousOver1()
print(v.match('bbb')) # does not match
print(v.match('a')) # match
print(v.match('aa')) # match
```

### `repeatPreviousOver0( )`
The previous pattern must be repeated at least 0 times.
```python
from VerbalRegex import VerRe

v = VerRe().find('a').repeatPreviousOver0()
print(v.match('ba')) # match
print(v.match('a')) # match
print(v.match('aa')) # match
```

### `repeatPreviousRange(minimum number, maximum number)`
- Parameters: start (minimum number of repetitions), end (maximum number of repetitions) - int type

The previous pattern must be repeated more than (minimum number of repetitions) and less than (maximum number of repetitions).
```python
from VerbalRegex import VerRe

v = VerRe().find('a').repeatPreviousRange(2, 3)
print(v.match('a')) # does not match
print(v.match('aa')) # match
print(v.match('aaa')) # match
```