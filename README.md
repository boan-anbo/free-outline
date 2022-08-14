# free-outline
A combination of TO with Freedraft

# Components:

## Backend

### 0. Data importer: 
- Given an external data source, convert it to TO.

1. PDF:

PDF Extractor and importer: PDF Annotation Card

2. Zotero:

Zotero exporter, plugin to send data directly to the interface

3. WebPage



### 0. TO types: TO, see [Textual objects](https://textual-object.com/)



### 1. TO parser, which convert TO markup from plain text to TO tickets (TOT).

### 2. TO data provider: 
  - non-agnostic data source to provide JSON-format collection of TOs (TOC). Could be sqlite, plain json file, etc.
  - should be written in different languages with system access, e.g. javascript for VsCode, Rust for Tauri

### 3. TO data reader:
  - arguments: 
    1. TO tickets
    2. data source configuration: data source type, url, password etc.
  - returns: TO collection (TOC)
  - 
### 3.1 TO data writer:
  - agnostic
  - given a TO, persist it in a data source
  - return a TOT (TO Ticket), with the information where it was stored. 

### 4. MD parser: parse raw markdown points to rich and structure Point Structure with content.
  - This should be multilayers: i.e. the point structure is stable, but import plain texts are variable
  - E.g. it should be able to process both tex and markdown formats. So the definition of levels etc does not need to follow the example of Markdown. Think of my writing plan parser.

### 5. A central processing unit: 
  - arguments: 
  1. markdown file
  2. json collection of TOs. 
  - returns: TO Markdown Tree (TMT): a structured list of markdown points.

## Interface

1. Standalone Desktop

2. VsCode Plugin

3. Obsidian Plugin.
