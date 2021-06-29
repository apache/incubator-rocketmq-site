# Apache RocketMQ website
[![Build Status](https://travis-ci.com/apache/rocketmq-site.svg?branch=master)](https://travis-ci.com/apache/rocketmq-site)

This is the website for [Apache RocketMQ](	http://rocketmq.apache.org/).

## About
This website is based on Jekyll and a Jekyll theme named Minimal Mistakes.

## Prerequisite
1. Ruby
2. Gem

## Install & Run
1. gem install jekyll bundler
2. git clone this repo
3. cd rocketmq-site
4. bundle install
5. bundle exec jekyll serve

## Deploy to asf-site
1. Checkout branch asf-site and merge the changes:`git merge origin/master`
2. Generate the site to content directory: `bundle exec jekyll build`
3. Check the changes and commit.
4. Push asf-site to remote branch.

## Questions

### How to post articles to **Documentation**?
Create a .md file in rocketmq-sites/_docs/, Jekyll will finish the rest of the work.

Please refer to **01-quick-start-guide.md** for more details.

### How to post articles to **Blog**?
Create a .md file in rocketmq-sites/_posts/, Jekyll will finish the rest of the work.

Please refer to **2016-12-23-mastering-component-compatible-dependency.md** for more details.

### How to modify the navigation?
Please refer to **_data/navigation.yml** for more details.
