## Basic commands
### `start_of_line( )`
Matches from the beginning of the line.
```python
v = VerRe().start_of_line().find('banana')
print(v.match('banana')) # match
print(v.match('anana')) # does not match
```

### `end_of_line( )`
Matches until the end of the line.
```python
v = VerRe().find('banana').end_of_line()
print(v.match('banana')) # match
print(v.match('bananas')) # does not match
```

### `find(string)`
Determine the expression to match.
```python
v = VerRe().find('hello')
print(v.match('hello')) # match
```

### `maybe(string)`
Determine expressions that might match. <br>
(It may or may not match)
```python
v = VerRe().find('http').maybe('s')
print(v.match('https')) # match
print(v.match('http')) # match
```

### `OR(string A, string B)`
Either A or B matches.
```python
v = VerRe().OR('hello', 'world')
print(v.match('hello')) # match
print(v.match('world')) # match
```