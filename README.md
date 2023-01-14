# Esa Crawler

simple esa.io crawle through API

# Get started

## Install

Install esa crawler dependencies with poetry

``` shell
poetry install
```

## Setup

you need to specify environment variable ESA_ACCESS_TOKEN, ESA_TEAM_NAME in your .env file.
``` .env
ESA_ACCESS_TOKEN={YOUR ACCESS TOKEN}
ESA_TEAM_NAME={YOUR TEAM NAME}
```

## Crawl

crawl your esa team posts

``` shell
poetry run python crawler.py
```

NOTE: esa crawler writeout `.last_crawled.json` in the end of crawl to effecient crawling when you crawl again.
If `.last_crawled.json` is existed, esa crawler crawl only posts that newly updated posts since last time.
You can hack `.last_crawled.json` for specifing post updated_at period to crawl.