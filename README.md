<div align="center">
<h1 align="center">Search with Chinese Social Media</h1>
Build A Chinese Media search engine using less than 500 lines of code with `lepton`, leveraging the data from Weibo, Little Red Book and many other social media platforms.
<br/>
<a href="https://search.lepton.run/" target="_blank"> Live Demo </a>
<br/>
<img width="70%" src="https://github.com/henryalps/search_with_chinese_media/blob/main/static/images/demo.png">
</div>


## Features
- Built-in support for Reasoning Augmented Generator (RAGs)
- Built-in support for crawl and search social media
- Customizable and user-friendly UI interface
- Shareable and cached search results

## Setup Search Engine API
Default supported search engines: 
- Weibo
- Xiaohongshu _(pending)_
- Bing
- Google
 
### Bing Search
To use the Bing Web Search API, please visit [this link](https://www.microsoft.com/en-us/bing/apis/bing-web-search-api) to obtain your Bing subscription key.

### Google Search
You have three options for Google Search: you can use the [SearchApi Google Search API](https://www.searchapi.io/) from SearchApi, [Serper Google Search API](https://www.serper.dev) from Serper, or opt for the [Programmable Search Engine](https://developers.google.com/custom-search) provided by Google.

## Setup LLM and KV

> [!NOTE]
> We recommend using the built-in llm and kv functions with Lepton. 
> Running the following commands to set up them automatically.

```shell
pip install -U leptonai && lep login
```


## Build

1. Build web
```shell
cd web && npm install && npm run build
```
2. Run pip install
```
pip install -r requirements.txt
```
3. Run server
For Weibo Search:
```shell
BACKEND=WEIBO python search_with_lepton.py
```

For Bing Search:
```shell
export BING_SEARCH_V7_SUBSCRIPTION_KEY=YOUR_BING_SUBSCRIPTION_KEY && BACKEND=BING python search_with_lepton.py
```

For Google Search using SearchApi:
```shell
export SEARCHAPI_API_KEY=YOUR_SEARCHAPI_API_KEY
BACKEND=SEARCHAPI python search_with_lepton.py
```

For Google Search using Serper:
```shell
export SERPER_SEARCH_API_KEY=YOUR_SERPER_API_KEY
BACKEND=SERPER python search_with_lepton.py
```

For Google Search using Programmable Search Engine:
```shell
export GOOGLE_SEARCH_API_KEY=YOUR_GOOGLE_SEARCH_API_KEY
export GOOGLE_SEARCH_CX=YOUR_GOOGLE_SEARCH_ENGINE_ID
BACKEND=GOOGLE python search_with_lepton.py
```

## Miscellaneous
[history.ipynb](history.ipynb) stores some commands excuted during deployment

## LISCENSE

![Non-commercial Use License](LICENSE)
