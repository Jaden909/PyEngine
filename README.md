# PyEngine
## Introduction
PyEngine is a python module designed to work with Pygame to make game development with Pygame easier. It includes functions that Pygame lacks, such as functions for generating UI elements.

## Usage
Once PyEngine is installed and imported into a project, all of its functions and classes are ready for use. 

## Examples
### `save()` and `load()`
Two of PyEngine's most useful functions are the `save()` and the `load()` functions. They save and load json files respectively.
An example of these functions:
```python
    import pygame #PyEngine dependency
    import PyEngine
    saveFile={'hp':100,'mana':100,'lives':2}
    PyEngine.save('saveData.json',saveFile)
    loadedFile=PyEngine.load('saveData.json')
    print(loadedFile)
    >>>{'hp':100,'mana':100,'lives':2}
```

### The `autoWrap()` function
Rendering font using pygame has one downside: there is no support for multi-line rendering, unless you split the text up yourself. With PyEngine's `autoWrap()` fucntion, you can turn a string into as many lines as you need, depending on the given `width` parameter
```python
lines=PyEngine.autoWrap('Long string to really test this functions mullti-line capabillities',50,pygame.font.SysFont('arial',12),'white')
for line in lines:
    surface.blit(line,(32,line.index()*32)) #Will blit each line of text 32 pixels vertically away from each other
```
