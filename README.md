# Esa Crawler

Simple esa.io crawler through API.
Crawled result is output as jsonl that consisting of one article per line.

# Get started

## Install

Install esa crawler dependencies with poetry

``` shell
poetry install
```

## Setup

You need to specify environment variable ESA_ACCESS_TOKEN, ESA_TEAM_NAME in your .env file.

``` .env
ESA_ACCESS_TOKEN={YOUR ACCESS TOKEN}
ESA_TEAM_NAME={YOUR TEAM NAME}
```

## Crawl

Crawl your esa team posts

``` shell
poetry run python crawler.py
```

NOTE: esa crawler writeout `.last_crawled.json` in the end of crawl to effecient crawling when you crawl again.
If `.last_crawled.json` is existed, esa crawler crawl only posts that newly updated posts since last time.
You can hack `.last_crawled.json` for specifing post updated_at period to crawl.