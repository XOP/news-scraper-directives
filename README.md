# NewScraper Directives




> The directives repo for the NewScraper  
> [https://github.com/XOP/news-scraper](https://github.com/XOP/news-scraper)




## Format

Directives are being digested by the [NewScraper application](https://github.com/XOP/news-scraper) and passed to the [NewScraper Core](https://github.com/XOP/news-scraper-core).  
If you follow, the uniformity of the content is pretty self-evident.

Directives can be provided in both JSON and YML format.  
The latter is used due to it's robust and descriptive nature.

Given the [template](_template.yml) here: 

```
'NAME':
  url: ''
  elem: ''
  link: ''
  author: ''
  time: ''
  image: ''
  limit: N
```

`NAME`  
name of the resource, **required**

`url`  
url of the resource, **required**

`elem`  
CSS selector of the news item container element, **required**

`link`  
CSS selector of the link (<a href="">...</a>) _inside_ of the `elem`
If the `elem` itself _is_ a link, this is not required

`author`  
CSS selector of the author element _inside_ of the `elem`

`time`  
CSS selector of the time element _inside_ of the `elem`

`image`  
CSS selector of the image element _inside_ of the `elem`
This one can be `img` tag or any other - NewScraper will search for `data-src` and `background-image` CSS properties to find proper image data

`limit`  
how many `elem`-s from the `url` will be scraped, maximum


To pass the collection of resources simply add empty line between them.  
See [examples](blogs.yml).

```
'NAME 1':
  url: '...'
  elem: '...'
  
'NAME 2':
  url: '...'
  elem: '...'

...

'NAME N':
  url: '...'
  elem: '...'
```




## [MIT License](LICENSE)
