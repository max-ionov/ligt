Generalizing over FLex RDF and Xigt
===

Data, concepts
---

	xigt:xigt-corpus ~ flex:document

This one is obvious

	xigt:igt ~ flex:phrase rather than flex:interlinear-text ?

This is actually problematic, because Xigt IGTs seeem to be glossed utterances (FLex "phrase") rather than coherent glossed texts.
FLex interlinear text (a full text) and FLex paragraph (a group of glossed "phrases") are thus missing in Xigt.
	
	xigt:item covers flex:word and flex:morph and other possible segments

In principle, FLex RDF allows different morph segmentations and thus resembles xigt:item. However, this does not seem to be intended and words receive a special status.
The problem is that next properties are defined within a tier in Xigt, in FLex, they're type-bound.
	
	xigt:tier ~ FLex (datatype) properties?

FLex does not have the concept of tiers. Instead, paragraph, phrase, word and morph are hard-wired segment types that may carry different (datatype) properties. In Xigt, every single datatype property would constitute a novel tier.

Xigt is tier-based, FLex is segment-based. The contradiction is hard to resolve, in particular if tiers can be assigned their own metadata (which they cannot directly in FLex RDF).
One way of giving FLex datatype properties tier metadata would be to assign the Xigt metadata to the FLex properties.
However, this is risky as we must not conflate metadata assigned to the same property/tier in different graphs/data sets.

Xigt has been designed for reversible IGT parsing. This means that it provides standoff mechanism that refer to segments and annotation values rather than providing them. In Xigt RDF, these are resolved, but xigt:content and xigt:alignment are preserved. In the generalization, these are no longer necessary. They should not be deleted, though, as they cannot be easily reproduced. But they provide xigt-specific information and do not need to be represented in the overarching model.

In the generalization, we can provide explicit tiers, but merge tiers that are defined by @alignment (they use the same segments).
flex:hasMorph and flex:hasWord can then be represented by nif:subString. The beauty of this approach is that flex:hasMorph does not need to be inferred for Toolbox, but that it can remain as it is (albeit limited in its usability).

In line with Toolbox, we can abandon the general differentiation between Words and Morphs but preserve the alignment via nif:subString where known.

Metadata
---
This is complicated: Xigt incorporates full XML fragments (currently for OLAC), so we need to allow this as an option in the generalization.
The reified metadata from Xigt actually makes sense for FLex media, but it seems like overkill for "simple" datatype properties such as flex:begin-time-offset.

Suggestion:
use RDF reification to express the complex Xigt metadata and the more transparently structured FLex metadata. This will keep the model simple but retain its expressivity. While RDF reification leads to non-decidability, this is not actually a problem here because we're mostly interested in searches using SPARQL. With SPARQL Update, we can always restore the unreified version.