---
title: COVID-19 - Social Monitoring Toolkit
subtitle: Find the untold stories of the coronavirus crisis.
layout: layouts/base.njk
---


## Introduction
COVID-19 is a watershed moment for journalism. Social distancing, self-isolation, quarantines and lockdowns mean that all journalists suddenly need new, digital reporting tactics and workflows to do their jobs. Many don’t know where to begin. 

FATHM has developed a social monitoring toolkit that will help journalists learn, on the fly, how to efficiently, effectively and ethically use social media and digital platforms as reporting tools. We aim to support reporters -- especially those working from home -- to get up and running with social monitoring as quickly as possible. 

Our toolkit provides actionable guides and resources on:

- How to set up monitoring dashboards
- Best practices for engaging communities
- Tips and tools for verifying content from social platforms
- Strategies for effective publishing of stories sourced through social monitoring 

This initiative will focus on building the capacity of journalists and news organisations that have limited background or experience with social monitoring. It is also for journalism instructors and their students whose classes -- and reporting -- must move online due to the COVID-19 pandemic. 

Participating journalists will have the option to join a journalistic collaboration FATHM is building that aims to explore how COVID-19 is impacting people in under-reported communities around the world. Coordinated social monitoring will allow us to listen to and engage with people whose voices haven’t been heard for a very long time, if at all. The collaboration will identify and amplify new, essential stories about the response to the pandemic in news deserts, conflict zones and other marginalised communities. 


### What kinds of stories can social monitoring allow you to cover?
Social monitoring helps you report on stories that have typically gone under-reported. Through social monitoring you can connect with individuals who’ve  survived a disaster, deadly disease outbreak, or may have been eyewitnesses in another newsworthy event. 

For example, you may be able to conduct a Skype interview with someone who has been living under lockdown in Iran, China, or Italy during COVID-19, do a Q&A with an international student who can recount the ordeal of being stranded abroad due to COVID-19 travel restrictions, or write an article about the unique trends in different countries to combat anxiety and isolation during the pandemic.      


## Post pages

The pages found in in the posts

<ul class="listing">
{%- for page in collections.post -%}
  <li>
    <a href="{{ page.url }}">{{ page.data.title }}</a> -
    <time datetime="{{ page.date }}">{{ page.date | dateDisplay("LLLL d, y") }}</time>
  </li>
{%- endfor -%}
</ul>

## Links from an external data source

These links were sourced from [hawksworx.com](https://www.hawksworx.com/feed.json) at build time.

<ul class="listing">
{%- for item in hawksworx.entries.slice(0,5) -%}
  <li>
    <a href="{{ item.link }}">{{ item.title }}</a>
  </li>
{%- endfor -%}
</ul>


## Prerequisite

- [Node and NPM](https://nodejs.org/)

## Running locally

```bash
# install the dependencies
npm install

# External data sources can be stashed locally
npm run seed

# It will then be available locally for building with
npm run start
```

## Add some Netlify helpers
Netlify Dev adds the ability to use Netlify redirects, proxies, and serverless functions.

```bash
# install the Netlify CLI in order to get Netlify Dev
npm install -g netlify-cli

# run a local server with some added Netlify sugar in front of Eleventy
netlify dev
```

A serverless functions pipeline is included via Netlify Dev. By running `netlify dev` you'll be able to execute any of your serverless functions directly like this:

- [/.netlify/functions/hello](/.netlify/functions/hello)
- [/.netlify/functions/fetch-joke](/.netlify/functions/fetch-joke)

### Redirects and proxies

Netlify's Redirects API can provide friendlier URLs as proxies to these URLs.

- [/api/hello](/api/hello)
- [/api/fetch-joke](/api/fetch-joke)




