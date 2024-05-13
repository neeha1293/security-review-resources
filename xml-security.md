# XML Parsing

## Java
Java parsers have XXE enabled by default, so we must always explicitly disable it.

Java parsers: 

DocumentBuilderFactory 
SAX parsers (SaxParserFactory, SAXReader, etc)
DOM4J
DOM Parser
TransformerFactory
Validator
SchemaFactory
XMLReader

## Safe XML configuration: 

```xml
dbf.setFeature('http://apache.org/xml/features/disallow-doctype-decl', true);
xmlInputFactory.setProperty(XMLInputFactory.SUPPORT_DTD, false);
domParser.setAttribute(DOMParser.EXPAND_ENTITYREF, false);
validator.setProperty(XMLConstants.ACCESS_EXTERNAL_DTD, "");
reader.setFeature("http://xml.org/sax/features/external-parameter-entities", false);
saxReader.setFeature("http://xml.org/sax/features/external-parameter-entities", false);
```

## Python

Python parsers:

xml.etree.ElementTree
xml.dom
xml.dom.minidom
xml.dom.pulldom
xml.sax

All these parsers are vulnerable to DDos through entity expansion (a billion laughs, quadratic blowup). 
They are safe from external entity expansion, dtd retrieval. 

