## My notes - python requests lib

Installation via pip requests.

[Official documentation](https://requests.readthedocs.io/)

Important requests methods:
1. GET
2. POST
3. HEAD
4. DELETE

- GET:
```python
import requests
url = 'https://httpbin.org/get'
r = requests.get(url)
print(r.text)
```
## Add payload:
```python
# payloads by get, note ? is added automatically
payload = {'nickname' : 'SlickRick', 'level' : '33'}
r = requests.get(url, params = payload)
print(r.url)
```
- HEAD:
```python
r = requests.head(url)
for i in r.headers:
   print(f'{i} : {r.headers[i]}')
# print(r.headers['content-type']) # or you can use: r.headers.get('content-type')
```

- JSON:
```python
## SENDING JSON, note: just parameter to encode payload as json:
payload = {"JSON_KEY" : "JSON_VALUE"}
r = requests.post('https://httpbin.org/post', json = payload)
# print(r.text)
```
YOU COULD ALSO DO A LONGER WAY BY ENCODING BY YOURSELF A JSON, but that means you will import json:
```python
r = requests.post(url, data = json.dumps(payload))
print(r.text)
# !!! so use option A with parameter json = some_payload !!!
```
### Using the json parameter in the request will change the Content-Type in the header to application/json

Displaying as a JSON, use external libs like json and pprint. Say you got status_code == 200 for certain API, and you'd like to print it as json, easy to do it with:
```python
import requests, json, pprint
...
bearer_token = <YOUR_TOKEN> # replace YOUR_TOKEN including <> in string, ex: "123xczj43"
url = 'https://api.twitter.com/2/tweets/1028039268030210048'
headers = {"Authorization" : f'Bearer {bearer_token}'}
r = requests.get(url, header = headers).json() # <<<--- NOTE .json() now it is using external lib json
pprint.pprint(r)
>> OUTPUT:
   {'data': {'id': '1028039268030210048',
             'text': 'Do You Dip Your Pizza In Ranch?'
             }
   }
```






You can use the [editor on GitHub](https://github.com/trolling-on-the-Moon/web_one/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/trolling-on-the-Moon/web_one/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
