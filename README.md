# PyEngine Documentation
#### Introduction
PyEngine is a python module designed to work with Pygame to make game development with Pygame easier. It includes functions that Pygame lacks, such as functions for generating UI elements.

#### Usage
Once PyEngine is installed and imported into a project, all of its functions and classes are ready for use. Two of its most useful functions are the `save()` and the `load()` functions. They save and load json files respectively.
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
