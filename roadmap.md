
## Key Topics - strategic view

1. Antibots will become more and more widespread
Website antibots will become more sophiscitaed. 

This is positive trend for the company because it means more users will have to use proxy rotating services. 

In 2010 I could run a curl to get data from any website, and it worked. In 2026 I have to use playwright with stealth even on my local machine to get 1 single request
running from manyw websites. 

DC proxies getting less and less usable without session, browser reuse.

2. AI will be enable even more users to get data.

AI Chatbots will make it much easier for people to extract data. In 2014 you had to write scrapy spider, you had to know python. Now you can generate scrapy spider no problem
with Claude or Codex.

This means more bots being created, more bot traffic. 

This creates feedback loop with point 1, because more bot traffic means more websites needing to defend it, and websites getting more aggressive.

3. AI will require huge amount of data and will be inefficient handling the data.

Point 2 will mean many bots created by humans will access the web. 

Many of them will be extremely inefficient and wasteful in data usage, e.g. I see my openclaw, instead of making browserless request to website it needs to control
my browser by default, it searches for content using browser relay, it controls my browser and spends a lot of time and rendering on something that would take one single 
browserless request.

This means there will be demand for tools that make efficient cheap usage of data, e.g. if my openclaw would know they can make one single browserless request he would make it
but it does not know, someone needs to tell them, there needs to be API for that. 

## Zyte Strentghs and Weaknesses

Zyt we got many legacy systems and heritage of manual configurations

## Key objectives

### Operational transformations - less manual, custom work

Key area: CCM, Crawlera Config Configurator, hundreds of configurations created by humans. 

* configurations per different google services per subdomains
* one configuration for all

Objective: just single config per netloc working for all clients. Human intervention on crawl management should be limited to minimum


### Pricing

AI Agent is just software, and software needs clear guidance on pricing

Website tiers are fine, but simplify pricing:
* less websites covered by tiers, increase threshold to XXX
* for domains where it does matter, ruthless process to make sure our tier pricing is adequate and competitive
* remove charges that are not needed and complexity (screenshot charge)
* full transparency about pricing for agent


Make our pricing easy to consume, imagine if AI agent needs to decide which scraping API to use, why would they choose Zyte?

Create central pricing API where you can pass specs on what needs to be done and we return clear price. 

### Configuration

Client should not have to configure anything, just works out the box, plug and play. No need to add any headers, decide if they need to use browser or not.
We just give the data straightway.

Currently not the case, if site needs browser it won't work. 

### Integrations with everything
We need to integrate zyte API with every single agent service availbale. Make it easy for everyone to use it. 


### Simple web API-s

INstead of passing headers, cookies etc to set zipcode in walmart - set zipcode via parameter, store id

### Prompt as primary API argument - set up crawl argument

If user needs to pass a prompt, does not know what to do, we return information how to do it with zyte API.

Not via docs, via api

request: "how do I extract product price information from walmart for Nevada"
response payload: "url, store_id, price

As little params as possible, not more, but less paramters.

### Crawl not just scrape
right now you got to run sofware to discoer, we are rest request-response, we don't support crawl, where we discover and explore website, add crawl endpoint
where crawler actually make sseveral requests and explores the website, finds relevant content. 

e.g.: "find alls news about Crude OIL and give me back all the data", site: finance.yahoo.com and you get back a structured list of articles about crude oil

### High speed mode where it matters
If client needs fast download, add it for them


### AIO scraping, scrape LLM if needed
Scrape all majort LLM-s
* chatgpt
* gemini
* claude
* perplexity
* ...

### SERP scraping
Extract all data from google, bing. Trends, reviews, maps, business listings, return data in structured format easy to parse, good support for uule.

### aaa
