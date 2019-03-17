# scrapy-douban

用scrapy爬取豆瓣top250


翻页

```
        next_link=response.xpath('//span[@class="next"]//a//@href').extract()
        if next_link:
            next_link=next_link[0]
            yield scrapy.Request('https://movie.douban.com/top250'+next_link,callback=self.parse)
```
