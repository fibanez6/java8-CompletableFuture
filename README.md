# The article enricher service

### The task
Our service has been asked to create a new Article Enricher service that produces an article definition containing an article name,  its hero image, and all videos associated with a given article id.

This service will leverage existing APIs to collect this information and return it to the requester.

We're lucky enough to have been given clients for our Article reference and Assets services, so we're not going to need you to implement that.
All we need you to do is to implement the logic of the ArticleEnricher. Please create an implementation for this class that gets all information needed provided the references.


### Solution

[CompletableFutures](https://docs.oracle.com/javase/8/docs/api/java/util/concurrent/CompletableFuture.html)
 is used to resolve this task.


In order to retrieve the image and video ids from urls. It has been considered the last part of the URL path,
which is the name of the content with the extension, as the id of the content. i.e:

if the URL looks like:
```
https://ichef-1.bbci.co.uk/news/1024/cpsprodpb/8F1A/production/_98943663_de27-1.jpg
```
then the id content is:
```
_98943663_de27-1.jpg
```