SortOrder: 0
# Site List

Site list is a service that retrieves sites related information for a given account.

## About The API
The Site List functionality is exposed via 
[SiteListServiceV2](https://github.com/wix-private/sites-list/blob/master/sites-list-proto-api/src/main/proto/com/wixpress/sitelist/api/sites-list-service.proto) service.

-- todo: add the relevant imports from node and scala

### The Site object
The returned [Site](https://github.com/wix-private/sites-list/blob/master/sites-list-proto-api/src/main/proto/com/wixpress/sitelist/api/site.proto) object consists of the following properties:
* id
* htmlWebId
* name
* displayName
* createdDate
* trashedDate
* published
* premium
* viewUrl
* editUrl
* thumbnail
* ownerId
* contributorIds
* editorType
* blocked
* folderId
* namespace

### Filters
Both `Query` and `Count` APIs accepts the following filters:
* folderId
* editorType
* appDefIds
* premium
* published 
* namespace
* name
* state
* hasConnectedDomain

## Under the hood
Site list service fetches all data from [meta-site-search](https://bo.wix.com/wix-docs/rest/meta-site/meta-site---meta-site-search).
