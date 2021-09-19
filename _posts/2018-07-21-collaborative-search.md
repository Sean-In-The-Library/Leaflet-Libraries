---
layout: post
title: Collaborative search - an implementation story
thumbnail: "/img/og_searchx.png"
---

Web search is generally seen as a solitary activity, as most mainstream technologies are designed for 
single-user search sessions. However, for a sufficiently complex task, **search collaborations** have shown to be beneficial.


## Existing systems

In one of my projects, **large-scale** collaborations whilst searching (think tens or hundreds of potential collaborators)
are the central focus. When starting this project with [Felipe Moraes](http://www.wis.ewi.tudelft.nl/moraes/) (a PhD student in my team), 
one of the first things we did was looking at existing
collaborative search systems, i.e. search systems that come with some of the typical collaborative search features such
as a chat allowing searchers to communicate, shared bookmarking, a shared query history and so on. 
After all, you can find more than 4000 research papers that mention *collaborative search* on Google Scholar, and some of them are dedicated solely to the description of collaborative search systems.
So, someone must have implemented a collaborative search system that is (1) open-sourced and (2) functioning. Turns out,
there is only one, [Coagmento](http://www.coagmento.org/) that fulfils both of these conditions. The drawback of Coagmento though is the need for client-side installations, either a browser plugin or a mobile app.

Here is an overview of existing systems as described in the literature and ours (```SearchX```), with the implementation dimensions highlighted. The table is taken from our [DESIRES 2018 preprint](../documents/publications/DESIRES2018-Putra.pdf):

<img src="https://chauff.github.io/img/searchx-systems.png" width="900px">


## Needs
The table above is of course a great way to establish the need for a new implementation and so we set out
to implement our own collaborative search system, that should be (1) open-sourced, (2) well documented,
(3) not requiring any client-side installation step, (4) based on modern Web standards and (5) easily configurable
for different experimental settings (e.g. switch the chat on or off, swap in different search engine backends).

Enter two Master students who started working with us on their thesis projects last year 
and happen to be excellent programmers: Sindunuraga Rikarno Putra and Kilian Grashoff. 
With Felipe in the lead, they were able to implement a first version of a 
collaborative search system that fulfilled all our wishes in a relatively short time.
This of course is only the first milestone of more to come - we now have a stable collaborative search system called
```SearchX``` that we can deploy in MOOCs, in crowdsourcing experiments and other scenarios we can think of.


## Publications
Together we wrote a SIGIR demo paper, showcasing the first version of our system ```SearchX```:

```bibtex
@inproceedings{Putra2018a,
 author = {Putra, Sindunuraga Rikarno and Moraes, Felipe and Hauff, Claudia},
 title = {SearchX: Empowering Collaborative Search Research},
 booktitle = {SIGIR '18},
 year = {2018},
 pages = {1265--1268}
} 
```

and a as already mentioned a [DESIRES 2018](http://desires.dei.unipd.it/) prototype paper, explaining in more detail the ups and downs of
the development process:

```bibtex
@inproceedings{Putra2018b,
 author = {Putra, Sindunuraga Rikarno and Grashoff, Kilian and Moraes, Felipe and Hauff, Claudia},
 title = {On the Development of a Collaborative Search System},
 booktitle = {DESIRES '18},
 year = {2018}
} 
```

.... as well as a CIKM 2018 paper where we make use of our system for search as learning experiments. More details in [this blog post](https://chauff.github.io/2018-08-07-sal-at-cikm/). 

## SearchX look and feel
There are many types of search collaborations, we focus on *remote*, *synchronous* and *explicit* collaborations, i.e.
search collaborations where each collaborator has its own device, the collaborators search together at the same time and
are aware of each other's activities. This requires a lot of interface work (some widgets in the search interface have
to be kept synchronized at all times, we need a document viewer to keep logging users' activities on the 
documents themselves, ...) as well as backend work (how do you ensure that the relevance labels of one 
collaborator influence the search result rankings seen by all collaborators). 

Here is the search interface with all implemented features switched on:

<img src="https://chauff.github.io/img/searchx-interface-main.png" width="900px">

As you can see we added quite a few things: chat, shared bookmarks, shared query history, document ratings, number of document views, color coding to provide a sense of which collaborator did what and different verticals (out of the box
we support the Bing API, Indri and Elastic as backends).

Here is the view after clicking on a search result:

<img src="https://chauff.github.io/img/searchx-interface-viewer.png" width="900px">

The built-in document viewer is not only great to tracking users (otherwise we would have no idea of what they are doing once they leave our search result page - often important for interactive IR experiments) but also allows users to annotate
the documents in tandem.

## Demo

If you head over to [http://searchx.ewi.tudelft.nl/search](http://searchx.ewi.tudelft.nl/search) you will see a demo version of our collaborative search system. To check out how well the system works with several collaborators open the same URL in different browsers or a regular browser tab and a private browser tab. Be aware though, that whatever you query for is visible to everyone!

## Available on GitHub

We have open-sourced ```SearchX``` on GitHub: [https://github.com/felipemoraes/searchx](https://github.com/felipemoraes/searchx). 

A big todo item on our list is to include basic authentication mechanisms to enable private collaboration sessions; right now, `SearchX` is a tool mainly for research. 

If you want to try it out and are getting stuck, please contact us, we are more than happy to help!
