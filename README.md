# Welcome to React-Review-Carousel 🎠

This package provides two imports for information, either the raw information 🥩🥊 (RawReviews) or the prettyfied (CSS-infused) information 💅✨ (ReviewCarousel).<br></bt>
You need to provide your own API keys wherever necessary. No rate bumming!<br></br>

# ReviewCarousel

Some want a prebuilt solution that both fetches and displays reviews, and trust me when I say this: this is the best option. I've tried other paid solutions that performed poorly and was formatted poorly as well.

## Getting started (ReviewCarousel)
Start by running this command in your terminal: <pre>npm i -g react-review-carousel</pre>

Then place this at the top of your file: <pre>import { ReviewCarousel } from 'react-review-carousel';</pre>

We need to feed the ReviewCarousel a source of reviews for it to get to work fetching and displaying them.<br></br>
Let's start with some Google reviews. Paste a link... wait! React-Review-Carousel doesn't use links? 😳<br></br>
No, links to reviews are temporary, so I've built some search functionality into this nifty package to overcome the power of search engines 😓<br></br>

Instead, we are going to pass a search term to an instance of ReviewCarousel. 

⭐️ &nbsp; ```Try to be descriptive here, if you have a bagel shop in New York City, put your exact address along with the full name. (Even if you don't have a bagel shop in NYC, this is good practice).```
<br></br>
Ok, now let's start by rendering an instance of ReviewCarousel.
<pre>< ReviewCarousel 
    limit={20}
    search='Brooklyn Bagel & Coffee Company 286 8th Ave, New York, NY 10001'
    /></pre>

### CSS Overriding: 
Everything is based on CSS flexbox, so keep that in mind if you're trying to override the styles. I always keep styling minimal so overrides are mostly possible.

To override the CSS (or attempt to override it) include a style prop in the component:
<pre>< ReviewCarousel 
    search='Brooklyn Bagel & Coffee Company 286 8th Ave, New York, NY 10001'
    style={{ padding: '5px', backgroundColor: 'gray' }}
    /></pre>

## Note: The default limit is 20, and the absolute max is 50.
### To get more results, use the RawReviews function below.
<br></br>
 ## That's It! 🤯

 ### Enjoy your prebuilt Review Carousel!

<br></br>
# RawReviews

Others may be looking for just the review data, without having to build a web-scraping server themselves. RawReviews returns a list of reviews, that you can then map to whatever you want (your own carousel, for example).

Heres the import:
<pre>import RawReviews from 'react-review-carousel';</pre>

Whereas ReviewCarousel is a React Component Class, RawReviews is a function that returns a list.

To get a list, you need to instantiate RawReviews to your own variable and await the result.

⭐️ &nbsp;```We achieve this through the fetchReviews(searchTerm: String, limit: Number) function that RawReview provides```

<pre>const reviewData = await RawReviews.fetch('Brooklyn Bagel & Coffee Company 286 8th Ave, New York, NY 10001', 20);</pre>

If you don't provide a limit, the web scraper may get a little out of control and start to get results from random places. Keep that in mind, because I only enforce a limit on < ReviewCarousel />!

<br></br>

# Conclusion

If you have any questions, you can reach out to me directly: blankinship2002@gmail.com

If you liked this package, consider supporting me: https://www.buymeacoffee.com/blankinshipb