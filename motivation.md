# Goals

StrictYAML aims to be:
- readable by humans
- simple to serialize and to deserialize
- secure
- portable between programming languages

# Removed features

## Typing

In serialized data, implicit or explicit information about types is:
- fallacious: implicit typing may be confusing to non-programmers, who may not understand that a directive needs to be given to the parser to avoid the data being misinterpreted
- superfluous: it’s not necessary if the type structure is maintained outside of the markup
- verbose: two extra characters per string makes the markup longer and noisier

For those reasons, StrictYAML replaces implicit and syntax typing with a type schema defined beforehand by the application. However, StrictYAML preserves three basic primitives to structure the data: maps, lists and strings.
