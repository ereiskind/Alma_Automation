# About Alma

## The Zones: Institution, Network, Community
* Alma divides the space where resource records are available into three zones
  * The institution zone (IZ) is for the school (FSU, not FSU Libraries)
  * The network zone (NZ) is for the consortium
  * The community Zone (CZ) is effectively the knowledgebase
* Consortially purchased resources will be managed by FALSC/FLVC in the NZ and will only appear in Alma searches that include the NZ
  * Joint licenses will be managed by each institution in their IZ
  * **Question:** Can licenses be shared IZ to IZ within NZ (as in the SUS-negotiated licenses—we upload and push out to everyone)?

## E-Resources

### E-Resource Record Structure
* Records for individual resources in Alma are made of two parts: the title and the portfolio
  * Titles are the bibliographic MARC records
  * Portfolios are for the individual instances of the resource (roughly the FRBR item)
* Portfolios are grouped into collections
  * Collections also have MARC records, but these are rarely used and can be hidden in Primo results

#### Collections

#### Portfolios

#### Title Records
* The 001/primary key is called the MMS ID
* Aleph SYS number have been saved in the 998 field
  * Related: Field "Record Number" *in titles or portfolios?* seems to be "Aleph" in parentheses, the BIB SYS, and the Aleph bucket it came from (UXU01, UXU60, ect.)
  * Presenter indicated that PDA01 BIBs may be labeled as something else

### E-Resource Management

## ERMS Functionality

### Vendors and Vendor Records
* Vendors can have three roles
  * Material suppliers: organizations that get paid for resources
  * Access providers: organizations responsible for platforms providing access
    * Only vendors with the access provider role can have interfaces (platforms/websites) added to their vendor record
  * Licensors: organizations connected to licenses
* PO lines can be connected to material suppliers or access providers
* Vendor accounts are shared by the institution
  * Material suppliers contain account records; those will be unique to the different purchasing entities on campus

## Primo


# Unorganized
•    Ways of activation
o    In task list because of PO line
o    Community zone, don’t add library, activate, find via IZ portfolio search, create e-activation task
•    Activate individual portfolio: find collection in CZ, go to portfolio list, click activate on portfolio, don’t add library
•    In task list
o    Edit resource
    Add proxy
•    Interface: “misc. ejournals” includes individual journal interfaces

# Questions:
* Do portfolios have underlying MARC?
* What's the point of attachment between resoruces and orders (portfolio to PO line?)?
* Indicating perpetual access rights for serials
* Alma defines an e-resource standing order as one where we lose access when payment stops (Alma Essentials video); does this mean subscriptions with perpetual access agreements can’t be established as standing orders?
## Primo Qs
•    Why did the ebooks in the first look share the label “book” with the print books? Is this something that can be changed? In demo, even presenter couldn’t tell between print and e in search results.
•    For links, what’s in View Online and what’s in Other Links?
•    What prompts BIBs to get FRBRized into a “Multiple Versions” search result?
•    “Expand my results” as way to get content we don’t have full-text access to—is this text we can change?
•    Are all loaded MARC records returned by “Library Catalog”?
## Own implementation Qs
•    Are we going to set up Gobi ordering within Alma?
•    Can Primo pull user access model info from the PO line record? If upgrades are/can be done by attaching multiple PO line records to a single portfolio, can Primo pull user access model info from the most recent of those records?
•    Do we intend to connect the BIB/HOL/item and collection/portfolio infrastructures in any way? If so, how?
•    Can the EOD (embedded order data) that can be added to an uploaded MARCXML file to automate the creation of records related to purchasing and invoicing be manually constructed (that is, added to a MARC file that came from the vendor without EOD)?
•    The record import example showed “files with records matching one or more existing records in Alma” as an import issue that needed manual resolution; what relation does this have to a record overlay system? (Does this mean an automated record overlay process where one exact match is found cannot be done?)
•    Auto loading of holdings can be configured for Ebook Central—do we want to do this?
•    How will we determine what A&I content will be marked as discoverable from KB (what they call CDI)?
•    How will we handle selecting resources outside the book/journal/database categories in the CDI?
•    
