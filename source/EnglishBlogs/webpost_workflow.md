
# Welcome to MyDocs



This site hosts some of my blogs written both in Egnlish and Chinese. 


This document is written in markdown and curated by MkDocs, for full documentation visit [mkdocs.org](https://www.mkdocs.org).

# English Blogs


## Markdown documentation, publish tools & workflows

 
14:10 Monday, December 13, 2021
 
I have been searching a lightweith, scablable and easy-to-use documentation method for around half a year since I finished my 150+ page-dissertation and wrote many other personal notes using Microsft Word. Previously, I searched and tried a few notetaking tools such as Roam, WorkFlowy, Evernote which didn't work out quite well for me. In fact, I sticked with Word and picked up OneNote, Notion, TheBrain to write notes, organize personal plans and projects. These tools works quite well for me at the beginning, but after I accumulated more data and records (e.g. seveal documents with 1000+ pages), Word and Notion begin to struggle with performance and scability issues. Additionally, word files and formats usually can't be coverted into html files in a straitforwad way, so another headache creeps in when I think about disseminating part of these written materials in my personal website on-line. I relize it is time to find an alternative. 

Initially, I tried to write light-weight documents using Markdown(md). But they were not very appealing to me immediately, because I missed some key features like table of cotents, navigation structures offered by what-you-see-is-what-you-get applications(e.g. Microsoft Word). Nonetheless, later on, when I browsed many extensive long structured documents/manuals originally written in md for open source projects, I reallized it would be a good solution to my problem too. These documents could either be hosted on-line in Github or  viewed locally, and they can also be compiled as HTML files to read and share.    

So I fall back on md and start to learn these enabling tools for md documentation. At this moment, I am experimenting with some tools and trying to set up efficient workflows. For local documentation, I now decide to pick up [Obsidian](https://obsidian.md/) which I abodoned before. For on-line publication, I firstly try to use [sphinx](https://www.sphinx-doc.org/en/master/) , it is not long before I find that [MkDocs](https://www.mkdocs.org) has similar functionalities but with more simpler md syntax and easier configuration. There is a more detailed article [StructuredText vs. Markdown for technical documentation](https://eli.thegreenplace.net/2017/restructuredtext-vs-markdown-for-technical-documentation/) and [reStructuredText ??? Markdown ????????????](https://www.readinghere.com/blog/restructuredtext-vs-markdown/). In the following sections, I will share the most useful tips and workflows I have used so far. 

### Markdown vs reStructuredTExt 

Markdown syntax is simple and used widely. By comparision,  reStructuredTExt is more powerful and uniformed. Sadly, these two are not fully compatible. 


TODOs: add some comparision between makrdown and reStructuredText

- [markdown guide](https://www.markdownguide.org/getting-started/)
- [reStructuredText](https://docutils.sourceforge.io/rst.html)
- [reStructuredText syntax reference ](https://docutils.sourceforge.io/docs/user/rst/quickref.html)
- [Markdown and reStructuredText](https://gist.github.com/dupuy/1855764)
- [tools for creating documentataion in reStructuredText](https://docs.acumos.org/en/elpis/docs-contributor-guide/rst-dev-tools.html)


### Markdown 

#### Publish md documents on Github repository using MkDocs

With MkDocs, all the md documents can be viewed locally on your browser. More attractively, they can be easily pushed to your Github repository and to be viewly publicly on a website as manuals or blogs as well. Actually all the contents of this website are initially witten in md, and then converted to HTML by MkDocs. How handy and fantastic it is!

To fully benefit from this feature,  firstly create a repositrory on your github account and clone it into your local computer. Starting from the local folder magic can happen soon, and you just execute the following commands or follow the instructions from [mkdocs.org](https://www.mkdocs.org/getting-started/):
```
* `mkdocs new .` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server, and view it at http://127.0.0.1:8000/ in your browser
* `mkdocs build` - Build the documentation site.
* `mkdocs gh-deploy` - upload your local documents to your remote repository on github and publish there. 
```

As one of the drawbacks of md documents compared with reStructureText, it is not handy to generate a hierarchial table of contents especially when you have extensive documents. The way to generate a table of content (TOC) is not uniformly specified in the syntax, so it is often problematic when you switch between md processing applications.

Though in MkDocs, there is a way to customize your website/file structure by [edit the yml configuration file](https://www.mkdocs.org/user-guide/writing-your-docs/), it would be very labourous if you have to adjust the structure of many different pages or sections by hand. 

In summary, MkDocs is a very convenienvet tool to deploy a simple website hosting limited number of pages. Nonetheless, if there is no automatic way to generate TOC, and it would be difficult to set up the hierarchial structure when you have a lot of md files. 


#### Local documentation with Obsidian
When work on md files localy, I use Obsidian to process and manage them. TOC has a direc reflect of your directory struture within one vault, which is a term/method used by Obsidian to curate an independent and standalone repository. This feature is pretty neat enough if you learn to use folder structure and naming appropriately. 

Two usefule tips:
```
- [[]] # internal link
- #tools #  the tag
```

To learn more instructions on how to use obsidian, check out at [obsidian workflow](https://www.youtube.com/watch?v=Ewhfok91AdE) . 


#### Publish md documents on Github repository using Jekyll
[Github Docs](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll)


### reStructuredTExt 
#### Publish reStructuredText on Github repository with Sphinx 
TODOs: 
 - add more instructions on how to use [sphinx](https://www.sphinx-doc.org/en/master/index.html).
 - local editing of rst files.
 - publish on github. read the docs


after running the command below:

```
$ sphinx-quickstart
```


You can use [Markdown using MyST](https://myst-parser.readthedocs.io/en/latest/using/intro.html) and reStructuredText in the same Sphinx project. We support this natively on Read the Docs, and you can do it locally:
```pip install myst-parser```

Then in your `conf.py`:

```extensions = ['myst_parser']```

## Pipelies to update and publish the document
TODOs: add more instructions on how the workflow is like. 

- [Read the Docs tutorial](https://docs.readthedocs.io/en/stable/index.html)
- [Read the Docs](https://readthedocs.org/)


