# ERC-DHARMA, Symbol Taxonomy


## Tall, single vertical bars (daṇḍa)
- for symbols that consist of, or are palaeographically derived from, a single vertical bar that is about as tall as an average character body, use the genus token “danda”
- the transliteration shorthand | stands for <g type="danda">.</g>
- the transliteration shorthand / stands for <g type="dandaOrnate">.</g>
- a <g> element (empty or containing a . character) with a @type starting with “danda” shall be provisionally displayed as |

<!-- model for table:

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

-->
|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
||plain vertical bar|dandaPlain||||
||vertical bar with a hook on top|dandaHooked||||
||vertical bar crossed by a predominantly horizontal line|dandaCross||||
||vertical bar with a headmark or small horizontal line on top|dandaSerif|||tfb-vengicalukya-epigraphy/CalE41-Diggubarru-Bhima2|
||vertical bar with more complex ornamentation|dandaOrnate||||

## Tall, double vertical bars (double daṇḍa)
- for symbols that consist of, or are palaeographically derived from, a double vertical bar as typically used for punctuation in many Indic scripts, use the genus token “ddanda” (for “double daṇḍa”)
- the transliteration shorthand || stands for <g type="ddanda">.</g>
- the transliteration shorthand // stands for <g type="ddandaOrnate">.</g>
- a <g> element (empty or containing a . character) with a @type starting with “ddanda” shall be provisionally displayed as ǁ

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

## Short vertical bars (half daṇḍa)
- for symbols that consist of, or are palaeographically derived from, a short, predominantly vertical bar that may be straight or curved, use the genus token “comma”
- the transliteration shorthand , stands for <g type="comma">.</g>
- a <g> element (empty or containing a . character) with a @type starting with “comma” shall be provisionally displayed as ,

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

## Short horizontal strokes, single and double
- for symbols that consist of, or are predominantly derived from, a single horizontal bar as used for punctuation in some regions and periods, use the genus token “dash”
- the transliteration shorthand ~ stands for <g type="dash">~</g>
a <g> element (empty or containing a . character) with a @type starting with “dash” shall be provisionally displayed as ~

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

## Dots
- for symbols that consist of one or more dots or very small circles and no other marks, use the genus token “dot”
- a <g> element (empty or containing a . character) with a @type starting with “dot” shall be provisionally displayed as °

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

@if we separate rings from dots, ◦ may be used as display for rings and • for dots

## Circles
- for symbols that are circular or have a circle as their most prominent element, use the genus token “circle”
- the transliteration shorthand @ stands for <g type="circle">.</g>
a <g> element (empty or containing a . character) with a @type starting with “circle” shall be provisionally displayed as ◯

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

## Spirals
- for symbols based on a spiral line, use the genus token “spiral”
- a <g> element (empty or containing a . character) with a @type starting with “spiral” shall be provisionally displayed as @

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

## Crosses
- for symbols that consist of, or are predominantly derived from, two straight lines crossing at a right angle, use the genus token “cross”
- a <g> element (empty or containing a . character) with a @type starting with “cross” shall be provisionally displayed as 🞩

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

## Florets
- for symbols resembling stylised flowers, generally consisting of several petals arranged radially around a central circle, use the genus token “floret”
- a <g> element (empty or containing a . character) with a @type starting with “floret” shall be provisionally displayed as ✤

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

## Gomūtra
- for symbols that consist of, or are stylised renderings of, a wavy line of gradually increasing or decreasing amplitude (with or without a squiggle at the widest end), use the genus token “gomutra”
- display suggestion: U+00B6 ¶ Pilcrow Sign; possibly also U+204B ⁋ Reversed Pilcrow Sign so that one of these stands for initial, and the other for final gomūtras

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

**ALTERNATIVE GOMŪTRA CLASSIFICATION, with a bit more detail**

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||

in this alternative, the variants  and  should be reclassified into the genus “circle”, and the variant . should be reclassified into whatever spiral genus we create for these

## Oṁ/Siddham
- siddham, for any variant of the signs discussed by
- Roth, Gustav. 1986. “Mangala-Symbols in Buddhist Manuscripts and Inscriptions.” In Deyadharma: Studies in Memory of Dr. D.C. Sircar, edited by Gouriswar Bhattacharya, 239–49. Sri Garib Dass Oriental Series 33. Delhi: Sri Satguru Publications.
- Sander, Lore. 1986. “Om or Siddham — Remarks on Openings of Buddhist Manuscripts and Inscriptions from Gilgit and Central Asia.” In Deyadharma: Studies in Memory of Dr. D.C. Sircar, edited by Gouriswar Bhattacharya, 239–49. Sri Garib Dass Oriental Series 33. Delhi: Sri Satguru Publications.

## Miscellaneous/unclassified
- symbols that don’t seem to fit any of the numbered species above may be added here
- a <g> element (empty or containing a . character) with a @type that does not start with one of the genus names listed above shall be provisionally displayed as NEED SUGGESTION

|archetype|description|preferred token|specimens|alternative token(s)|remarks, clipping source|
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|||||||
