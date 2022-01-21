# search
A Python package for searching and getting results with many different search engines.
#Installation
To install the package, run the following command:
```bash
python3 -m pip install search
```
Or install from Github:
```bash
python3 -m pip install git+https://github.com/Neurs1/search.git
```
#Features
This package support many different search engines like Google, Yahoo, Bing,... (Full list).
Provide the best speed with BS4 using lxml.
Fix bugs, adapt new features and page design from fearch engines.
Output in dict type, easier to interact with.
#Usage
Search using multiple search engines!
```python3
import search
search.google("Python")
search.bing("Python")
search.yahoo("Python")
```
Customize Google search engine:
```python3
import search
search.google("Python", max_results = 30, lang = "en")
```
You could use your own proxy:
```python3
import search
search.google("Python", proxy = {
    "https": "https://example.com"
  })
```
#Known issues
I could only find max results and languages in Google search engine, still trying to figure it out on other search engines.
