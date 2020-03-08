# intranet-search-cockpit

Intranet search cockpit. Coperate Intranet search is not plug-and-play.

## Introducion

[Content Repository](https://en.wikipedia.org/wiki/Content_repository): A content repository or content store is a database of digital content with an associated set of data management, search and access methods allowing application-independent access to the content, rather like a digital library, but with the ability to store and modify content in addition to searching and retrieving. 

[Intranet](https://en.wikipedia.org/wiki/Intranet): An intranet is a computer network for sharing information, collaboration tools, operational systems, and other computing services only within an organization, and to the exclusion of access by outsiders to the organization. The term is used in contrast to public networks, such as the Internet.


In most coperate intranets there are several content repositories.

This has the drawback, that users don't have **one** search interface.

Internet search is easy: Just use ecosia or bing. But coperate Intranet search is .... (please send me your favorite term via mail: guettli.intranet-search-term@thomas-guettler.de)

## Two Options

* Option1: Constantly index the content repositories in background. The search gets executed on the own index.
* Option2: Use the search API of the content repositories. No own index exists. The result of N systems gets displayed on one page.

## Tools

### Indexing + DB (low-level) (Option1)

* [solr](https://lucene.apache.org/solr/)
* [elasticsearch](https://www.elastic.co/de/elasticsearch/)
* [django fulltext](https://docs.djangoproject.com/en/3.0/ref/contrib/postgres/search/)

[Trend comparing above tools](https://trends.google.com/trends/explore?date=all&q=%2Fm%2F02qd9s1,%2Fm%2F0h64sgb)

[Stackoverflow Tag-trend of above tools](http://sotagtrends.com/?tags=solr+elasticsearch)

Detecting which pages have changend: [RSS](https://en.wikipedia.org/wiki/RSS)

### High level

* [manifoldcf](http://manifoldcf.apache.org/en_US/index.html#What+Is+Apache+ManifoldCF%3F) looks dated.
* [opensemanticsearch](https://www.opensemanticsearch.org/) Community project or one-man-show? [github contributors](https://github.com/opensemanticsearch/open-semantic-etl/graphs/contributors) [Contact](https://opensemanticsearch.org/contact)
* [List of open source Enterprise Search Software](https://en.wikipedia.org/wiki/List_of_enterprise_search_vendors#Free_and_open_source_enterprise_search_software)

## List of Content Repositories

Examples:

* [github](//github.com)
* [confluence](//www.atlassian.com/software/confluence)
* [Staffbase](//staffbase.com)
* [Stackoverflow Team](https://stackoverflow.com/teams)

## Goals

* Provide **one** search interface for several content repos.
* Every search should get logged. This allows to understand the employees needs and improve the search results in the future. (Build-Measure-Learn feedback loop)

## Stretch Goals

* Extend knowledge of a content repository. Example: In the coperate intranet the definition of [Scrum Master at Wikipedia](https://en.wikipedia.org/wiki/Scrum_(software_development)#Scrum_master) can get extended by local annotations. These local annotations provide additional details how to apply the general (world wide) knowledge to the particular ??? inside the company.


## Cockpit

Good search results don't fall from the sky. You need a way to point the non-intelligent indexers into the right direction.

* Configure Content Repositories. Store credentials. GUI to add new repos
* A way to add hints to the non-intelligent indexers. I guess this is needed, since there are not enough hyperlinks between the documents to get a solid [PageRank](https://en.wikipedia.org/wiki/PageRank)

## Related

* [Content Management Interoperability Services](https://en.wikipedia.org/wiki/Content_Management_Interoperability_Services) (looks dated: [Trend](https://trends.google.com/trends/explore?date=all&q=%2Fm%2F04lgyys))
* [invotra enterprise search](https://invotra.com/features/enterprise-search/)

## ETL

[ETL](https://en.wikipedia.org/wiki/Extract,_transform,_load): In computing, extract, transform, load is the general procedure of copying data from one or more sources into a destination system which represents the data differently from the source(s) or in a different context than the source(s). 

* [ETL of opensematic](https://opensemanticsearch.org/dev/enhancer)

## Authentication Libs
* [libsaas (Python)](http://ducksboard.github.io/libsaas/) unmaintained.


## Content Repos

### Confluence

* [RSS Feed docs](https://confluence.atlassian.com/confcloud/subscribe-to-pre-specified-rss-feeds-724765361.html)

### Github

* [Github Feeds API](https://developer.github.com/v3/activity/feeds/)
* [PyGithub Python Client](https://github.com/PyGithub/PyGithub)

### Stackoverflow Teams

* [StackExchange RSS Feeds docs](https://meta.stackexchange.com/tags/rss/info)

### Change Name?

"Intranet" is dead. We don't own servers, we don't run a corporate network. It is about searching corporate Saas pages. Alternatives: multi-saas-search, SaaSRank, SaaS-Umbrella, ...

## Later

### Platform

Make it easy to add new SaaS sites and authentication methods. Add "platform" to the name.

