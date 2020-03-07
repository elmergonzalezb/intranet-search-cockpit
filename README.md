# intranet-search-cockpit

Intranet search cockpit. Sorry, Intranet search is not plug-and-play. You need a cockpit.

## Introducion

[Content Repository](https://en.wikipedia.org/wiki/Content_repository): A content repository or content store is a database of digital content with an associated set of data management, search and access methods allowing application-independent access to the content, rather like a digital library, but with the ability to store and modify content in addition to searching and retrieving. 

[Intranet](https://en.wikipedia.org/wiki/Intranet): An intranet is a computer network for sharing information, collaboration tools, operational systems, and other computing services only within an organization, and to the exclusion of access by outsiders to the organization. The term is used in contrast to public networks, such as the Internet.


In most coperate intranets there are several content repositories.

This has the drawback, that users don't have **one** search interface.

Internet search is easy: Just use ecosia or bing. But Intranet search is .... (please send me your favorite term via mail: guettli.intranet-search-term@thomas-guettler.de)

## Two Options

* Option1: Constantly index the content repositories in background. The search gets executed on the own index.
* Option2: Use the search API of the content repositories. No own index exists. The result of N systems gets displayed on one page.

## Tools

### Indexing (low-level) (Option1)

* [solr](https://lucene.apache.org/solr/)
* [elasticsearch](https://www.elastic.co/de/elasticsearch/)

[Trend comparing above tools](https://trends.google.com/trends/explore?date=all&q=%2Fm%2F02qd9s1,%2Fm%2F0h64sgb)

### High level

* [manifoldcf](http://manifoldcf.apache.org/en_US/index.html#What+Is+Apache+ManifoldCF%3F)
* [opensemanticsearch](https://www.opensemanticsearch.org/)

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

## Related

* [Content Management Interoperability Services](https://en.wikipedia.org/wiki/Content_Management_Interoperability_Services) (looks dated: [Trend](https://trends.google.com/trends/explore?date=all&q=%2Fm%2F04lgyys))


