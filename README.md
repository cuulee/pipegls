# pipegls
Data analysis in pandas dfs > mapbox gl-js output made simple.


Usage:

Say you have dataframes with a colorkey and ready to be output to nlgeojson in memory.


```python
import pandas as pd
import pipegls as gl


polygons = pd.read_csv('polygons.csv')
lines = pd.read_csv('lines.csv')

# structuring a list with lines and polygons into the correct data structure 
# syntax row : [pandas dataframe, shape type ('lines','polygons','points','blocks') ] 
a = [[polygons,'polygons'],[lines,'lines']]

gl.make_map(a)
```
