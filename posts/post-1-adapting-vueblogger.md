# Adapting VueBlogger
## Introduction
I was looking for a simple web site generator to build Blogs and a portfolio, built in Vue so I could learn it. Then I found VueBlogger from Sam Zhang. That's exactly what I need.  
**Big thanks to Sam Zhang: 谢谢你**
           
## Installation
[Download](https://github.com/samzhangjy/VueBlogger/tree/main)

[Instructions](https://samzhangjy.github.io/#/posts/vue-blogger)


## Writing posts
Just add a file under /posts  
Add some reference to it on `/posts/data/posts.json` for example:

```
{
    "posts": [
        {
            "title": "VueBlogger: A simple blogging site for Vue",  // Post title
            "tags": ["Vue.js", "project", "frontend"],  // Post tags
            "cover": "https://dev-to-uploads.s3.amazonaws.com/i/95lvt23xz4ozer5byomi.png",  // Post cover image url
            "des": "There isn't really a simple blogging tool for Vue. VuePress works, but it's to complicated. So for that purpose, I developed this light-weight blogging site for Vue: VueBlogger.",  // Post description
            "date": [  // Post publish date
                2023,  // Year
                12,  // Month
                10  // Day
            ],
            "id": "post-1-adapting-vueblogger"  // Post file name stored under `/posts/`
        }
    ]
}
```

## Adapting the style
To fix the height or the post cover images  
Add that code into `PostCard.vue`

```
.vs-card__img img {
  height: 142px !important;
  object-fit: cover;
}
.vs-card__img .vs-avatar img {
  object-fit: inherit;
}
```

`object-fit: cover` avoid strching of the images  
`object-fit: inherit` reset the status for the avatar

## Changing the favicon
The favicon should be placed under `/public`, then change the reference on the file `/public/index.html`  
```<link rel="icon" href="/favicon.ico">```