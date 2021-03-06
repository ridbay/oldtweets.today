# oldtweets.today
You know of [Facebook's "On This Day" feature](https://www.facebook.com/help/439014052921484)? It shows you the posts you made (and a few other things) on this day (for example, February 15) in the past. If you're on Facebook, you can see yours at [facebook.com/onthisday]().

Yeah, this is that, but for Twitter. You can see the tweets you've made on this day in the past by visting [oldtweets.today]().

## How this works
This repo contains two different components.

### The website
A simple page served via GitHub Pages from the `docs/` folder. This is where you enter your Twitter username, and then a request is made to the API to retrieve your old tweets.

### The API
The API is a serverless JavaScript function hosted on [Google Cloud Functions](https://cloud.google.com/functions/) (Node.js 8). Normally, this would call Twitter's API to request your old tweets, but Twitter's Standard Search API only provides access to tweets made in the past 7 days, so that's pretty useless.
 
 However, you can use the search on twitter.com to fetch tweets by a particular person on a particular date, with little restriction. That's what this API does. It runs the search on Twitter's site, scrapes the results and extracts the necessary data and returns the tweets requested as embeddable HTML.

## License
Do whatever you want with the code.

## Support
Hey, I love building cool, open-source stuff like this. You can help support me and keep them running by [becoming a Patron](https://patreon.com/shalvah). Thanks!🤗
