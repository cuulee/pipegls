# pipegls
Data analysis in pandas dfs > mapbox gl-js output made simple.


Usage:

Say you have dataframes with a colorkey and ready to be output to nlgeojson in memory.

NOTES:
  This module is for entirely data analysis and visualization purposes upon creating map default browser will be opened and then files (geojson created) will be served locally at point 8000. So be aware this is a procedural script thats more of a tool.


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
![](https://cloud.githubusercontent.com/assets/10904982/21585799/814e5a32-d095-11e6-9d13-ce9920fd05d9.png)
![](https://cloud.githubusercontent.com/assets/10904982/21585798/8148946c-d095-11e6-8191-29208a4b1c95.png)
