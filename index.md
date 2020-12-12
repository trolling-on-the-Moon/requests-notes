![Image](https://avatars0.githubusercontent.com/u/75700504?s=460&u=2824feea3d4b0ac8dad59fc199386a2f08749994&v=4)
## 8off notes - python requests lib

Installation via pip requests.

Important requests methods:
1. GET
2. POST
3. HEAD
4. DELETE

- GET:
```markdown
import requests
url = ''https://httpbin.org/get'
r = requests.get(url)
```
# Add payload:
```markdown
payload = {'nickname' : 'SlickRick', 'level' : '33'}
r = requests.get(url, params = payload)
```
- HEAD:
```markdown
r = requests.head(url)
for i in r.headers:
   print(f'{i} : {r.headers[i]}')
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
