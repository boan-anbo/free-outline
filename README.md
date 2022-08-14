# free-outline
A combination of TO with Freedraft

## Components:

### 0. TO types: TO, see [Textual objects](https://textual-object.com/)

### 1. TO parser, which convert TO markup from plain text to TO tickets (TOT).

### 2. TO data provider: agnostic data source to provide JSON-format collection of TOs (TOC). Could be sqlite, plain json file, etc.

### 3. TO data reader:
  - arguments: 
    1. TO tickets
    2. data source configuration: data source type, url, password etc.
  - returns: TO collection (TOC)

### 4. MD parser: parse raw markdown points to rich and structure Markdown Structure.

### 5. A central processing unit: 
  - arguments: 
  1. markdown file
  2. json collection of TOs. 
  - returns: TO Markdown Tree (TMT): a structured list of markdown points.
