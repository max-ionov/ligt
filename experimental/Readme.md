
# Sandbox for developing the next version (v.0.3)

## Modifications

- ligt:subSegment => ligt:hasSubSegment
  must be rdfs:subPropertyOf nif:superString
- Ligt v.0.3 elements should *not* be nif:Strings, but as data structures independent from strings
  This can be done my either:
  - powla:Node (http://purl.org/powla/powla.owl)
  - oa:Annotation (with oa:target being the utterance and oa:body being the annotation, https://www.w3.org/TR/annotation-vocab/#web-annotation-ontology)
  - the consolidated linguistic annotation vocabulary currently developed by LD4LT (https://github.com/ld4lt/linguistic-annotation)
- Utterances can remain nif:Strings
- Inventory of typical annotations (e.g., ligt:gloss, ligt:morph, etc.)
