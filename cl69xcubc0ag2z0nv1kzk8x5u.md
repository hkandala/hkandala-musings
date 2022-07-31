## Introducing keepup: stay up to date with tech trends from a single page

## Inspiration
As a developer, I visit a few websites to keep myself up to date with what's happening in the industry. These are some of sites that I regularly visit: [Hacker News](https://news.ycombinator.com/), [Reddit](https://www.reddit.com/), [Hashnode](https://hashnode.com/), [Dev.to](https://dev.to/), [Medium](https://medium.com/), [InfoQ](https://www.infoq.com/), [Github Explore](https://github.com/explore) etc. Because I visit these sites quite frequently, I wanted to build an aggregator app that dumps all the links in one place, free from all the clutter and supports both desktop and mobile. In simple words, I should be able to see all the trending links from all the sources I visit on a single page. So in a few weeks, I came up with an MVP (https://keepup.page). Thanks to Hashnode x Planetscale Hackathon for keeping me motivated throughout!

## What makes keepup different?
Now some of you will be thinking: why not use [daily.dev](https://daily.dev/) or any other RSS feed aggregator? While these alternatives have solved some of the use cases for me but not all. I don't prefer [daily.dev](https://daily.dev/) curating links using its dedicated scoring (upvotes) and discussion. I prefer to view the scores/upvotes from the source and do not have another discussion section as most of these websites already have a discussion section with an active thread. Also, I should be able to view top links weekly/monthly from each source. And most importantly the app should be as minimal as possible with super quick load times.

## Features

### Source Integrations
As a part of this MVP, I was able to integrate the following sources: [Hacker News](https://news.ycombinator.com/), [Dev.to](https://dev.to/), [Hashnode](https://hashnode.com/) and [Reddit](https://www.reddit.com/). Each integration has its own set of APIs defined using Next.js serverless functions. For every integration, there will be an index page listing all the possible API endpoints available for the given source. For example, Hacker News has Trending, Ask HN, Show HN, etc. And for certain integrations like Reddit and Hashnode users can also configure to view top posts of certain subreddit or a tag. All source APIs follow a contract such that UI components can render the links in a generic way independent of the source type.

### Sign in with NextAuth.js
Github provider is configured with the [NextAuth.js](https://next-auth.js.org/) for signing in and saving user data. Future work is to integrate more OAuth providers and also provide traditional email and password authentication.

### Manage Feed Dashboard
A default list of feeds is displayed on the https://keepup.page when loaded without signing in. User can customize their dashboard after signing in from the Manage Feed section. Manage Feed page is intuitive and users can fully customize every part of the feed, and add as many integrations as needed.

### Save for Later
This feature also requires the user to sign in with their Github account. Like the title says, this feature does what it is meant to be. Users can save links by clicking on the heart icon which is available beside every link in the dashboard.

### PWA Support
keepup is built fully responsive and works beautifully on screens of all sizes. As of now, keepup doesn't provide any offline experience, which is a work in progress.  

### Dark Theme Support
We all know it is a must to have a dark theme for any app these days :P

## Tech Stack
- [Next.js](https://nextjs.org/)
- [PlanetScale](https://planetscale.com/)
- [Prisma](prisma.io)
- [Geist UI](https://geist-ui.dev/en-us)
- [Vercel](https://vercel.com/)

## About Planetscale
Planetscale is a serverless database platform to quickly bring up a DB and integrate it with whatever app you are building. For keepup, planetscale has provided seamless integration with Prisma and Vercel and made my job very simple when it comes to managing a database. I find it quite interesting to bring in the concept of branches to databases. It is way more useful in practice than I imagined.

## What's Next?
- **More source integrations:** These source integrations are already in-progress: Medium, InfoQ, Github Explore, ProductHunt, and Indie Hackers. Let me know in the comment section for integration suggestions.
- **Email Newsletters: **Send a daily/weekly email digest for user configured feed.
- **Keyword Highlight:** Users should be able to add keywords that they are interested in and keepup should highlight all the links in the dashboard with those keywords present. This makes it easy to focus quickly on relevant links.

Would love to hear your feedback on https://keepup.page and let me know if you have any feature suggestions. You are always welcome to contribute to the project on Github.

## Reference
- [keepup.page](https://keepup.page/)
- [Github Repo](https://github.com/hkandala/keepup)
- [Database Schema](https://github.com/hkandala/keepup/blob/main/prisma/schema.prisma)