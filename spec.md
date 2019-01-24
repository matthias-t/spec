# Specification

## Meta

This document is a complete specification for StrictYAML, a restricted subset of the [YAML](yaml.org) data serialization format.

### Style

This specification aims to be coherent and minimal without omitting recommendations. Linear reading is not a priority.

## Definitions

### Requirement levels

The key words **must**, **must not**, **required**, **shall**, **shall not**, **should**, **should not**, **recommended**,  **may**, and **optional** in this document are to be interpreted as described in [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt).

### Processors

A *processor* is a tool for converting between streams and native data structures. It is assumed that a processor does its work on behalf of another tool, called an *application*.

### Representations

A *character* is a Unicode character.

This specification defines a syntax for representing structured data as series of characters. Such a series of characters is called a *stream*. Streams contain no implicit or explicit type information.

This specification also defines a data structure representing a stream. This data structure is called a *syntax tree*. The conversion between stream and syntax tree is bijective.

A *schema* defines types inside a data structure.

## Processes

name | input | output | description
-----|-------|--------|-------------
analyze | stream | syntax tree |
deserialize | syntax tree | native data structure |
betype | native data structure + schema | native data structure | parse strings inside native data structures according to a schema provided by the application
detype | native data structure | native data structure | produce strings from elements inside native data structures
serialize | native data structure | syntax tree
present | syntax tree | stream

A processor **should** implement all of the above conversions.

### Analyze

### Deserialize

### Betype

### Detype

### Serialize

*Native data structures* are represented using 3 kinds of *nodes*:
- *list*: an ordered collection of nodes
- *map*: an unordered collection of associations of unique strings to nodes
- *string*: a collection of characters

### Present
