# Data Object #
This object represents a data endpoint and the local cache of that data. Each object typically represents a list of one type of model.

## State ##
The data object contains properties that angular scopes can bind to.

- Data Subsets
- Paging Data
- Local Data Set
  
### Local Data Set ###
The current list of raw model objects stored in memory

### Data Subsets ###
A subset of the local data set. Each subset is defined in the object config. and is added to and removed from programatically.

Example:
An implementor sets up a "message inbox" page with a list of messages on the left. The list is based off a data object bound to a /message REST endpoint.

A "starred" subset is set up in the data object config. In each list item, whenever the a star is toggled on, the item is added to the "starred" subset. Another list view on the page is also bound to the same data object, specifically the "starred" subset. This view now displays the newly starred item in it's list.

The data object can have other subsets that directives can bind to, for this example an "unread" subset could be practical.


### Paging Data ###
If a data endpoint supports paging the data object can store this page data and provide methods for updating the page data. This data includes...

- Current Page
- Total Pages
- Page Size


## Functionality ##
To be completed

##Configuration
To be completed