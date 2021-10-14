SortOrder: 0
# Introduction

The Activity Counters service allows site owners and third-party developers to keep track of Wix site members' activity. For example, counting their:
- comments
- followers
- posts

The service allows public and private counters: 
 - Public counters can be read by any site member.
 - Private counters can only be accessed by the site member who owns the counter.

The Activity Counters API gives third-party developers access to the counters on a site at a per-member, per-app level.

Counters are only activated when a site member actually performs the activity the counter tracks.

This means that the query and list endpoints for this API may return a large number of results, for sites with many members.

## Access

Third-party developers can
 - read (but not set) counts for Wix apps.
 - read **and** set counts for their own apps.

## Initializing a counter

To create a new counter for a third-party app, use the [Set Activity Counters
 endpoint.](https://bo.wix.com/wix-docs/rest/drafts/activity-counters/set-activity-counters)

## Use cases

**Most active writer widget.** 
A developer wants to add a "most active writer" widget to their home page, based on the number of posts each member creates.

1. Get per-member post numbers for blog or forum app using the [Get Activity Counters endpoint.](https://bo.wix.com/wix-docs/rest/drafts/activity-counters/get-activity-counters)
2. Process counts and display in widget.
 
**Most influential member widget.** 
A developer wants to add a "most influential members" widget to his community, based on how many likes and comments each member's posts get.

1. Get per-member reaction numbers for blog/forum app using [Get Activity Counters endpoint.](https://bo.wix.com/wix-docs/rest/drafts/activity-counters/get-activity-counters)
2. Process counts and display in widget.
