# Links Page

[![Build Status](https://travis-ci.org/igventurelli/links-page.svg?branch=master)](https://travis-ci.org/igventurelli/links-page) [![Discord](https://img.shields.io/discord/728053623799676928.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/aEfF8CC)

A simple project that exposes your social links in a single page.  
This kind of page is used a lot on Instagram on the "bio link".

## How does it works?

This project is based on a json file called `config.json`.  
This file contains all the data you want to expose: your picture, name, bio and obviously: your links

The structure is a quite simple:

```json
{
  "avatar": "img/photo.png",
  "name": "John Doe",
  "bio": "I'm a very cool person",
  "links": [
    {
      "image": "img/linkedin.png",
      "url": "https://www.linkedin.com/in/johndoe/",
      "text": "in/johndoe",
      "title": "LinkedIn"
    },
    {
      "image": "img/medium.png",
      "url": "https://medium.com/j@ohndoe/",
      "text": "@johndoe",
      "title": "Medium"
    }
  ]
}
```

## Setup

To run the project in development mode you just need to follow these simple steps:

- `npm install`
- `npm run dev`

## Technologies

This project is made with:
- [Vue](https://vuejs.org/)
- [Nuxt](https://nuxtjs.org/)
- [Vuetify](https://vuetifyjs.com/en/)

## CI/CD

We are using [Travis CI](https://travis-ci.org/) to build and deploy the static page into the GitHub Pages, but you can use any CI/CD you want (including [GitHub Actions](https://github.com/features/actions), by the way)

For Travis be able to deploy to GitHub Pages, you need to create a [personal token](https://github.com/settings/tokens) on GitHub and [store it on Travis](https://docs.travis-ci.com/user/deployment/pages/#Setting-the-GitHub-token) (or the CI you use).  
