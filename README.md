
# Ligt

Ligt is a native RDF vocabulary for representing linguistic examples as text with interlinear glosses (IGT) in a linked data formalism. 

Interlinear glossing is a notation used in various fields of linguistics to provide readers with a way to understand linguistic phenomena and to provide corpus data when documenting endangered languages. This data is usually provided with morpheme-by-morpheme correspondence which is not supported by any established vocabularies for representing linguistic corpora or automated annotations. Interlinear Glossed Text can be stored and exchanged in several formats specifically designed for the purpose, but these differ in their designs and concepts, and they are tied to particular tools, so the reusability of the annotated data is limited. To improve interoperability and reusability, we propose to convert such glosses to a tool-independent representation well-suited for the Web of Data, i.e., a representation in RDF. Beyond establishing structural (format) interoperability by means of a common data representation, our approach also allows using shared vocabularies and terminology repositories available from the (Linguistic) Linked Open Data cloud. We describe the core vocabulary and the converters that use this vocabulary to convert IGT in a format of various widely-used tools into RDF. Ultimately, a Linked Data representation will facilitate the accessibility of language data from less-resourced language varieties within the (Linguistic) Linked Open Data cloud, as well as enable novel ways to access and integrate this information with (L)LOD dictionary data and other types of lexical-semantic resources. In a longer perspective, data currently only available through these formats will become more visible and reusable and contribute to the development of a truly multilingual (semantic) web. 

## Acknowledgements
Ligt is primarily developed in the project [Linked Open Dictionaries (LiODi)](http://acoli.informatik.uni-frankfurt.de/liodi), funded as an independent research group in the eHumanities programme of the German Federal Ministry of Education and Science (BMBF, 2015-2020).

## History

* 2019-05-21 migration to GitHub (MI)
* 2019-03-25 validation (CC)
* 2018-01-18 ligt 0.2: extensions to represent non-coherent groups of examples (MI)
* 2018-01-12 introduction of ligt:UtteranceSet; now not only coherent texts can be modeled (MI)
* 2017-03-25 ligt:Document *rdfs:subClassOf* ligt:Element (CC)
* 2017-03-18 ligt 0.1: initial RDFS formalization (CC)

## Contributors

* CC - Christian Chiarcos, christian.chiarcos@web.de
* MI - Max Ionov, max.ionov@gmail.com

## References

	@InProceedings{chiarcos_et_al:OASIcs:2019:10367,
	  author =	{Christian Chiarcos and Maxim Ionov},
	  title =	{{Ligt: An LLOD-Native Vocabulary for Representing Interlinear Glossed Text as RDF}},
	  booktitle =	{2nd Conference on Language, Data and Knowledge (LDK 2019)},
	  pages =	{3:1--3:15},
	  series =	{OpenAccess Series in Informatics (OASIcs)},
	  ISBN =	{978-3-95977-105-4},
	  ISSN =	{2190-6807},
	  year =	{2019},
	  volume =	{70},
	  editor =	{Maria Eskevich and Gerard de Melo and Christian F{\"a}th and John P. McCrae and Paul Buitelaar and Christian Chiarcos and Bettina Klimek and Milan Dojchinovski},
	  publisher =	{Schloss Dagstuhl--Leibniz-Zentrum fuer Informatik},
	  address =	{Dagstuhl, Germany},
	  URL =		{http://drops.dagstuhl.de/opus/volltexte/2019/10367},
	  URN =		{urn:nbn:de:0030-drops-103672},
	  doi =		{10.4230/OASIcs.LDK.2019.3},
	  annote =	{Keywords: Linguistic Linked Open Data (LLOD), less-resourced languages in the (multilingual) Semantic Web, interlinear glossed text (IGT), data modeling}
	}
