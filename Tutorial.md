This page describes how to bootstrap a basic config for gfuzzy.

# Code #
The minimal python code would look like:

```
import system

self.system = system.System()
self.system.LoadConfig('myconfig.protoascii')
inputs = {'set1': [0, 1, 2], 'set2': [2, 1, 0]}
self.system.UpdateValues(inputs)
outputs = self.system.results.copy()

```

# Config File #

```

  name: "CPU Memory System"
  input:<
    name: "set1"
  >
  input:<
    name: "set2"
  >
  output:<
    name: "health"
  >
  set:<
    name: "high"
    type: "triangular"
    param: 0.5
    param: 1
  >
  set:<
    name: "low"
    type: "rectangle"
    param: 0
    param: 0.5
  >
  rule:<
    name: "1"
    antecedent: "set1 is high * set2 is high"
    consequent: "set3 is low"
  >
  consequent:<
    name: "set3 is low"
    output: "set3"
    set: "low"
  >

```