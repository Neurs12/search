# search
A Python package for searching and getting search results with many different search engines.
# Installation
To install the package, run the following command:
```bash
python3 -m pip install search
```
Or install from Github:
```bash
python3 -m pip install git+https://github.com/Neurs1/search.git
```
# Features
This package support many different search engines.
Provide the best speed with BS4 using lxml.
Fix bugs, adapt new features and page design from fearch engines.
Output in dict type, easier to interact with.
# Usage
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
search.google("Python", proxies = {
    "https": "https://example.com"
  })
```
# Output format
Example `search.google("YouTube")`:
```python3
{
  0: {
    "title": "YouTube",
    "url": "https://www.youtube.com/"
  },
  1: {
    "title": "YouTube - Apps on Google Play",
    "url": "https://play.google.com/store/apps/details?id=com.google.android.youtube&hl=en_US&gl=US"
  },
  2: {
    "title": "YouTube - Home | Facebook",
    "url": "https://www.facebook.com/youtube/"
  },
  3: {
    "title": "YouTube - Wikipedia",
    "url": "https://en.wikipedia.org/wiki/YouTube"
  }
}
```
How to access search results:
```python3
import search
results = search.google("YouTube")
#At the first result, get the title of the result.
print(results[0]["title"])
#At the second result, get the url of the result.
print(results[1]["url"])
```
Output:
```bash
YouTube
https://play.google.com/store/apps/details?id=com.google.android.youtube&hl=en_US&gl=US
```
# Supported search engines
- Google
- Bing
- Yahoo
- Aol
# Known issues
I could only find max results and languages in Google search engine, still trying to figure it out on other search engines.
