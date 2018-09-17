# es-lambda-indexing
AWS elasticsearch cloudwatch lambda indexer

This is a fork off of Amazon's LogsToElasticsearch.  This replaces the script that is created
for you when you use the ```Stream to Amazon Elasticsearch Service``` from within Cloudwatch logs.

### Add functionality beyond Amazon
* Multiple index support.  Needed to support multiple cloudwatch logs to a single ES cluster.

###To Install/Use  
* Enable ```Stream to Amazon Elasticsearch Service``` for cloudwatch logs.
* Find the lambda function with a name that starts with LogsToElasticsearch
* In the editor replace the script code with the code from index.js in this repo
* edit ```var endpoint = 'put_your_search_endpoint_here';``` and put in your ES endpoint.  
**DO NOT** include the **https://** part of the name. example 
```node.js
var endpoint = 'search-logs-34ssdwijjopsef23jsdf44.us-west-2.es.amazonaws.com'
```