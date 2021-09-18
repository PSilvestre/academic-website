---
title: Hello World!
subtitle: An introduction to the website

# Summary for listings and search engines
summary: An introduction to the website and what we will be doing. Paper reviews, tech ideas and such.

# Link this post with a project
projects: []

# Date published
date: "2021-03-08T00:00:00Z"

lastmod: "2021-03-08T00:00:00Z"

draft: false

featured: true

image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/K7JEYFDictM)'
  focal_point: ""
  placement: 2
  preview_only: false

authors:
- admin

tags:
- Academic
- Hugo

categories:
- Meta


bibFile: content/post/hello-world/bib.json 
---

## About this website

I built this website quite easily using [Hugo](https://gohugo.io/), a fantastic static website generator.
Static websites have many advantages which we have been rediscovering over the years, one of them being the ease of deployment. 
The last time I built a website I went the route of designing a flexible webapp, using Angular for the frontend, Spring boot for the backend and MariaDB for storage. 
Deploying it thus involved setting up at least three seperate components, and connecting them to each other, for something which would have maybe 5 visits a year. 
Static sites on the other hand, can be served from any number of hosting services, or you can quickly set-up an Apache webserver and point it to the generated directory.

While it was exactly what I was looking for at the time, the website I built was not much different from what I just created in a couple hours with Hugo.
It had a homepage with some basic bio information, a blog section and tags for searching. It also had authentication and authorization, and users with the "writer" role could submit posts in LaTeX, which would be compiled to HTML.
I thought it was a cool concept at the time, but really Markdown is a much better fit. Hugo allows users to write posts in Markdown, and these get compiled into HTML later on. This is a much more "declarative" way of generating content.

Hugo has a bunch of pre-built themes for many different purposes. One of these themes is the "Academic" theme, which as you may be able to guess was designed to help build webpages for academics.
This theme further speeds up the creation of such a page, by bringing in many useful pre-built widgets, styling and formatting. For example, I took the route of cloning their example project, and then removing features until I was happy with the result.
One of the downsides of using the Academic theme is that there are many pages sharing the same design. Your webpage is not unique. Not at all, as this is a very popular project nowadays.

As far as I was able to tell, there isn't much you can easily do to set your page apart.
You can tweak fonts, color themes (I built my own based off of the [Nord](https://www.nordtheme.com/docs)),
and declaratively decide to include some information, but they all end up "feeling" the same. I think this is mostly due to the biography component, which I will attempt to change in the near future.

In any case, Hugo + Academic has many other advantages. For example, built in support for math formulas and diagrams. I will now include a number of examples of interesting features, both for you dear reader and for living documentation which I can look at later.

#### To-do lists

Left to do on this set of examples:
- [x] Write math example
  - [x] Write diagram example
- [ ] Do something else

#### Math

Both in-line math $ \lambda f . (\lambda x) . (f (x x)) (f (x x)))$ and block math as per below:

$$ \forall e : \square ((|Log(e)| \leq f) \implies \\\\
((Depend(e) \subseteq Log(e)))) $$


#### Code

Code highlighting is also supported with little configuration. Here is an example from a personal project:
```python
    def simulate_system(self):
        ms_per_update = Decimal(1000 / self.fps)
        current_milli_time = lambda: Decimal(round(time.time() * 1000))
        previous = current_milli_time()
        lag = Decimal(0.0)

        while self.running.is_running():
            current = current_milli_time()
            elapsed = Decimal(current - previous)
            previous = current
            lag += elapsed

            while lag >= ms_per_update:
                self.step(ms_per_update / 1000 / 60 * self.time_multiplier)
                lag -= ms_per_update

            time.sleep(ms_per_update / 1000 / 4)
```

#### Academic citations

Now one thing that strangely is not supported is quoting academic work of other authors. You may import your own work and reference it, but using something like Bib is not implemented.
I had to rely on an external project, namely [hugo-cite](https://github.com/loup-brun/hugo-cite) to provide this. 
Installation was not straightforward, but luckily this [github conversation](https://github.com/wowchemy/wowchemy-hugo-modules/issues/830#issuecomment-753782484) has some answers.
Unfortunately however, this project currently only supports citing in APA style. Furthermore, one must export citations to CSL-JSON format, which is a messy workflow for me, as I do not use a normal reference manager like Zotero or Mendeley.
In any case, here is an example with one of my favourite survey papers {{< cite "elz" >}}. Check the end of this post for the bibliography.

## What am I doing here?

So, I have set all this up, what am I using it for?

Well, currently, I plan on writing paper reviews/summaries on any eye-opening papers. I may also just write about some of my areas of interest, as I have found this to help me greatly in organizing information in my hand.
Topics to expect go from pure distributed systems (consensus, DHTs, rollback recovery, fault-tolerance), database systems (storage engines, query compilation, transactions and distributed transactions) and stream processing systems (architectures, delivery guarantees and future directions).
I may also blog about any interesting projects I get into for fun, such as my Raspberry Pi cluster or cross-discipline simulation framework (built in collaboration with chemical engineering students).

Expect a post on the internals of a modern Stream Processing Engine distributed runtime, such as threading model, memory management, processing and fault-tolerance.

## Cited Bibliography
{{< bibliography cited >}}
