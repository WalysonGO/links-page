# Links Page

[![Build Status](https://travis-ci.org/igventurelli/links-page.svg?branch=master)](https://travis-ci.org/igventurelli/links-page)

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

For you be able to deploy to GitHub Pages, you need to create a [personal token](https://github.com/settings/tokens) on GitHub and store it on Travis (or the CI you use).  
Besides the personal token, we need to provide the "environment name" to the CI, for the project be built ready to the GH Pages.  
We can perform these actions with environment variables:

- `GITHUB_ACCESS_TOKEN`, that will store the personal token you've created
- `DEPLOY_ENV`, that must contains the value: `GH_PAGES`

For more information about the `DEPLOY_ENV` and why do we need it, please take a look to the [Nuxt documentation](https://nuxtjs.org/faq/github-pages/#deploying-to-github-pages-for-repository) (it's just a trick to not "crash" the app in local environment execution)