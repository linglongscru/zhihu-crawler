# zhihu-crawler

[![StyleCI](https://styleci.io/repos/98495729/shield?style=plastic)](https://styleci.io/repos/98495729)
[![Latest Stable Version](https://poser.pugx.org/pithyone/zhihu-crawler/v/stable)](https://packagist.org/packages/pithyone/zhihu-crawler)
[![Latest Unstable Version](https://poser.pugx.org/pithyone/zhihu-crawler/v/unstable)](https://packagist.org/packages/pithyone/zhihu-crawler)
[![License](https://poser.pugx.org/pithyone/zhihu-crawler/license)](https://packagist.org/packages/pithyone/zhihu-crawler)
[![Build Status](https://travis-ci.org/pithyone/zhihu-crawler.svg)](https://travis-ci.org/pithyone/zhihu-crawler)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/pithyone/zhihu-crawler/badges/quality-score.png)](https://scrutinizer-ci.com/g/pithyone/zhihu-crawler)
[![Code Coverage](https://scrutinizer-ci.com/g/pithyone/zhihu-crawler/badges/coverage.png)](https://scrutinizer-ci.com/g/pithyone/zhihu-crawler)
[![Build Status](https://scrutinizer-ci.com/g/pithyone/zhihu-crawler/badges/build.png)](https://scrutinizer-ci.com/g/pithyone/zhihu-crawler/build-status)

🕷 轻量级知乎爬虫

## Feature

- 简单易操作，不用关心 `Cookie`
- 自定义输出对象属性，:smirk: 输出回答中所有图片

## Installation

```shell
$ composer require pithyone/zhihu-crawler
```

## Basic Usage

```php
<?php

use pithyone\zhihu\crawler\Handler\AnswerHandler;

$answerHandler = new AnswerHandler(58481349, 1);

$answerHandler->pick(function ($item) {
    // 存储操作，保存到数据库...
    return $item['images']; // 输出回答中所有图片
});

```

## Links

- [知乎热门钓鱼贴图片版](http://zhihu.pithyone.tk/)
- [热门收藏 - 知乎](http://pithyone.tk/feed/zhihu/collection)
- [本月最热 - 知乎](http://pithyone.tk/feed/zhihu/month)

## License

MIT
