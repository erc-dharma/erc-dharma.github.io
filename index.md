# ERC-DHARMA, Symbol Taxonomy

1. [Daṇḍa](https://erc-dharma.github.io/danda)
2. [Double daṇḍa](https://erc-dharma.github.io/doubledanda)
3. [Half daṇḍa](https://erc-dharma.github.io/halfdanda)
4. [Short horizontal strokes](https://erc-dharma.github.io/horizontalstrokes)
5. [Dots](https://erc-dharma.github.io/dots)
6. [Circles](https://erc-dharma.github.io/circles)
7. [Spirals](https://erc-dharma.github.io/spirals)
8. [Crosses](https://erc-dharma.github.io/crosses)
9. [Florets](https://erc-dharma.github.io/florets)
10. [Gomūtra](https://erc-dharma.github.io/gomutra)
11. [Oṁ/Siddham](https://erc-dharma.github.io/siddham)
12. [Miscellaneous](https://erc-dharma.github.io/miscellaneous)


## Preliminary Remarks
- as indicated in EGD §4.2 (to which we refer for further details), the use of a <g> tag is mandatory on all symbol characters
- when the function of a symbol is confidently established, this tag shall be used as a wrapper which qualifies a transliteration character (that in turn represents a symbol):
- if it is a punctuation mark in the narrow sense, then <g> wraps the character . (period, full stop), representing an abstract punctuation mark
- if it is a space filler, then <g> wraps the character § representing an abstract space filler
- when the function of a (non-numeral) symbol is not clearly one of the above, then the same tag shall be used as an empty element which represents and qualifies a symbol
- in all of the above cases, <g> mandatorily takes the attribute @type for encoding the physical appearance of the symbol character
- the values available for @type, hereafter referred to as “(symbol) tokens”, are at present not constrained, except by the following practical considerations:
- for the sake of XML validity, a token must not contain a space
- for the sake of simplicity, a token should preferably not contain characters other than letters of the English alphabet and numerals, and should only include uppercase letters to mark the initials of second or subsequent words within a token (camelCase)
- our long-term goal is to gather the symbol tokens used by encoders and use it as a starting point for the creation of a constrained list for symbol classification
- to facilitate this, it is strongly recommended that you consult this Supplement whenever you encode a symbol, and
- whenever possible, use a token recommended herein for symbols resembling your symbol in shape
- whenever you find no symbol listed here that is close enough in shape to yours, choose one of the primary categories (“genus”) introduced here and, if you feel that more detail is warranted, create a new secondary token (“species”) under that for your symbol
- if possible, add a clipping of symbols you encounter to enrich this Supplement (see below about how to contribute)

## A Hierarchical Taxonomy of Symbols
- eventually, we intend to classify symbols by using a limited number of values for @type and a likewise limited number of permitted values of @subtype for each @type
- with this aim in mind, we shall attempt already at this stage to describe symbols in this hierarchical manner, but without constraints on permitted values and with the hierarchy compressed into a single token, using camelCase to segment the token into “genus” and “species” (and optional “subspecies”) as a precursor to future @type and @subtype
- thus, when encoding a symbol, proceed in the following steps:
- see if it can be classified as a variety of one of the numbered species described in the following subsections
- if it can, proceed to step 2
- if it cannot, because it is indistinct, encode it as per “Unclear symbols” below
- if it cannot, because it is a radically different shape, assign it a genus of your choice, comparing it to specimens already recorded under “Miscellaneous” below
- use the selected genus name as the token for your symbol
- classifying symbols by genus is sufficient: there is no obligation to add a species name
- so you may stop at this step and encode e.g. <g type="floret"/>
- species names should generally be used if a particular symbol is not a typical representative of the genus as a whole, but they may be used at any time when you think encoding this level of detail is advantageous enough to be worth the trouble
- if you deem that a species name should be used for more accurate classification, proceed to step 3
- have a look at the specimens below for the genus you have selected and see if any of them are a close enough match for your particular symbol
- if yes, choose the species name listed as preferred for that specimen, and add it to your token with a capital initial
- you may stop at this step and encode e.g. <g type="floretComplex"/>
- if not, you may do either of the following:
- create a new species name for your symbol and use that, e.g. <g type="floretSixpetalled"/>
- choose a roughly similar species name from what is already listed below, and add a “subspecies”, again with a capital initial, after the species name, e.g. <g type="floretComplexDottedcircle"/>
- always keep in mind that the diversity of actual symbols can never be fully represented in a classification scheme and you should not attempt to create tokens that provide an accurate and detailed description of symbols
- thus, while it is possible and permitted to create tokens more complex than the above (adding sub-subspecies, etc.), it is recommended that you never go beyond the subspecies level (i.e. three components in your token) and generally stop at the species level (two components in your token)
- an accurate and detailed human-readable description can, and for unusual symbols should, be recorded in the Hand Description section of your TEI header (EGD §11.2/The Hand Description)

## Using the Tables
- each of the numbered subsections concerns one “approved” symbol genus, containing
- a description of the significant features or criteria on the basis of which a symbol can be allocated to that genus
- some notes on encoding shorthand and display
- a table of species (and potential subspecies) belonging to that genus
- each primary row of the tables contains one “approved” symbol species or subspecies, described using the following columns
- archetype: an image that we consider to be a typical form of the subspecies or species concerned
- this image may be a clipping from a facsimile, a drawing, or it may (especially at this early stage) be missing
- description: a concise description of what we consider to be the significant features or criteria on the basis of which a symbol can be allocated to that species or subspecies
- preferred token: the “approved” token to use for that species or subspecies
- specimens: where available, this cell contains one or more specimens encoded as that species or subspecies
- each specimen is recorded in a new row within the primary row, and numbered for reference
- alternative tokens: this cell will contain tokens that have previously been used for symbols to which we have assigned a new preferred token
- if you have already encoded a symbol with one of the tokens listed here as “alternative”, there is no obligation to change your encoding to the preferred token, but newly encoded symbols should receive the preferred token
- if we have a specimen of the actual symbol encoded with one of the alternative tokens, then the alternative token will have a number indicating the number of the corresponding specimen in the previous column
- remarks, clipping source
- this column may contain further notes about the actual species or subspecies
- this is also the place where the source (DHARMA repository and filename) of specimens may be recorded, numbered to indicate the corresponding specimen

## Contributing to the Tables
- when you encode a symbol using a genus, species or subspecies already featured in the tables below, it is generally not necessary to add anything to the tables
- but if the tables do not already have a specimen for the species or subspecies that you use, or if your symbol looks quite different from the specimen(s) already featured, then it would be appreciated if you could create a clipping of your symbol and add it to the table
- when you choose to employ a species or subspecies not already listed in the tables below, then
- mandatorily create a new row in the table pertaining to the genus of your token, and record your new species or subspecies there
- optionally add a clipping
- to add a new species or subspecies to the table,
- create a new row at the end of the table for a new species, or below the applicable species for a new subspecies
- write a description for your (sub)species, making an effort to summarise its most salient features concisely
- add the token you have used for that symbol as the preferred token for the new (sub)species
- if possible, add a clipping of your symbol as a specimen
- to add a specimen to a pre-existing row or one that you have just created,
- create a clipping of your specimen
- add it to the column “specimens”, giving it the number 1 or, if there are already specimens in the table for the applicable (sub)species, the next higher available number
- under “remarks”, record the repository and filename of the inscription from which your symbol has been taken, and give this record the same number as that given to the specimen
- optionally, especially for long inscriptions, also record the line number from which the clipping was taken
- there is no need to record the name of the image file from which your clipping comes
- to create a clipping, use any image processing software you are familiar with
- as far as possible, choose an instance of your symbol that is clear and typical of its kind
- clip the symbol from your digital surrogate, and if possible, include one or two alphabetic characters before and/or after the symbol so its relative size and position can be seen in the clipping
- if your surrogate has a very high resolution, preferably reduce the size of your clipping so that it is no more than 200 pixels in height
- but feel free to use larger images if you cannot manage reducing it
- do not enlarge your clipping if it is smaller in size to begin with
- if possible, save your clipping as a PNG file (your graphic editor will probably be able to do that) before inserting it into this document
- but if saving as PNG is a problem, do not worry and use whatever image format you can handle (though if you must save as JPG, do try to avoid high compression and choose high quality instead)
- our plan is that the tables will be reviewed every now and then, in the course of which we may ask you for further information/clarification on your contributions; moreover,
- descriptions provided by you may be rephrased (to make them clearer or improve their English), and
- new (sub)species created by you may be merged into other (sub)species, or the preferred token suggested by you may be overruled by a different token
- in this case, the token originally suggested by you will be relegated to the status of an alternative token
