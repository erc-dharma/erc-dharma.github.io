## Multiple symbols

when several symbols (of a different kind, the same kind, or any combination) appear together, create a separate <g/> element for each symbol
the only exception to this rule of thumb is the double daṇḍa which, as covered under 2 above, is often a special sign (i.e. different from two separata daṇḍas) and is therefore normally encoded as a single <g/> element
when multiple signs are used together, there is usually no need to add a . within any of the <g/> elements involved in the encoding, since such combinations are not normally used for punctuation in the narrow sense (as defined in EGD §4.2.4)
but if it is your judgement that such a combination serves for punctuation, then free to include a . character within any or all of the <g/> elements involved
for example, the symbols in the image on the right may be encoded as follows:
<g type="dandaSerif"/><g type="dandaSerif"/><g type="dandaSerif"/><g type="circleLarge"/><g type="dandaSerif"/><g type="dandaSerif"/><g type="dandaSerif"/><g type="circleSmall"/><g type="gomutraFinal"/>
