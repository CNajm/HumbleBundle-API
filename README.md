Retrieves information from [Humble Bundle](https://www.humblebundle.com) store pages smoothly and cleanly using selenium.
<br>
>You need a [PhantomJS](http://phantomjs.org) executable in your PATH environment

## Examples
**Getting the time left for a promotion**
```python
import humbleScraper

mypage = humbleScraper.page("https://www.humblebundle.com/store/LIMITED_TIME_OFFER_PAGE")
timer = mypage.getTimeLeft()

# >> 2 days 7 hours 49 mins 35 secs
```

**Getting a product's name**
```python
import humbleScraper

mypage = humbleScraper.page("https://www.humblebundle.com/store/PRODUCT_PAGE")
name = mypage.getProductName()

# >> DOOM®
```

**Getting a product's price information**
```python
import humbleScraper

mypage = humbleScraper.page("https://www.humblebundle.com/store/PRODUCT_PAGE")
name = mypage.getPriceInformation()

# >> {'price_preview': '$14.99 USD', 'price_full': '$24.99', 'price_currency': 'USD', 'price': '14.99', 'price_modifier': '-40%', 'availability': 'http://schema.org/InStock'}
```

## License
MIT
