# DHARMA List of Elements for Critical Editions

An official full length release is to be published soon.

|Elements name|Attributes|Status|Description|Reference|
|:-----:|:-----:|:-----:|:-----:|:-----:|
||||||
|ab|-@xml:lang -@xml:id -@n||Anonymous Block. Contains any arbitrary component-level unit of text, acting as an anonymous container for phrase or inter level elements analogous to, but without the semantic baggage of a paragraph.|§3.2|
|abbr|-@type (Values: siglum, hand)|Recommended|Abbreviation. Contains an abbreviation of any sort. In the context of the critical edition, it is used to provide the expected rendering display of any witnesses sigla.|§2.1.3|
|add|||Addition. Contains premodern correction and insertion in the source text made by an author, scribe, or a previous annotator or corrector. Can work as twin with `<del>` by being wrapped in `<subst>`.||
|app|||Apparatus. Contains one entry in a critical apparatus, with a lemma `<lem>`  and usually one or more readings `<rdg>` or notes `<note>` on the relevant passage. Each apparatus entry must be individually wrapped in the element `<app>` .||
|author|||Identify an author.|§2.1.3|
|authority||Mandatory|Release Authority. Supplies the name of a person or other agency responsible for making a work available, other than a publisher or distributor. By default, contain "DHARMA".|§2.1.2|
|availability||Mandatory|A description of the conditions for the distribution and use of the text. Contains `<licence>`.|§2.1.2|
|back||||§3.1|
|bibl|-@n="siglum"||Bibliographic citation. Used for each bibliographic reference. Contains `<ptr>` and possibly `<citedRange>`.|§2.1.3|
|body||Mandatory|The main body of the text. This element is required in any TEI conformant document.|§3.1|
|certainty|||Indicates the degree of certainty associated with some aspect of the text markup. If a text in damaged and you cannot identify the metre with absolute certainty. To be used right after||
|change|-@status -@when -@who|Mandatory|Records a change or set of changes made during the production of a source document, or during the revision of an electronic file.|§2.2.3|
|cit|||Citation. Encodes a direct quotation from a published source.||
|citedRange|||To refer to page numbers.|§2.1.3|
|colophon|-@xml:lang (mandatory)||Record scribal statements not shared between your different witnesses.|§2.1.3|
|correction|||Give specifications regarding the correction principles within your edition|§2.2.1.1|
|date|-@from -@to|Mandatory|Contains a date in any format.|§2.1.2|
|del|||Purposeful deletion. Text deleted in ancient or medieval time.||
|div|-@type(Values:chapter, canto, dyad)|Mandatory|Text division. Contains a subdivision of the text.|§3.2|
|editor|-@ref(Mandatory) -@xml:id|Recommended|The `<editor>` element is allowed to record the editors of the critical edition. It must contained either `<forename>`and `<surname>`, either `<name>`. |§2.1.1.2|
|editorialDecl||Recommended|Formulates methodological choices underlying your edition. It is especially useful if you need to give more detail than, or need to make exceptions from DHARMA Guides and practices.|§2.2.1.1|
|encodingDesc||Recommended|Use to document the encoding process and work.|§2.2|
|fileDesc||Mandatory|File Description. Contains information on the title, on the publication and on the source. This element is a mandatory part of the header and is treated in two separate subsections, one dealing with the meta-level information on the file history, `<titleStmt>`, the other concerning the source from which the XML-file is created `<sourceDesc>`.|§2.1|
|filiation|||Provides information on the relationship between the manuscript and other surviving manuscripts of the same text, either specifically or in a general way.|§2.1.3|
|foreign|||Identifies a word or phrase as belonging to some language other than that of the surrounding text. Note that in the context of the DHARMA, this element is used to encode any element identified as foreign, even under the level of the word and that should be italicized in the render of the edition.||
|forename|||The first name of a person, contained in the `<persName>` element. Used with `<surname>`.||
|front||||§3.1|
|g|||Glyph or Gaiji. Represents a non-standard character. This element indicates that no equivalent is available in DHARMA transliteration system.||
|gap|||Indicates a point where material has been omitted in a transcription because it is physically missing for whatever reason.Can contained `<certainty/>`.||
|gloss|||Identifies a phrase or word used to provide a translation within an inscription. Must be used in correlation with `<term>`.||
|handDesc|-@hands|Mandatory|Description of hands. Contains a description of all the different hands used in a manuscript. The description may be encoded as one or more paragraphs, `<p>`, but more commonly, the various paragraphs are structured as a series of `<handNote>` elements, each containing a prose description of the hands.|§2.1.3; §2.1.3.1|
|handNote|-@xml:id(Mandatory) -@scriptRef(Mandatory)|||Note on a hand. Contains a prose description of one of the hands, containing one or more paragraphs, `<p>`.|§2.1.3; §2.1.3.1|
|head|||Heading. Contains headings on all levels of the document. Allows you to give another editorial title to the part of the inscription. Overstep the attributes given in the preceding `<div>` element. This element can contained only `<foreign>` as child.||
|hi|-@rend (Values: superscript, subscript)||Distinguishes graphical features when there is not pre-existing element.|§2.1.3|
|history||Recommended||§2.1.3|
|idno|-@type(Mandatory in teiHeader with value filename)|Mandatory|Identifier.|§2.1.2; §2.1.3|
|institution||||§2.1.3|
|interpretation|||Describe any additions you are making to the text edition that relate to issues of analysis or interpretation|§2.2.1.1|
|item|||Element as a container for each list item.||
|keywords||Recommended|List containing keywords.|§2.2.2|
|l|||Verse line.|§3.2|
|label|||||
|language|-@ident(mandatory)|Mandatory|Declare a language used in the file.|§2.2.2|
|langUsage||Mandatory|Record the languages used in the file.|§2.2.2|
|lem|||Lemma. Contains a lemma for an apparatus entry. First child of the element `<app>`.||
|lb|||Line beginning. An empty element which marks the beginning of a new line.||
|lg|||Line group. Marks the stanza as a whole.|§3.2|
|licence| -@target(Mandatory)|Mandatory|Licence set by default to a Creative Commons licence identifying the author|§2.1.2|
|list|||Contains any sequence of items organized as a list.||
|listApp|||Contains a list of apparatus entries.||
|listBibl|||Citation list. Contains a list of bibliographic citations of any kind regarding the manuscript as a whole. Inside the `<listBibl>` element, one or more `<bibl>` elements are used for each bibliographic reference.||
|listPrefixDef||Mandatory|List of paths to external file containing some data relevant to the edition.|§2.2|
|listWit||Mandatory|container for all the witnesses that you will be referring to in the critical apparatus|§2.1.3|
|locus||||§2.1.3|
|measure|||Encodes quantity references.||
|milestone|||An empty element which marks any break in the transcription.||
|msContents||Recommend|Describes the intellectual content of any manuscript or part of it|§2.1.3|
|msDesc||Recommended|Manuscript description. Contains a description of a single identifiable manuscript. Within this element six sub-elements are available: `<msIdentifier>`, `<msContents>`, `<physDesc>`, `<history>`, `<additional>` and `<msPart>`.|§2.1.3|
|msFrag|||To declare if your text is transmitted in a fragmented manuscript|§2.1.3|
|msIdentifier||Mandatory|Manuscript identifier.|§2.1.3|
|msItem|-@n|||§2.1.3|
|msName|-@xml:lang|||§2.1.3|
|msPart|||Declares that your witness belongs to a manuscript composed of parts that were originally separated and that have been bound together at a later stage|§2.1.3|
|name|||Contains a name, i.e. a proper noun or a noun phrase.||
|note|| |Contains comments to the text by the editor. It can be in a freeform text pertaining to a particular lemma.||
|normalization|||Explain the extent of normalization and regularization applied on the text as critically edited|§2.2.1.1|
|num|||Numeral. Contains a numeral, including any delimiters. It does not replace the <g> element.||
|objectDesc||||§2.1.3|
|origDate|@when||Date of creation of your manuscript|§2.1.3|
|origPlace|||Place of creation of your manuscript|§2.1.3|
|p|||Paragraph. Marks paragraphs in prose of at least one complete sentence or the equivalent of a semantic paragraph.|§2.1.2; §2.1.3; §3.2|
|pb|||Page beginning. An empty element which marks the beginning of a new page in a paginated document. It is also used in foliated documents (having numbers like ‘1r’, ‘1v’, ‘2r’, ‘2v’, and so on.)||
|persName|-@ref(mandatory in the teiHeader)||Personal name. Contains a proper noun or a proper noun phrase referring to a person, consisting of one or more words. For Occidental names, use `<forename>` and `<surname>` structures and for others `<name>`.|§2.1.1.2|
|physDesc||Mandatory||§2.1.3|
|placeName||A name of a specific location.|||
|prefixDef|-@ident(mandatory) -@matchPattern(mandatory) -@replacementPattern(mandatory)|Mandatory|Path toward some data to complete the edition|§2.2|
|projectDesc||Recommended|Use to state your project|§2.2; §2.2.1|
|profilDesc|||Provide metadata related to non-bibliographic aspects of the text|§2.2.2|
|ptr|-@target||Pointer for bibliographical data and citing witnesses, sigla and hands|§2.1.3; §2.1.4|
|publicationStmt||Mandatory|Publication statement. Groups information concerning the publication or distribution of an electronic or other text.|§2.1.2||
|pubPlace||Mandatory|Publication place for legal matters stating the edition. ||
|punctuation|||Explain the degree of correspondence between punctuation of your constituted text and the punctuation found in the witnesses|§2.2.1.1|
|q|||Quoted text not attributed to a publish source.||
|quote|||Quotation. Contains a quotation from another source.||
|rdg|||Reading. Contains an alternative reading. Must be wrapped inside the element `<app>` and follow a `<lem>`.||
|ref|||Reference. Defines a reference to another inscription in the DHARMABase.|§2.2|
|repository||Mandatory|Contains the name of a repository which stored the inscription.|§2.1.3|
|resp||Recommended|Responsibility. Contains a phrase describing the type of responsibility, e.g. transcription, conversion, proof-reading.|§2.1.1.2|
|respStmt||Recommended|Statement of responsibility. Particularly important when listing the contributors to an edition.|§2.1.1.2|
|revisionDesc||Mandatory|Revision description. Summarises the revision history of the text.|§2.2.3|
|roleName|||Contains a name component which indicates that the referent has a particular role or position in society, such as an official title or rank.||
|samplingDesc|||Record free-text information about inclusion or omission of portions of the text, manuscripts, or witnesses|§2.2.1.2|
|schemaRef|-@type -@key @url(mandatory)|Mandatory|Point to any external customization file of the TEI.|§2.2; §2.2.1.3|
|seg|||Segment. Groups one or more strings of text, e.g. words.||
|settlement||||§2.1.3|
|sic|||Contains a passage reproduced as is although apparently incorrect or inaccurate. By EpiDoc convention, this markup is used for text that is legible but does not seem intelligible.||
|sourceDesc||Mandatory|Source description. Mandatory part of the header and describes the source material. Sub-element of `<fileDesc>`. Record details about the original manuscripts and printed texts used as witnesses in establishing your critical edition|§2.1.3|
|space|||Space is an empty element which indicates a "blank space". DHARMA does not follow regular TEI practice and is not Epic conformant either regarding the attributes.||
|subst|||Substitution. Wraps the combination of deletion and addition.||
|summary|-@xml:lang||Provides a summary of the edition|§2.1.3|
|supplied|||Signifies text supplied by the transcriber, encoder or editor either in place of text which is missing or to clarify a reading.||
|supportDesc||||§2.1.3|
|surname|||Contains a family (inherited) name of a person, excluding patronyms and metronyms.||
|surplus|||Characters were erroneously added by the scribe, and you correct the text by suppressing the superfluous segment.||
|TEI|-@corresp (mandatory for external files) -@type (values: bibliography, commentary, edition and translation- Mandatory) -@xml:id (mandatory on the main file) -xml:lang (by default eng) ||The element `<TEI>` must wrap all TEI-compliant content as a root tag. The `<TEI>` element must contain two sub-elements, `<teiHeader>` and `<text>`.|§1|
|teiHeader||Mandatory|The TEI-based header contains additional descriptive information (metadata) about the digital document and is a mandatory component of every TEI document.|§2|
|term|||Contains a single-word, multi-word, or symbolic designation which is regarded as a technical term. Use it to wrap a foreign element followed by its translation into a local language that shall be encoded as `<gloss>`.|§2.2.2|
|text|-@xml:space(Default value must be ‘preserve’) -@xml:lang|Mandatory|Contains a single text of any kind.|§3.1|
|textClass|||Contain the element `<keywords>`.|§2.2.2|
|textLang|-@mainLang (Recommended)|||§2.1.3|
|title|-@type (Values: main, sub) -@subype (Values: editorial, base-text, commentary) -@xml:lang (only if the title isn't in English) -@n (Only if more than one title bear the same @subtype)|Mandatory in the `<teiHeader>`|Contains a title for any kind of work.|§2.1.1.1; §2.1.3|
|titleStmt||Mandatory|Title statement. Contains information on the title, editor and other people who have been involved in the edition.|§2.1.1|
|unclear|||Stands in EpiDoc for any character “of which at least traces survive, but not adequately to identify the letter unambiguously outside of its context”.|§2.1.1|
|variantEncoding|-@method(mandatory; values: parallel-segmentation, double-end-point and location-referenced) -@location(mandatory; values: internat, external)|Mandatory|Declare the methodology chosen to encode the apparatus|§2.2.1.4|
|witness|-@xml:id (Mandatory)|Mandatory|Declaration of witnesses|§2.1.3|
