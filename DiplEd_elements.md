# DHARMA List of Elements for Diplomatic Editions


An official full length release has been published already [here](https://erc-dharma.github.io/project-documentation/encoding-diplomatic/DHARMA%20EGD%20v1%20release.pdf), but you can find the candidate release [here](https://docs.google.com/document/d/1hjWrrwRZQp4hmEqw4jBhhqoXdwJvRlw3EWboJteOPw0/edit?usp=sharing)
Version 0.2 (July 2019), compiled and edited by Axelle Janiak.

## Index of elements and attributes
### A
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;ab&gt;||Anonymous Block. Contains any arbitrary component-level unit of text, acting as an anonymous container for phrase or inter level elements analogous to, but without the semantic baggage of a paragraph.|2.2.2, 7.2.1, 7.5.4, 7.5.5|
|@part |Optional|The beginning or end of one of these containers falls within a lacuna. Sample values: ‘I’ if the initial part of the container is extant; ‘F’ if the final part of the container is extant, and ‘M’ if only the medial part of the container is extant.||
|@rend|Optional|This attribute can take several values. Order then following (1) script and (2) lettering. The directionality is not available for this element.Recommended values for script: ‘grantha’Recommended values for lettering:‘ornate’, ‘large’, ‘small’, ‘tall’, ‘wide’ and ‘expanded’.||
|@xml:lang|Optional|Use this attribute only if the containing text is in a language other than the primary one. Use the 3 letters language code define in Appendix D.||
|&lt;abbr&gt;||Abbreviation. Contains an abbreviation of any sort. If your text includes abbreviations, it is recommended that you wrap these in the element &lt;abbr&gt; to flag them for computer processing.Don’t expand the abbreviations.|7.3|
|&lt;add&gt;||Addition. Contains premodern correction and insertion in the source text made by an author, scribe, or a previous annotator or corrector.Can work as twin with &lt;del&gt; by being wrapped in &lt;subst&gt;.|4.5.2, 4.5.3|
|@place|Mandatory|Indicates where the addition is made. Sample values: ‘ inline’, ‘below’,  ‘above’, ‘top’, ‘bottom’ ‘left’, ‘right’ and ‘overstrike’ when a correction is written over previously engraved text, which was rendered completely illegible in the process. (closed list) ||
|@rend|Optional|Encodes the involvement of a premodern editorial mark. Value: ‘mark’. (closed list)||
|&lt;app&gt;||Apparatus. Contains one entry in a critical apparatus, with a lemma &lt;lem&gt;  and usually one or more readings &lt;rdg&gt; or notes &lt;note&gt; on the relevant passage.Each apparatus entry must be individually wrapped in the element &lt;app&gt;.|9.1.1, 9.1.2, 10.3|
|@loc|Mandatory|Indicates the location of the variation, using line numbers as reference. ||
|&lt;authority&gt;||Release Authority. Supplies the name of a person or other agency responsible for making a work available, other than a publisher or distributor.Contains &lt;note&gt;.|1.4, 11.1|
|&lt;availability&gt;||A description of the conditions for the distribution and use of the text.Contains &lt;licence&gt;.|11.1|

### B
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;bibl&gt;||Bibliographic citation. Used for each bibliographic reference.Contains &lt;ptr&gt; and possibly &lt;citedRange&gt;.|9.4.2, 9.4.3, 10.4.5|
|@n|Optional|Provides a siglum for a bibliographic entry. ||
|@rend|Optional|With the value ‘omitname’ to provide a display without the name; or with ‘ibid’ to display ibid. and not the name of the author. (Closed list)||
|&lt;body&gt;||The main body of the text. This element is required in any TEI conformant document. Contains &lt;div&gt; @type : edition, apparatus, translation, commentary, bibliography.|1.4|

### C
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;certainty/&gt;||Indicates the degree of certainty associated with some aspect of the text markup. If a text in damaged and you cannot identify the metre with absolute certainty. To be used right after|2.3.4, 5.4.6|
|@locus|Mandatory|‘name’  concerns whether the name of the element or attribute used is correctly applied while ‘ value’ concerns the content for an element or the value for an attribute. With an &lt;lg&gt; element, the content should be @locus="value"With a &lt;gap/&gt; element, the content should be @locus="name".||
|@match|Mandatory|Supplies an XPath expression to identify the node. ‘..’ to mention a parent element and ‘../@attribute’ to refer to an attribute of the parent element. With an &lt;lg met=""&gt; , the value should be @match="../@met".  With a &lt;gap/&gt; element, the content should be @match="..".||
|&lt;change&gt;||Records a change or set of changes made during the production of a source document, or during the revision of an electronic file.|11.3|
|@when|Mandatory|Recommended value is a date in format year-month-day, i.e. YYYY-MM-DD.||
|@who|Mandatory|Value of which shall be the personal identifier of the person(s) making the change, i.e. normally yours, with the prefix “part:” (as an abbreviated reference to the file listing participants of the project) and the two first letters of each of your names. ||
|@status|Optional|Keep track of significant milestones in the history of the file, with one of the following values: ‘draft’, ‘candidate’, ‘approved’, ‘published’, ‘withdrawn’. (Closed list)||
|&lt;choice&gt;||Groups a number of alternative encodings for the same point in the text, usually the twins &lt;orig&gt; et &lt;reg&gt; as well as &lt;sic&gt; and &lt;corr&gt;.Gathers limited number of alternative interpretations with &lt;unclear&gt;. Can only contained two &lt;unclear&gt;|5.3.3|
|&lt;cit&gt;||Citation. Encodes a direct quotation from a published source. Works with the element &lt;quote&gt;.|10.4.4|
|&lt;citedRange&gt;||To refer to page numbers.|10.4.5|
|@unit|Optional|To refer to an entity other than a page, values: ‘page’, ‘volume’, ‘item’, ‘figure’, ‘plate’, ‘table’, ‘appendix’, ‘note’, ‘entry’, ‘part’. (Closed list) ||
|&lt;code&gt;||Contains literal code from some formal language such as a programming language.|Template|
|&lt;corr&gt;||Correction. Contains the correct form of a passage apparently incorrect or inaccurate in the inscritption text.Accompanied by the &lt;sic&gt; element wrapped by &lt;choice&gt; as parent.|6.2.2, 6.2.5, 6.2.6|

### D
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;damage&gt;||Contains an area of damage to the text.|5.2|
|&lt;date&gt;||Contains a date in any format. |10.4.5|
|@from|Optional|Records the starting point of a period. Works in twin with @to. Recommended value is a date in format year-month-day, e.g. ‘2019-10-15’. ||
|@to|Optional|Records the ending point of a period. Works in twin with @from. Recommended value is a date in format year-month-day, e.g. ‘2019-10-15’.||
|@when|Optional|Records a precise date. Recommended value is a date in format year-month-day, e.g. ‘2019-10-15’.||
|&lt;del&gt;||Purposeful deletion. Text deleted in ancient or medieval time. Can work in pair with &lt;add&gt; and be wrapped by &lt;subst&gt;. By default, any deletion will be understood as erased. |4.5.1, 4.5.3|
|@rend|Optional|Specifies the deletion by marks, using any convenient typology. Sample values: ‘strikeout’, ‘ui’ and ‘other’ (Closed list)Use the value ‘corrected’ while &lt;del&gt; is used in combinaison with &lt;add&gt; and &lt;subst&gt;.||
|&lt;div&gt;|2 uses cases|Text division. Contains a subdivision of the text.|3.4.2, 3.4.3, 3.4.4, 7.2.1, 7.5.2, 7.5.3, 9.1.1, 9.2.1, 9.2.2, 9.2.3, 9.3.1, 9.4.1|
|&lt;div&gt; @type: ‘edition’, ‘apparatus’, ‘translation’, ‘commentary’ and ‘bibliography’.|All the attributes must be used together. |Structure the content of the Digital file. ||
|@type|Mandatory|Specifies the name conventionally given to the type of division. Values: ‘edition’, ‘apparatus’, ‘translation’, ‘commentary’ and ‘bibliography’. (Closed list)||
|@resp|Optional|If a translation is made by a member of the project.||
|@source|Optional|To use, if a translation in adopted verbatim from a printed edition. ||
|@xml:lang|Optional|Gives the language for the edition and for the translation. Use the 3 letters language code define in Appendix D.||
|&lt;div&gt; @type: ‘textpart’.|All the attributes can be combined if necessary.|Structure the content of the &lt;div type="edition"&gt;. There must be at least two &lt;div type="textpart"&gt;.||
|@n|Mandatory|Mandatory with ‘textpart’. Uppercase Latin letters are generally recommended for numeration, but any scheme may be used depending on your preference and the conventions of your specific field as long as the content is unique.||
|@rend|Optional|Qualify the orientation of the text. Values: ‘bt-rotated’, ‘tb-rotated’, ‘bt-upright’, ‘tb-upright’, ‘rl-upright’, ‘rl-flipped’ and ‘rl-rotated’.(Closed list)||
|@style|Optional|Records the alignment of the text. Value: ‘text-align: right’, ‘text-align: center’, ‘text-align: left’, ‘text-align: justify’. (Closed List)||
|@subtype|Optional|Recommended to qualify and define more precisely the  ‘ textpart’. Possible values : ‘ fragment’, ‘face’, ‘facet’, ‘faces’, ‘facets’, ‘zone’, ‘column’, ‘item’ … (Open list)||
|@type|Mandatory|Specifies the name conventionally given to the type of division. Sample values: ‘textpart’. (Closed list)||
|@xml:lang|Optional|Gives the language for a part of the text if it changes from ‘textpart’ to ‘textpart’. Use the 3 letters language code define in Appendix D.||

### F
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;fileDesc&gt;||File Description. Contains information on the title, on the publication and on the source. This element is a mandatory part of the header and is treated in two separate subsections, one dealing with the meta-level information on the file history, &lt;titleStmt&gt;, the other concerning the source from which the XML-file is created &lt;sourceDesc&gt;.|1.4, 11.1, 11.2|
|&lt;foreign&gt;||Identifies a word or phrase as belonging to some language other than that of the surrounding text.Note that in the context of the DHARMA, this element is used to encode any element identified as foreign, even under the level of the word and that should be italicized in the render of the edition.|7.2.2, 9.2.8, 9.2.12, 10.2.1, 10.3.3|
|@xml:lang|Optional|Gives the language of the text wrapped. Its use is optional but are mandatory inside the &lt;div type="edition"&gt;.Use the 3 letters language code define in Appendix D.||
|&lt;forname&gt;||The first name of a person, contained in the &lt;persName&gt; element.Used with &lt;surname&gt;.|10.5.1, 11.1|
|&lt;fw&gt;|All the attributes can be combined if necessary.|Forme Work. Epigraphic occurrences of forme work are primarily foliation or pagination marks on copper plates.|3.3.4, 7.5.1, 7.5.3, 7.5.4, 7.5.5|
|@n|Mandatory|The value of @n shall be the same as the @n of the &lt;pb/&gt; element marking the beginning of the page on which the forme work item appears||
|@place|Mandatory|Location of the foliation/pagination marks on the "page". Values: ‘top-left’, ‘top’, ‘top-right’, ‘left’, ‘right’, ‘bot-left’, ‘bottom’ and ‘bot-right’. (Closed list)||
|@rend|Optional|This attribute can take several values. Order then following (1) directionality and orientation, (2) script and (3) lettering. Values for orientation: ‘bt-rotated’, ‘tb-rotated’, ‘bt-upright’, ‘tb-upright’, ‘rl-upright’, ‘rl-flipped’ and ‘rl-rotated’.Recommended values for script: ‘grantha’Recommended values for lettering: ‘ornate’, ‘large’, ‘small’, ‘tall’, ‘wide’ and ‘expanded’.  ||
|@style|Optional|Records the alignment of the forme work. Value: ‘text-align: right’, ‘text-align: center’, ‘text-align: left’, ‘text-align: justify’. (Closed list)||

### G
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;g&gt;|3 uses cases|Glyph or Gaiji. Represents a non-standard character. This element indicates that no equivalent is available in DHARMA transliteration system.|4.2.1, 4.2.2, 4.2.3, 4.2.4, 4.2.5, 4.2.6|
|@type|Mandatory|Value: ‘numeral’Miscellaneous symbol. See Symbol Taxinomy, EGD Supplement. Values: ‘dandaPlain’, ‘dandaHooked’, ‘dandaCross’, ‘dandaOrnate’, ‘ddandaPlain’, ‘ddandaHooked’, ‘ddandaCross’, ‘ddandaOrnate’, ‘comma’, ‘commaSmall’, ‘dashPlain’, ‘dashConcave’, ‘dashConvex’, ‘dashHooked’, ‘dashWavy’, ‘dashLong’, ‘dashDouble’, ‘dashDoubledot’, ‘dotMid’, ‘dotDouble’, ‘dotTriangle’, ‘circleSmall’, ‘circleLarge’, ‘circleHigh’, ‘circleLow’, ‘circleCross’, ‘circleDouble’, ‘circleFloret’, ‘circleHorned’, ‘circleConcentric’, ‘circleTarget’, ‘circleTriangle’, ‘spiralR’, ‘spiralL’, ‘crossPlus’, ‘crossX’, ‘floretQuatrefoil’, ‘floretComplex’, ‘gomutraInitial’, ‘gomutraFinal’, ‘gomutraFinalBars’, ‘gomutraFinalComplex’, ‘tennisBall’, ‘squiggelVertical’… (open list) Those won’t be added inside the schema.||
|@subtype|Optional|||
|&lt;gap/&gt;||Indicates a point where material has been omitted in a transcription because it is physically missing for whatever reason.Can contained &lt;certainty/&gt;.|3.2.3, 5.1, 5.4.1, 5.4.2, 5.4.3, 5.4.4, 5.4.5, 5.4.6, 5.4.7, 5.4.8, 9.1.3, 9.2.9, 9.2.12 |
|@extent|Optional|Indicates a size of a lacuna that can’t be counted. Can’t be used with @quantity. Value ‘unknown’. (Closed list)||
|@precision|Optional|Indicates the estimation about the number of lost characters. Must be used with @reason, @ quantity and @unit. Value ‘low’. (Closed list)||
|@quantity|Optional|Indicates approximately the extent of the gap. Values refer to the @unit attribute and are thus the number of characters, words, lines, leaves or quires in the manuscript, i.e. ‘1’, ‘2’, ‘3’, and so on.||
|@reason|Mandatory|States the reason for omission. Sample values: ‘illegible’, ‘lost’, ‘undefined’, ‘ellipsis’. (Closed list)@reason can ber used on its own in the div[@type=‘translation’]||
|@unit|Optional|Names the unit used for describing the extent of the gap. Sample values:  ‘character’, ‘component’ and ‘line’.  The values ‘page’, ‘plate’ and ‘folio’ are allowed but not recommended. (Open list)||
|&lt;gi&gt;||Contains the name in the form of a generic identifier|Template|
|&lt;gloss&gt;||Identifies a phrase or word used to provide a translation within an inscription. Must be used in correlation with &lt;term&gt;|7.2.2|
|@xml:lang|Optional|Use this attribute only if the containing text is in a language other than the primary one. Use the 3 letters language code define in Appendix D.||

### H
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;handDesc&gt;||Description of hands. Contains a description of all the different hands used in a manuscript. The description may be encoded as one or more paragraphs, &lt;p&gt;, but more commonly, the various paragraphs are structured as a series of &lt;handNote&gt; elements, each containing a prose description of the hands.|4.4, 11.2.1|
|&lt;handNote&gt;||Note on a hand. Contains a prose description of one of the hands, containing one or more paragraphs, &lt;p&gt;.|7.5, 10.6.4, 11.2.1|
|@xml:id|Mandatory|Specifies how widely the hand is used in the manuscript. Sample values: ‘filename_hand1’, ‘filename_hand2’… (Open list)||
|&lt;handShift/&gt;||Change of scribal hand. Since a shift of hands in most cases will conflict with other divisions of the text, the recommended element is an empty one. If there are two hands in a document there will thus be a single &lt;handShift/&gt; element, located at the break between hand 1 and hand 2.|4.4|
|@new|Mandatory|Value shall be the identifier associated in the header with the hand in question ‘#filename_hand1’, ‘#filename_hand2’…||
|&lt;head&gt;||Heading. Contains headings on all levels of the document. Allows you to give another editorial title to the part of the inscription. Overstep the attributes given in the preceding &lt;div&gt; element. This element can contained only &lt;foreign&gt; as child.|3.4.3, 9.2.2|
|@xml:lang|Optional|Specifies the editorial nature of the heading. By default the value will be set on English. ||
|&lt;hi&gt;||Distinguishes graphical features when there is not pre-existing element. |7.5.1, 7.5.4, 7.5.5, 10.2.1|
|@rend|Mandatory|This attribute can take several values. Order then following (1) script and (2) lettering. The directionality is not available for this element.Recommended values for script: ‘grantha’,Recommended values for lettering: ‘ornate’, ‘large’, ‘small’, ‘tall’, ‘wide’ and ‘expanded’. Recommended values for typographic highlighying: ‘italic’, ‘bold’, ‘subscript’ and ‘superscript’.||

### I
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;idno&gt;||Identifier. Provide the filename without the extension. |1.4, 10.6.4, 11.1.3|
|@type|Mandatory|The name of the file. Value: ‘filename’ ||
|&lt;item&gt;||Element as a container for each list item.|10.2.2|

### L
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;l&gt;||Verse line.|2.3.2, 2.3.3, 2.3.4, 2.3.5, 2.3.6, 5.4.7, 7.5.1, 7.5.3, 7.5.4, 7.5.5|
|@enjam|Optional|Enjambement. Encode the fact that the break at the end of the line does not coincide with the end of a word. This attribute must be added to the &lt;l&gt; element containing the initial part of the broken word, not to the one containing the final part. Value must be: ‘yes’.||
|@met|Optional|Metrical structure. Contains a user-specified encoding for the conventional metrical structure of the element, for lines that deviate from the metro of the stanza. Identifies the meter of the stanza by a conventional name, or in prosodic notations if you can’t put a name to the metre. Sample values in appendix B and "uncertain". (open list)||
|@n|Mandatory|Indicates the line number within the stanza. Values must be given as pairs of lowercase Latin letters: ‘ab’, ‘cd’ for Sanskrit/Prakrit quantitative verse; lowercase Latin letters: ‘a’, ‘b’, ‘c’ for stanza with 4 to 8 lines;  Arabic numbers: ‘1’, ‘2’, ‘3’ for stanzas with more than 8 lines or in Tamil. ||
|@real|Optional|Contains a user-specified encoding for the conventional metrical structure of the element, for lines that deviate from the metro of the stanza. Table 2 of Appendix B for the prosodic form and Table 3 of Appendix B for the conventional name.||
|@rend|Optional|This attribute can take several values. Order then following (1) script and (2) lettering. Recommended values for script: ‘grantha’Recommended values for lettering: ‘ornate’, ‘large’, ‘small’, ‘tall’, ‘wide’ and ‘expanded’.||
|@part |Optional|The beginning or end of one of these containers falls within a lacuna. Sample values: ‘I’ if the initial part of the container is extant; ‘F’ if the final part of the container is extant, and ‘M’ if only the medial part of the container is extant.||
|&lt;label&gt;||Provides a title for zones. Override the content of the &lt;milestone/&gt; attributes. This element can contained only &lt;foreign&gt; as child.|3.5.4, 3.6.2|
|@xml:lang|Mandatory|Specifies the editorial nature of the heading. By default the value will be set on English. ||
|&lt;lem&gt;||Lemma. Contains a lemma for an apparatus entry. First child of the element &lt;app&gt;|9.1.1, 9.1.3, 9.1.5|
|@source|Optional|Shows which previous edition supports the reading adopted in your edition. ||
|&lt;lb/&gt;||Line beginning. An empty element which marks the beginning of a new line.|3.2.1, 3.2.2, 3.2.3, 3.2.4, 3.3.3, 3.5.3, 7.5.1, 7.5.2, 7.5.4, 7.5.5|
|@break|Optional|The line beginning does not signify a break in the text.  Always use it if you are reasonably certain that an interruption is present. Value ‘no’.||
|@n|Mandatory|Specifies the line number with numerical values: ‘1’, ‘2’, ‘3’… The value shall be unique in the file, so for more complex line numbers pattern add the content of the @n of the partitions before such as ‘A1’, ‘A2’, ‘1v1’, ‘2r1’…Note that if your partitions are numbered with numerals or end with a numeral, add a full stop ‘A1.1’, ‘A1.2’…||
|@rend|Optional|This attribute can take several values. Order then following (1) directionality and orientation, (2) script and (3) lettering. Values for orientation: ‘bt-rotated’, ‘tb-rotated’, ‘bt-upright’, ‘tb-upright’.Recommended values for script: ‘grantha’Recommended values for lettering: ‘ornate’, ‘large’, ‘small’, ‘tall’, ‘wide’ and ‘expanded’.||
|@style|Optional|Value: ‘text-align: right’, ‘text-align: center’, ‘text-align: left’, ‘text-align: justify’.||
|&lt;lg&gt;||Line group. Marks the stanza as a whole.|2.3.2, 2.3.3, 2.3.4, 5.4.7, 7.2.1, 7.5.1, 7.5.3, 7.5.4, 7.5.5|
|@met|Mandatory|Identifies the meter of the stanza by a conventional name, or in prosodic notations if you can’t put a name to the metre.Sample values in appendix B and "uncertain". (open list)||
|@n|Mandatory|Indicates the identity of the stanza. Values must be given as numbers: ‘1’, ‘2’, ‘3’, and so on.||
|@part |Optional|The beginning or end of one of these containers falls within a lacuna. Sample values: ‘I’ if the initial part of the container is extant; ‘F’ if the final part of the container is extant, and ‘M’ if only the medial part of the container is extant.||
|@rend|Optional|This attribute can take several values. Order then following (1) script and (2) lettering. Directionality is not available for this element. Recommended values for script: ‘grantha’Recommended values for lettering: ‘ornate’, ‘large’, ‘small’, ‘tall’, ‘wide’ and ‘expanded’.||
|@xml:lang|Optional|Use this attribute only if the containing text is in a language other than the primary one. Use the 3 letters language code define in Appendix D.||
|&lt;list&gt;||Contains any sequence of items organized as a list.|10.2.2|
|@rend|Optional|Values: ‘numbered’ and ‘bulleted’||
|&lt;listApp&gt;||Contains a list of apparatus entries. |9.1.1|
|&lt;listBibl&gt;||Citation list. Contains a list of bibliographic citations of any kind regarding the manuscript as a whole. Inside the &lt;listBibl&gt; element, one or more &lt;bibl&gt; elements are used for each bibliographic reference.|9.4.2|
|@type|Mandatory|Distinguishes between primary and secondary bibliographies. ||
|&lt;listPrefixDef&gt;||||

### M
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;measure&gt;||Encodes quantity references.|7.4.4|
|@commodity|Optional|Expresses the measured substance. ||
|@quantity|Optional|Records a numeric value||
|@type|Optional|Records the typology used to measure, e.g. ‘volume’, ‘weight’, ‘currency’….||
|@unit|Optional|Indicates the unit used for the measurement expressed by its standard symbol. ||
|&lt;milestone/&gt;||An empty element which marks any break in the transcription.|2.3.2, 3.5.3, 3.5.4 , 3.5.5, 3.6.2, 3.6.3 |
|@break|Optional|The&lt;milestone/&gt; does not signify a break in the text.  Its value will always be by default "no". ||
|@n|Mandatory with @unit. |To identify the section. Uppercase latin letters are recommended, but any schema may be used depending your material. Uppercase letters N, S, E and W can be used for cardinal directions and lowercase letters in alternance with uppercase to denote major/frontal and minor/lateral faces. ||
|@type|Optional|To mark a caesura that was disregarded by the composer or involves sandhi that blurs its location, e.g. &lt;milestone type="yati" break="no"/&gt;To encode a inscribed zones. Value: ‘pagelike’||
|@unit|Mandatory|Pagelike partition shall be a single word describing the nature of the transition. Values: ‘face’, ‘facet’, ‘faces’, ‘facets’, ‘zone’, ‘column’, ‘block’, ‘surface’, ‘fragment’, ‘item’, ‘area’… (open list)||
|&lt;msContents&gt;||Describes the intellectual content of the inscription. |Template|
|&lt;msDesc&gt;||Manuscript description. Contains a description of a single identifiable manuscript. Within this element six sub-elements are available: &lt;msIdentifier&gt;, &lt;msContents&gt;, &lt;physDesc&gt;, &lt;history&gt;, &lt;additional&gt; and &lt;msPart&gt;.|11.2|
|&lt;msIdentifier&gt;||Manuscript identifier.||

### N
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;name&gt;||Contains a name, i.e. a proper noun or a noun phrase.|10.5.1|
|&lt;note&gt;||Contains comments to the text by the editor. It can be in a freeform text pertaining to a particular lemma. |9.1.1, 9.1.7, 9.2.1, 9.2.2, 9.2.12, 10.3.2, 10.4.1|
|@resp|Optional|To give authorship to some members of the project. ||
|@source|Optional|Stating verbatim if the note is adopted from a publication. ||
|@type|Optional|It can only be used in the commentary division. Giving credit to someone who has helped with the translation, e.g. ‘credit’||
|@xml:lang|Optional|||
|&lt;num&gt;||Numeral. Contains a numeral, including any delimiters. It does not replace the &lt;g&gt; element. |7.1.1, 7.1.2, 7.1.3|
|@atLeast|Can replaced @value with @atMost|Element to record the lowest possible value of the number as a whole. Works with @atMost||
|@atMost|Can replaced @value with @atLeast. |Element to record the highest possible value of the number as a whole. Works with @atLeast. ||
|@cert|Optional|Attribute @cert with the value ‘low’ to flag the value as tentative.||
|@value|Mandatory, but can be replaced by @atLeast and @atMost|Specifies the numeral in numbers in machine-readable format, i.e. ‘1’, ‘2’, ‘3’, and so on.Fractions shall be recorded as decimal with a round value to three digits after the decimal.||

### O
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;orig&gt;||Original form. Contains a passage in its original form in a non-standard usage. &lt;reg&gt; can be used for normalisation by substitution. |6.3.1, 6.3.2, 6.3.4|

### P
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;p&gt;||Paragraph. Marks paragraphs in prose of at least one complete sentence or the equivalent of a semantic paragraph.|2.2.1, 3.2, 5.4.7, 7.2.1, 7.5.1, 7.5.4, 7.5.5, 9.2.6, 9.3.2, 9.4.4, 10.3.2|
|@n|Optional|Indicates in the translation to either a line number or a stanza number in the original. ||
|@part |Optional|The beginning or end of one of these containers falls within a lacuna. Sample values: ‘I’ if the initial part of the container is extant; ‘F’ if the final part of the container is extant, and ‘M’ if only the medial part of the container is extant.||
|@rend|Optional|This attribute can take several values. Order then following (1) script and (2) lettering. Directionality is not available for this element.Recommended values for script: ‘grantha’Recommended values for lettering: ‘ornate’, ‘large’, ‘small’, ‘tall’, ‘wide’ and ‘expanded’. Use @rend="stanza", to interpret the element &lt;p&gt; as a stanza in the translation.||
|@xml:lang|Optional|Use this attribute only if the containing text is in a language other than the primary one. Use the 3 letters language code define in Appendix D.||
|&lt;pb/&gt;||Page beginning. An empty element which marks the beginning of a new page in a paginated document. It is also used in foliated documents (having numbers like ‘1r’, ‘1v’, ‘2r’, ‘2v’, and so on.)|3.3.4, 3.3.5, 3.5.2, 3.5.3, 3.5.5|
|@break|Optional|The&lt;pb/&gt; does not signify a break in the text.  Its value will always be by default "no". ||
|@n|Mandatory|Number. In a paginated document, the values will be numbers like ‘1’, ‘2’, ‘3’, and so on. In a foliated document, it should indicate front or back pages (recto, verso), with values like ‘1r’, ‘1v’, ‘2r’, ‘2v’, and so on. Note that you can an underscore, but not a space if you built your own numbering schema. ||
|&lt;persName&gt;||Personal name. Contains a proper noun or a proper noun phrase referring to a person, consisting of one or more words.|7.4.1, 7.4.5, 10.6.3|
|@key|Optional|Contains the common name of a place.||
|@next|Optional|Provides the following identifier when the person name is cut in two parts. ||
|@prev|Optional|Provides the preceding identifier when the person name is cut in two parts. ||
|@ref|Optional|Provides an explicit means of locating a full definition or identity for the entity being named by means of one or more URIs.||
|@subtype|Optional|Subcategorisation of the @type. Sample values: ‘coronation’, ‘sobriquet’, ‘title’, ‘other’. (Not in the schema for now) ||
|@type|Optional|Indicates the type of name. Sample values: ‘divine’, ‘human’, ‘personification’. (Not in the schema for now) ||
|@xml:id|Optional|Provides a unique identifier for the element bearing the attribute. Must be used if the person name is cut in two by some overlapping tags.||
|&lt;placeName&gt;||A name of a specific location.|7.4.3, 7.4.5, 10.6.3|
|@key|Optional|Contains the common name of a person.||
|@next|Optional|Provides the following identifier when the place name is cut in two parts. ||
|@prev|Optional|Provides the preceding identifier when the place name is cut in two parts. ||
|@ref|Optional|Provides an explicit means of locating a full definition or identity for the entity being named by means of one or more URIs.||
|@subtype|Mandatory|Provides precision of the place type: ’province’, ‘district’, ‘site’, ‘sitePart’, ‘temple’, ‘shrine’, ‘monastery’, ‘feedingHall’, ‘tank’, ‘pavillion’, ‘garden’. ||
|@type|Mandatory|Indicates if it is a ’territorialDivision’ or a ‘builtPlace’. ||
|@xml:id|Optional|Provides a unique identifier for the element bearing the attribute. Must be used if the place name is cut in two by some overlapping tags. ||
|&lt;prefixDef&gt;||||
|&lt;ptr/&gt;||Pointer. |10.4.5|
|@target|Mandatory|Must contain the Zotero Short Title||
|&lt;publicationStmt&gt;||Publication statement. Groups information concerning the publication or distribution of an electronic or other text.|1.4, 11.1|
|&lt;pubPlace&gt;||Publication place for legal matters stating the edition. |11.1.3|

### Q
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;q&gt;||Quoted text not attributed to a publish source.|10.4.3|
|@xml:lang|Optional|Use this attribute only if the containing text is in a language other than the primary one. Use the 3 letters language code define in Appendix D.||
|&lt;quote&gt;||Quotation. Contains a quotation from another source.|9.2.4, 10.4.4|
|@rend|Mandatory|To create a block quote. Sample value: ‘block’.||

### R
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;rdg&gt;||Reading. Contains an alternative reading. Must be wrapped inside the element &lt;app&gt; and follow a &lt;lem&gt;.|9.1.1, 9.1.4, 9.1.5|
|@source|Mandatory|Gives credit to the editor(s) responsible of the reading. ||
|&lt;ref&gt;||Reference. Defines a reference to another inscription in the DHARMABase.|10.4.6|
|@n|Optional|Add the name of the repository if it is stored in another repository. ||
|@target|Optional|Specifies the destination of the reference by supplying one or more URI references. For a DHARMA inscription, you need to provide the name of the file. ||
|&lt;reg&gt;||Regularised form. Contains a passage in the manuscript corrected by the scribe (or a later scribe). It is usually accompanied by an &lt;orig&gt; element in which the uncorrected original form is rendered.|6.3.2|
|&lt;repository&gt;||Contains the name of a repository which stored the inscription.|Template|
|&lt;resp&gt;||Responsibility. Contains a phrase describing the type of responsibility, e.g. transcription, conversion, proof-reading.|11.1.2|
|&lt;respStmt&gt;||Statement of responsibility. Particularly important when listing the contributors to an edition.|11.1.2|
|&lt;revisionDesc&gt;||Revision description. Summarises the revision history of the text.|11.3|
|&lt;roleName&gt;||Contains a name component which indicates that the referent has a particular role or position in society, such as an official title or rank.|7.4.2, 7.4.5|
|@next|Optional|Provides the following identifier when the place name is cut in two parts. ||
|@prev|Optional|Provides the preceding identifier when the place name is cut in two parts. ||
|@subtype|Mandatory|Indicates the role of the person in the transaction recorded. Sample values: ‘donor’, ‘donee’, ‘trustee’, ‘inChargeDonation’, ‘witness’, ‘orderGiver’, ‘orderReceiver’, ‘auditor’, ‘beneficiaryMerit’, ‘commemoratedPerson’. ||
|@type|Mandatory|Indicates the role or rank of the person. Sample values: ‘king’, ‘chief’, ‘landlord’, ‘godTemple’, ‘priest’, ‘merchant’, ‘brahminDelegate’, ‘regionalDelegate’, ‘officer’, ‘dancer’, ‘singer’, ‘shepherds’, ‘unknown’. ||
|@xml:id|Optional|Provides a unique identifier for the element bearing the attribute. Must be used if the place name is cut in two by some overlapping tags. ||
|&lt;rs&gt;||||

### S
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;seg&gt;||Segment. Groups one or more strings of text, e.g. words.|4.1.1, 4.1.2, 5.4.4, 5.4.5, 9.2.10, 9.2.14|
|@cert|Optional|Uncertainty or tentativeness of a translated word or sentence. The default value is always ‘low’. ||
|@met|Optional|Sample values in appendix B, table 2 and 3, and "uncertain". (open list) ||
|@rend|Optional|Bitextuality. Value: ‘pun’||
|@subtype|Optional|Can be apply only if @type="component"Sample values: ‘body’, ‘superscript’, ‘subscript’, ‘prescript’, ‘postscript’, ‘consonant’, ‘conjunct’, ‘vowel’. (closed list)||
|@type|Optional|States the type of segmentation. Recommended values: ‘aksara’, ‘component’.||
|&lt;sic&gt;||Contains a passage reproduced as is although apparently incorrect or inaccurate. By EpiDoc convention, this markup is used for text that is legible but does not seem intelligible. Usually accompanied by the &lt;corr&gt; element, in which the editor offers a correction of the text.|6.2.1, 6.2.2, 6.2.5, 6.2.6, 9.2.4, 9.2.10|
|&lt;sourceDesc&gt;||Source description. Mandatory part of the header and describes the source material. Sub-element of &lt;fileDesc&gt;.|1.4, 11.2|
|&lt;space/&gt;||Space is an empty element which indicates a "blank space". DHARMA does not follow regular TEI practice and is not Epic conformant either regarding the attributes. |4.3.1, 4.3.2, 4.3.3, 4.3.4, 4.3.5, 4.3.6, 4.3.7, 4.3.8, 9.2.13|
|@quantity|Mandatory|Indicates approximately the extent of the space. Values refer to the @unit attribute and are thus the number of characters, words, lines, leaves or quires in the manuscript, i.e. ‘1’, ‘2’, ‘3’, and so on.||
|@type|Optional|Classification. Sample value: ‘vacat’, ‘defect’, ‘binding-hole’, ‘descender’, ‘ascender’ (closed list) ||
|@unit|Mandatory|Names the unit used for describing the extent of the space. Sample value:  ‘character’||
|&lt;subst&gt;||Substitution. Wraps the combination of deletion and addition.|4.5.3|
|&lt;summary&gt;||Provides a summary of the parent element.|11.2.1|
|&lt;supplied&gt;||Signifies text supplied by the transcriber, encoder or editor either in place of text which is missing or to clarify a reading.|3.2.3, 5.1, 5.5.1, 5.5.2, 6.2.4, 6.2.5, 6.3.6, 9.2.9, 9.2.10, 9.2.12 |
|@cert|Optional|Indicates a tentative restoration. Sample value: ‘low’. ||
|@evidence|Optional|Indicates a restoration based on something other than conjecture. Sample values: ‘parallel’ and ‘previousEditor’. ||
|@reason|Mandatory|Indicates why the text has been supplied. Sample values: ‘lost’, ’omitted’, ‘subaudible’, ‘undefined’ and ‘explanation’. ||
|&lt;surname&gt;||Contains a family (inherited) name of a person, excluding patronyms and metronyms.|10.5.1|
|&lt;surplus&gt;||Characters were erroneously added by the scribe, and you correct the text by suppressing the superfluous segment.|6.2.3, 6.2.5|

### T
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;TEI&gt;||The element &lt;TEI&gt; must wrap all TEI-compliant content as a root tag.The &lt;TEI&gt; element must contain two sub-elements, &lt;teiHeader&gt; and &lt;text&gt;.|1.4, 10.3.2|
|&lt;teiHeader&gt;||The TEI-based header contains 	additional descriptive information (metadata) about the digital document and is a mandatory component of every TEI document.|1.4, 11|
|&lt;term&gt;||Contains a single-word, multi-word, or symbolic designation which is regarded as a technical term. Use it to wrap a foreign element followed by its translation into a local language that shall be encoded as &lt;gloss&gt;. |7.2.2|
|@xml:lang|Optional|Use this attribute only if the containing text is in a language other than the primary one. Use the 3 letters language code define in Appendix D.||
|&lt;text&gt;||Contains a single text of any kind.|8.1.2|
|@xml:space|Mandatory|Default value must be ‘preserve’||
|&lt;title&gt;||Contains a title for any kind of work.|10.2.1, 10.4.2, 11.1.1|
|@level|Optional|For titles of chapter and articles. Only value possible: ‘a’||
|@rend|Optional|To display the title without italics. Only value: ‘plain’.||
|&lt;titleStmt&gt;||Title statement. Contains information on the title, e|:-----:|:-----:|:-----:|:-----:|ditor and other people who have been responsible for the edition.|1.4, 11.1|

### U
|Elements and attributes|Attributes Use|Contents|Encoding Guide section|
|:-----:|:-----:|:-----:|:-----:|
|&lt;unclear&gt;||Stands in EpiDoc for any character “of which at least traces survive, but not adequately to identify the letter unambiguously outside of its context”.&lt;g&gt; is the only element allowed as child of &lt;unclear&gt;|5.1, 5.3.1, 5.3.2, 5.3.3|
|@cert|Optional|Tentatively legible. Sample value: ‘low’||
|@reason|Optional|When the confidence of a reading is affected not by damage, but by the unusual, awkward or incomplete execution of a glyph by its original engraver. Sample value: ‘eccentric_ductus’. ||
