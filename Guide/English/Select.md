## Selection command

### `oneOf(patterns)`
- Parameters: *args (patterns) - Number: 1 ~

One of the (patterns) must match.

```python
from Package.VerbalRegex import VerRe

v = VerRe().oneOf('a', 'b')
print(v.match('a'))  # match
print(v.match('b'))  # match
print(v.match('c'))  # mismatch
```

### `notOneOf(patterns)`
- Parameters: *args (patterns) - Number: 1 ~

None of the (patterns) must match.

```python
from Package.VerbalRegex import VerRe

v = VerRe().notOneOf('a', 'b')
print(v.match('c'))  # match
print(v.match('b'))  # mismatch
print(v.match('a'))  # mismatch
```

### `oneOfRange(start, end)`
- Parameters: start (starting point), end (end)
- Note: The ASCII value of end must be greater than the ASCII value of start.

There must be a pattern that ranges from (start) to (end).

```python
from Package.VerbalRegex import VerRe

v = VerRe().oneOfRange('a', 'c')
print(v.match('a'))  # match
print(v.match('b'))  # match
print(v.match('c'))  # match
print(v.match('d'))  # mismatch
```

### `notOneOfRange(start, end)`
- Parameters: start (starting point), end (end)
- Note: The ASCII value of end must be greater than the ASCII value of start.

There must be no pattern in the range from (start) to (end).

```python
from Package.VerbalRegex import VerRe

v = VerRe().notOneOfRange('a', 'c')
print(v.match('a'))  # mismatch
print(v.match('b'))  # mismatch
print(v.match('c'))  # mismatch
print(v.match('d'))  # match
```