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
  * The grouping of the portfolios and the metadata common to all the portfolios are handled by the electronic service, which are contained within collections, which handles metadata applicable to the group as a whole
  * Collections have MARC records, but these are rarely used and can be hidden in Primo results

#### Collections

#### Electronic Services
* Configuration changes that should trickle down to all portfolios in a collection, like enabling the proxy, are made in the electronic service
* The tool for uploading spreadsheets for bulk updates is part of the electronic service's portfolio list

#### Portfolios

#### Title Records
* The 001/primary key is called the MMS ID
* Aleph SYS number have been saved in the 998 field
  * Related: Field "Record Number" *in titles or portfolios?* seems to be "Aleph" in parentheses, the BIB SYS, and the Aleph bucket it came from (UXU01, UXU60, ect.)
  * Presenter indicated that PDA01 BIBs may be labeled as something else

### E-Resource Management

#### Updating Portfolios in Bulk
1. Download the Extended Export of the collection's portfolio list
2. Delete columns BO-BQ, replace with single column "OWNERSHIP"
3. Delete columns CO-CQ
4. Delete column CP
5. Activate portfolios by changing column `LOCALIZED` from `N` to `Y`
**Question:** How can portfolios be bulk deleted? Changing `LOCALIZED` doesn't work.
6. Make changes to portfolios by changing the following columns
   * `FROM_YEAR`: holdings start year as YYYY; change `COVERAGE_STATEMENT`
   * `TO_YEAR`: holding end year as YYYY; change `COVERAGE_STATEMENT`
   * `FROM_MONTH`: holdings start month as MM; change `COVERAGE_STATEMENT`
   * `TO_MONTH`: holding end month as MM; change `COVERAGE_STATEMENT`
   * `FROM_DAY`: holding start day as DD; change `COVERAGE_STATEMENT`
   * `TO_DAY`: holding end day as DD; change `COVERAGE_STATEMENT`
   * `PUBLICATION_DATE_OPERATOR`: `>` for an embargo, `<` for a moving backfile paywall
   * `PUBLICATION_DATE_YEAR`: number of years in the embargo/paywall
   * `PUBLICATION_DATE_MONTH`: number of months in addition to the number of years in the embargo/paywall
   * `ACCESS_TYPE`: `Current`, `Perpetual`, or `Current, Perpetual`
   * `PROXY_ENABLE`: `true` to enable the proxy, `false` to disable it; requires changing `PROXY_LEVEL` to `PORTFOLIO`
   * `PROXY_SELECTED`: the proxy to use, where `Default` will select the default; requires changing `PROXY_LEVEL` to `PORTFOLIO`
   * `COVERAGE_STATEMENT`: options `Only global`, `Only local`, `Global and local`, `Global or local`
   * `LICENSE`: **Question:** Can licenses and portfolios be linked in bulk by adding the license code here?
7. Reorder the columns so all the empty columns are at the end
8. Save the Excel file
9. Edit the collection's electronic service, then go to the Portfolios tab
10. Click "Load Portfolios"
11. In the wizard, select the Excel file and "Update portfolios" from the actions list
12. Click "Next"
    * If there's a validation error, a copy of the uploaded file with the same name and a new column A with the type of validation error will be available for download
    * Content included in the download may prompt a validation error on upload
13. Review the changes to be made by downloading the spreadsheet (which will have the same name as the uploaded file, so both can't be open at the same time)
14. Click "Next"


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
