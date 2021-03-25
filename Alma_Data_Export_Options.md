# Alma Export Options
This is a listing of the export options in Alma and the output when used on different types of sets.

## Bibliographic Export Job as XML
*Binary outputs .mrc*
- Set of "All Titles" > MARCXML BIB records
- Set of "Electronic Titles" > MARCXML BIB records

## Portfolio Export Job as XML
- Set of "Electronic Titles" >
  - MARC title fields
  - ISBNs
  - Resource type
  - Resource as print or electronic
- Set of "Electronic Portfolios" >
  - MARC title fields
  - ISBNs
  - Resource type
  - Resource as print or electronic

## URL Export Job as CSV
- Set of "Electronic Titles" >
  - Resource Type *[all "Bibliographic Record"]*
  - ID *[resource MMS]*
  - URL
- Set of "Electronic Portfolios" >
  - Resource Type *["Bibliographic Record" or "Portfolio"]*
  - ID *[for the resource: MMS for BIBs, Portfolio ID for portfolios]*
  - URL

## Export Search Results as Excel
- Set of "Electronic Portfolios" >
  - title *[at beginning and end of CSV; think it's MARC 245]*
  - Name *[unsure of source]*
  - ProQuest purchase model
  - ISBN
  - ISBN (13)
  - ISSN
  - Coverage
  - Perpetual Coverage
  - Collection Library
  - Access Type
  - Electronic Material Type
  - Creation Date
  - Modification Date
  - Managed by
  - Electronic collection COUNTER Platform
  - Orders
  - Peer Reviewed
  - Portfolio ID
  - Service ID
  - Collection ID
  - MMS ID
  - COUNTER Platform
  - underReview
  - Availability
  - resultFromNetwork
  - Open Access
  - Library
  - Notes
  - Related Portfolios
  - View It
  - [null] *[the penultimate column of the CSV has a null value in row 1]*