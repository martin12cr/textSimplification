# GeoSimp Annotation and Simplification Manual

**Classifying discourse segments by linguistic complexity and simplifying texts for blind and low-vision screen reader users**

This is the annotation manual used by the four professional philologists who built the GeoSimp dataset: it defines the 21 linguistic complexity attributes they identified in each discourse segment and the guideline they applied when producing the simplified version.

## About this document

**Dataset.** GeoSimp — a Spanish-language dataset for automatic text simplification, comprising discourse segments drawn from articles published in the *Revista Geológica de América Central* under a CC BY-NC-SA 3.0 licence.

**Repository.** <https://github.com/martin12cr/textSimplification>

**Permanent archive.** Zenodo, DOI [10.5281/zenodo.21516742](https://doi.org/10.5281/zenodo.21516742)

**Data article.** N. Pérez-Rojas, M. Solís, S. Calderón-Ramírez, M. Arias-Monge, H. Saggion, and D. Xie-Li, "A Step Toward Inclusion: A Transparent Dataset for Automatic Text Simplification for Screen Reader Users," *Data in Brief* (submitted).

**Provenance of the scheme.** Twenty of the 21 attributes derive from the SIMPLEXT manual: A. Anula, *Pautas básicas de simplificación textual y diseño del corpus SIMPLEXT*, Grupo DILES, Universidad Autónoma de Madrid, Tech. Rep., 2011. The exception is attribute 3, **Visual Reference Dependence**, which has no counterpart in SIMPLEXT and was introduced in N. Pérez-Rojas et al., "A Novel Spanish Dataset for Financial Education Text Simplification Targeting Visually Impaired Individuals," *IEEE Access*, 2025, because of the profile of the intended readership.

**Licence.** CC BY-NC-SA 3.0, matching the licence of the source texts from which the dataset was derived.

## How to read this manual

Each entry gives the attribute code, its canonical English label, and the original Spanish label in italics. The two fields that follow — how the attribute appears in the original text, and the simplification guideline — are translations of the two corresponding columns of the source manual, with every conditional qualifier preserved.

**The examples are not translated.** They are Spanish sentences that demonstrate grammatical phenomena which either do not exist in English or do not behave the same way: the gerund, the compound subjunctive, the *pretérito anterior*, relative *cuyo*, non-canonical constituent order. Translating them would destroy the evidence for the rule. Each example is therefore given in the original Spanish, exactly as written, followed by a functional gloss in English marked `EN:`. The gloss conveys the content; it does not reproduce the phenomenon. Where a phenomenon has no English counterpart, a *Note* states what changed in the Spanish.

**Coding in the dataset.** In the `attributes` column of `GeoSimp_train.xlsx` and the `attribute_*` columns of `GeoSimp_test.xlsx`, attributes are recorded as codes separated by a hyphen. A code is repeated as many times as the attribute occurs in the segment: a segment showing attributes 2, 3 and 17, with attribute 2 occurring twice, is coded `2-3-2-17`. The code `0` marks a segment in which no complexity attribute was identified. Attributes 8 and 9 are subdivided below for descriptive purposes, but every subtype is coded simply as `8` or `9`.

---

## Contents

| Code | Attribute |
|---|---|
| 1 | [Word Frequency](#1-word-frequency) |
| 2 | [Abstract vs. Concrete Language](#2-abstract-vs-concrete-language) |
| 3 | [Visual Reference Dependence](#3-visual-reference-dependence) |
| 4 | [Ambiguity in Word Meaning](#4-ambiguity-in-word-meaning) |
| 5 | [Unnecessary Words](#5-unnecessary-words) |
| 6 | [Multiword Lexical Expressions](#6-multiword-lexical-expressions) |
| 7 | [Use of Nominalizations](#7-use-of-nominalizations) |
| 8 | [Conjunctions](#8-conjunctions) (8a–8d) |
| 9 | [Subordinating Conjunctions](#9-subordinating-conjunctions) (9a–9f) |
| 10 | [Compound Indicative Tenses](#10-compound-indicative-tenses) |
| 11 | [Subjunctive Mood Verb Forms](#11-subjunctive-mood-verb-forms) |
| 12 | [Use of the Gerund](#12-use-of-the-gerund) |
| 13 | [Abbreviations-Shortenings](#13-abbreviations-shortenings) |
| 14 | [Use of Numerical Expressions](#14-use-of-numerical-expressions) |
| 15 | [Sentence Length](#15-sentence-length) |
| 16 | [Parenthetical Insertions](#16-parenthetical-insertions) |
| 17 | [Relative Clauses](#17-relative-clauses) |
| 18 | [Sentences of Formal and Aesthetic Use](#18-sentences-of-formal-and-aesthetic-use) |
| 19 | [Non-Canonical Constituent Order](#19-non-canonical-constituent-order) |
| 20 | [Common Discourse Markers](#20-common-discourse-markers) |
| 21 | [Use of Complex Punctuation Marks](#21-use-of-complex-punctuation-marks) |

---

## 1. Word Frequency

*(Frecuencia léxica)*

**How the attribute appears in the original text:** Infrequent, archaic, or dialectal words are used. Reference resource: the *Corpus de Referencia del Español Actual* (CREA) of the Real Academia Española.

**Simplification guideline:** Replace low-frequency, archaic, or dialectal words with commonly used words or words belonging to "standard Spanish".

**Complex segment:** *La muestra fue sometida a un análisis pormenorizado en el laboratorio de petrología.*
`EN: The sample underwent a detailed analysis in the petrology laboratory.`

**Simplified segment:** *La muestra fue sometida a un análisis detallado en el laboratorio de petrología.*
`EN: Same content; the low-frequency adjective is replaced by an everyday equivalent.`

---

## 2. Abstract vs. Concrete Language

*(Abstracción léxica e imaginabilidad)*

**How the attribute appears in the original text:** Words with abstract referents are used, that is, words that do not designate a material reality. Words with referents that are difficult to visualize, or with low semantic weight, are used.

**Simplification guideline:** Where possible, replace words with abstract or hard-to-visualize referents with words that have concrete or imaginable referents. If the word occurs within an idea that is unnecessary for conveying the message, it may be deleted.

**Complex segment:** *La manifestación de la actividad volcánica fue registrada por los investigadores.*
`EN: The manifestation of volcanic activity was recorded by the researchers.`

**Simplified segment:** *La actividad volcánica fue registrada por los investigadores.*
`EN: The abstract head noun is removed; the concrete event remains.`

---

## 3. Visual Reference Dependence

*(Dependencia de referencias visuales)*

**How the attribute appears in the original text:** Visual references are used to convey the message. Comprehension of the discourse segment depends on the sense of sight.

**Simplification guideline:** Where possible, replace discourse segments that contain visual references. If the word occurs within an idea that is unnecessary for conveying the message, it may be deleted.

**Complex segment:** *Como se observa en la figura 3, las capas sedimentarias presentan una inclinación hacia el este.*
`EN: As can be seen in figure 3, the sedimentary layers dip towards the east.`

**Simplified segment:** *Las capas sedimentarias presentan una inclinación hacia el este.*
`EN: The appeal to the figure is removed; the propositional content is unchanged.`

*Note:* This is the one attribute with no counterpart in SIMPLEXT. It was introduced for readers who receive the text as an audio stream, in which references to page layout have nothing to point to.

---

## 4. Ambiguity in Word Meaning

*(Ambigüedad léxica)*

**How the attribute appears in the original text:** Polysemous words are used in their secondary senses.

**Simplification guideline:** Use polysemous words in their primary senses. Replace polysemous words with terms that have a less ambiguous meaning.

**Complex segment:** *Los investigadores abordaron el estudio de la formación rocosa.*
`EN: The researchers took up the study of the rock formation.`

**Simplified segment:** *Los investigadores iniciaron el estudio de la formación rocosa.*
`EN: A verb used in a secondary sense is replaced by one whose primary sense fits.`

*Note:* Spanish *abordar* primarily means "to board" a vessel; the sense required here is a secondary one, which is what the attribute marks.

---

## 5. Unnecessary Words

*(Palabras superfluas)*

**How the attribute appears in the original text:** Words or phrases are used that are not absolutely necessary for conveying the message. Particular stylistic preferences are favoured that reduce concision and precision.

**Simplification guideline:** Delete words and phrases that are not necessary in order to understand the message of the text.

**Complex segment:** *Cabe destacar que, debido a las razones previamente mencionadas, el magma ascendió a través de la corteza terrestre.*
`EN: It is worth noting that, for the reasons mentioned above, the magma rose through the earth's crust.`

**Simplified segment:** *El magma ascendió a través de la corteza terrestre.*
`EN: Both framing expressions are removed.`

---

## 6. Multiword Lexical Expressions

*(Expresiones léxicas complejas)*

**How the attribute appears in the original text:** Complex lexical expressions are used, formed by groups of words that function as a single grammatical category (phraseological units, locutions, idioms).

**Simplification guideline:** Replace these multiword expressions with their single-word equivalents.

**Complex segment:** *El sismo tuvo lugar en horas de la madrugada.*
`EN: The earthquake took place in the early hours of the morning.`

**Simplified segment:** *El sismo ocurrió en la madrugada.*
`EN: The light-verb construction is replaced by a single verb, and the periphrastic time expression is shortened.`

---

## 7. Use of Nominalizations

*(Nominalizaciones)*

**How the attribute appears in the original text:** Nominalizations are used to express states, processes, or actions, particularly in combination with non-canonical constituent order or parenthetical insertions.

**Simplification guideline:** Replace nominalizations with the verbs that express the same states, processes, and actions.

**Complex segment:** *Con la observación detallada de las capas estratigráficas, realizada por el equipo de geólogos, se logró la identificación de cambios en el ambiente deposicional.*
`EN: Through the detailed observation of the stratigraphic layers, carried out by the team of geologists, the identification of changes in the depositional environment was achieved.`

**Simplified segment:** *El equipo de geólogos observó detalladamente las capas estratigráficas e identificó cambios en el ambiente deposicional.*
`EN: Both nominalizations become finite verbs and the agent becomes the subject.`

---

## 8. Conjunctions

*(Conjunciones coordinativas)*

This attribute covers four subtypes, described separately below. All four are coded as `8` in the dataset.

### 8a. Coordinating conjunctions

*(Conjunciones coordinativas)*

**How the attribute appears in the original text:** Adverbs and prepositions with conjunctive value are used: *"además de"*, *"tanto… como"*.

**Simplification guideline:** Use the conjunctions *"y"* and *"ni"* by preference. However, the substitution is not necessary in short statements, or in statements where no other attributes that make the text difficult are present.

**Complex segment:** *Tanto la presión tectónica como la actividad volcánica contribuyen a la formación de montañas.*
`EN: Both tectonic pressure and volcanic activity contribute to mountain formation.`

**Simplified segment:** *La presión tectónica y la actividad volcánica contribuyen a la formación de montañas.*
`EN: The discontinuous correlative is replaced by simple coordination.`

*Note:* *"tanto… como"* is a discontinuous correlative: its two parts frame the coordinated elements and only function together.

### 8b. Disjunctive coordination

*(Coordinativas disyuntivas)*

**How the attribute appears in the original text:** Expressions such as *"o bien… o bien"*, *"tan pronto como"* are used.

**Simplification guideline:** Use the conjunction *"o"*. However, it is recommended to modify only when the marker is of infrequent use, or when the style used is insufficiently explanatory for a natural sciences text.

**Complex segment:** *El sismo pudo haberse originado o bien por la reactivación de una falla antigua, o bien por la acumulación de presión en el manto superior.*
`EN: The earthquake may have originated either from the reactivation of an old fault or from the build-up of pressure in the upper mantle.`

**Simplified segment:** *El sismo pudo haberse originado por la reactivación de una falla antigua o por la acumulación de presión en el manto superior.*
`EN: The correlative is reduced to a single conjunction.`

### 8c. Adversative coordination

*(Coordinativas adversativas)*

**How the attribute appears in the original text:** Complex forms are used to express adversative coordination, such as *"sin embargo"*, *"no obstante"*, *"con todo"*, *"por el contrario"*, *"en cambio"*, *"antes bien"*, *"sino más bien (al contrario)"*.

**Simplification guideline:** Use the conjunction *"pero"* in affirmative constructions and *"sino"* in negative constructions. However, it is recommended to modify only when the marker is of infrequent use, or when the style used is insufficiently explanatory for a natural sciences text.

**Complex segment:** *El modelo no busca predecir eventos sísmicos con precisión, sino más bien ofrecer una herramienta para evaluar el riesgo geológico.*
`EN: The model does not seek to predict seismic events precisely, but rather to offer a tool for assessing geological risk.`

**Simplified segment:** *El modelo no busca predecir eventos sísmicos con precisión, sino ofrecer una herramienta para evaluar el riesgo geológico.*
`EN: The reinforced adversative is reduced to the simple form.`

### 8d. Other coordinating links

*(Otros enlaces de coordinación)*

**How the attribute appears in the original text:** Constructions close to discourse markers are used, such as *"es decir que"*, *"esto es"*, *"o sea que"*, and similar.

**Simplification guideline:** Modify these coordinating links only when the marker is of infrequent use, or when the style used is insufficiently explanatory for a natural sciences text.

**Complex segment:** *Las capas se depositaron en ambientes marinos poco profundos, es decir que se formaron cerca de la costa.*
`EN: The layers were deposited in shallow marine environments, that is to say that they formed near the coast.`

**Simplified segment:** *Las capas se depositaron en ambientes marinos poco profundos, es decir, se formaron cerca de la costa.*
`EN: The link is reduced to its plain form and the clause boundary is marked by a comma.`

---

## 9. Subordinating Conjunctions

*(Partículas subordinantes)*

This attribute covers six subtypes, described separately below. All six are coded as `9` in the dataset.

### 9a. Relative subordinating particles

*(Partículas subordinantes relativas)*

**How the attribute appears in the original text:** Particles such as *"cuyo"*, *"el cual"* or *"el que"* and their variants are used instead of *"quien"* and *"que"*.

**Simplification guideline:** Use the simple relative forms *"que"*, *"quien"* and *"cuanto"*. Replace the form *"cuyo"*.

**Complex segment:** *La falla, la cual atraviesa toda la cordillera, ha sido objeto de múltiples estudios.*
`EN: The fault, which crosses the entire mountain range, has been the subject of many studies.`

**Simplified segment:** *La falla, que atraviesa toda la cordillera, ha sido objeto de múltiples estudios.*
`EN: The heavy relative is replaced by the simple relative.`

*Note:* Spanish distinguishes several relative forms where English has one *which*; the alternation between *el cual* and *que* has no equivalent in English, and *cuyo* is a possessive relative determiner that agrees with the possessed noun.

### 9b. Temporal subordinating particles

*(Partículas subordinantes temporales)*

**How the attribute appears in the original text:** Complex forms such as *"una vez que"*, *"una vez cuando"*, *"en el momento que"*, and similar, are used.

**Simplification guideline:** Use *"cuando"* and *"mientras"* by preference.

**Complex segment:** *Una vez que las rocas alcanzan la temperatura de fusión, comienzan a formar magma.*
`EN: Once the rocks reach melting temperature, they begin to form magma.`

**Simplified segment:** *Cuando las rocas alcanzan la temperatura de fusión, comienzan a formar magma.*
`EN: The complex temporal connector is replaced by the simple one.`

### 9c. Locative subordinating particles

*(Partículas subordinantes locativas)*

**How the attribute appears in the original text:** Complex forms such as *"lugar donde"* are used.

**Simplification guideline:** Use *"donde"*.

**Complex segment:** *Los fósiles fueron hallados en un lugar donde hubo actividad volcánica hace millones de años.*
`EN: The fossils were found in a place where there was volcanic activity millions of years ago.`

**Simplified segment:** *Los fósiles fueron hallados donde hubo actividad volcánica hace millones de años.*
`EN: The redundant head noun is removed and the bare relative adverb is used.`

### 9d. Modal subordinating particles

*(Partículas subordinantes modales)*

**How the attribute appears in the original text:** Complex forms such as *"según como"*, *"tal como"* are used.

**Simplification guideline:** Use *"como"* and *"según"*.

**Complex segment:** *La lava se solidificó de forma irregular, tal como lo muestran las formaciones basálticas.*
`EN: The lava solidified irregularly, just as the basaltic formations show.`

**Simplified segment:** *La lava se solidificó de forma irregular, como lo muestran las formaciones basálticas.*
`EN: The reinforced comparative connector is reduced to the simple one.`

### 9e. Conditional subordinating particles

*(Partículas subordinantes condicionales)*

**How the attribute appears in the original text:** Complex forms such as *"a condición de que"*, *"excepto que"*, *"en caso de (que)"*, *"siempre que"*, *"siempre y cuando"*, *"solo si"* are used.

**Simplification guideline:** Use *"si"*, *"por si"*, provided that logical expressions important for natural sciences texts are not affected.

**Complex segment:** *La erupción podría afectar la zona costera, en caso de que los vientos se dirijan hacia el oeste.*
`EN: The eruption could affect the coastal area, in the event that the winds blow towards the west.`

**Simplified segment:** *La erupción podría afectar la zona costera si los vientos se dirigen hacia el oeste.*
`EN: The complex conditional connector is replaced by the simple one, and the verb shifts from subjunctive to indicative.`

*Note:* The qualifier in the guideline is substantive: connectors such as *solo si* and *siempre y cuando* encode necessary versus sufficient conditions, and collapsing them into *si* would change the logical content of a scientific claim.

### 9f. Concessive subordinating particles

*(Partículas subordinantes concesivas)*

**How the attribute appears in the original text:** Complex forms such as *"aun cuando"*, *"a riesgo de que"*, *"ni siquiera si"*, *"pese a que"*, *"por más/mucho/poco/ que"*, *"si bien"*, *"tanto si… como si"* are used.

**Simplification guideline:** Use *"aunque"*, or other frequently used forms such as *"a pesar de que"* and *"incluso cuando"*.

**Complex segment:** *Las rocas sedimentarias pueden conservar fósiles, pese a que hayan estado sometidas a presión.*
`EN: Sedimentary rocks can preserve fossils, despite having been subjected to pressure.`

**Simplified segment:** *Las rocas sedimentarias pueden conservar fósiles, aunque hayan estado sometidas a presión.*
`EN: The complex concessive connector is replaced by the most frequent one.`

---

## 10. Compound Indicative Tenses

*(Formas personales de indicativo)*

**How the attribute appears in the original text:** The *pretérito anterior* and the *futuro compuesto* are used.

**Simplification guideline:** Use the *presente*, *pretérito perfecto simple*, *pretérito imperfecto*, *futuro simple*, *condicional simple*, *pretérito perfecto compuesto*, *pretérito pluscuamperfecto*, and *condicional compuesto*.

**Complex segment:** *Cuando el magma hubo ascendido, se fracturó la corteza terrestre.*
`EN: Once the magma had risen, the earth's crust fractured.`

**Simplified segment:** *Cuando el magma ascendió, se fracturó la corteza terrestre.*
`EN: The same sequence of events, expressed with a simple past.`

*Note:* The *pretérito anterior* (*hubo ascendido*) has no English equivalent. It is not the past perfect, which corresponds to the Spanish *pluscuamperfecto* (*había ascendido*) and is expressly permitted by the guideline. The *pretérito anterior* marks an event immediately preceding another past event and is largely confined to formal written Spanish, which is why it is treated as a source of difficulty.

---

## 11. Subjunctive Mood Verb Forms

*(Formas personales de subjuntivo)*

**How the attribute appears in the original text:** The subjunctive is used in its compound forms.

**Simplification guideline:** Restrict the subjunctive to its *presente*, *pretérito imperfecto*, *futuro simple*, and *pretérito pluscuamperfecto* forms.

**Complex segment:** *Es posible que las rocas se hubieren desplazado por efecto del sismo.*
`EN: It is possible that the rocks shifted as a result of the earthquake.`

**Simplified segment:** *Es posible que las rocas se hayan desplazado por efecto del sismo.*
`EN: The same content, in a form that is current in present-day Spanish.`

*Note:* English has no morphological subjunctive comparable to the Spanish paradigm. The complex example uses the *futuro compuesto de subjuntivo* (*hubieren desplazado*), a form effectively obsolete outside legal and liturgical registers, which is what makes it a source of difficulty here.

---

## 12. Use of the Gerund

*(Formas no personales)*

**How the attribute appears in the original text:** The gerund form is used.

**Simplification guideline:** Replace gerund forms in the statement.

**Complex segment:** *El agua infiltró las grietas, disolviendo minerales presentes en la roca.*
`EN: Water seeped into the cracks, dissolving minerals present in the rock.`

**Simplified segment:** *El agua infiltró las grietas y disolvió los minerales presentes en la roca.*
`EN: The subordinate non-finite clause becomes a coordinated finite clause.`

**Simplified segment (second example):** *Las placas tectónicas se desplazan lentamente y esto provoca una acumulación de tensión.*
`EN: Tectonic plates move slowly and this causes a build-up of stress.`

*Note:* The Spanish *gerundio* is not the English gerund. English *-ing* forms function as nouns in gerund use; the Spanish *gerundio* is an adverbial non-finite form that attaches a secondary predication to a main clause, and its scope is often indeterminate — which is the difficulty the attribute captures.

---

## 13. Abbreviations-Shortenings

*(Abreviaturas, acortamientos, siglas y acrónimos)*

**How the attribute appears in the original text:** Abbreviations, clippings, initialisms, and acronyms are used.

**Simplification guideline:** Use full expressions instead of abbreviations, clippings, initialisms, and acronyms.

**Complex segment:** *La muestra fue analizada con un equipo de espectroscopía FTIR.*
`EN: The sample was analysed with an FTIR spectroscopy instrument.`

**Simplified segment:** *La muestra fue analizada con un equipo de espectroscopía por infrarrojo por transformada de Fourier.*
`EN: The initialism is expanded into its full Spanish name.`

*Note:* This attribute is the most frequent in the dataset. Speech synthesizers resolve abbreviated forms inconsistently — the same string may be pronounced as a word, spelled out, or both — so expansion serves the listening situation even though it lengthens the segment.

---

## 14. Use of Numerical Expressions

*(Expresiones numéricas)*

**How the attribute appears in the original text:** Numerical expressions are used (numbers, decimals).

**Simplification guideline:** Write numerical expressions in words.

> **Exception:** Years must not be modified, either in running text or in bibliographic references.

**Complex segment:** *El espesor de la capa sedimentaria alcanza los 12,7 metros en algunas zonas.*
`EN: The thickness of the sedimentary layer reaches 12.7 metres in some areas.`

**Simplified segment:** *El espesor de la capa sedimentaria alcanza los doce metros con setenta centímetros en algunas zonas.*
`EN: The decimal is rewritten in words and re-expressed as metres and centimetres.`

*Note:* Spanish uses the comma as decimal separator, so *12,7* is twelve point seven. The simplified version also converts the decimal fraction into a second unit, which is a rendering choice specific to the audio reading situation.

---

## 15. Sentence Length

*(Extensión de los segmentos discursivos)*

**How the attribute appears in the original text:** Segments of more than 20 words are used.

**Simplification guideline:** Use segments of 20 words or fewer. Where possible, it is recommended to divide the discourse segment into several segments.

**Complex segment:** *Las capas de sedimento se depositaron durante miles de años a partir de procesos aluviales, eólicos y volcánicos, lo que permitió la formación de suelos con diferentes características físicas y químicas según la región.*
`EN: The sediment layers were deposited over thousands of years through alluvial, aeolian, and volcanic processes, which allowed the formation of soils with different physical and chemical characteristics depending on the region.`

**Simplified segment:** *Las capas de sedimento se depositaron durante miles de años por procesos aluviales, eólicos y volcánicos. Estos procesos permitieron la formación de suelos con distintas características físicas y químicas según la región.*
`EN: The segment is split in two, and the resumptive noun phrase replaces the relative link.`

---

## 16. Parenthetical Insertions

*(Incisos)*

**How the attribute appears in the original text:** Parenthetical insertions are used to characterize subjects and to add information, but this produces complex syntax.

**Simplification guideline:** Reserve their use for cases in which they are indispensable for understanding the message. Replace them by means of a coordination or juxtaposition strategy.

**Complex segment:** *El magma, al ascender por la corteza terrestre, generó una serie de fracturas.*
`EN: The magma, as it rose through the earth's crust, generated a series of fractures.`

**Simplified segment:** *El magma ascendió por la corteza terrestre y generó una serie de fracturas.*
`EN: The intercalated clause becomes the first of two coordinated clauses.`

*Note:* The Spanish *inciso* is broader than an English parenthetical phrase: it covers appositions, intercalated non-finite clauses, and any element that interrupts the main clause. The example here is a non-finite adverbial clause, not a phrase.

---

## 17. Relative Clauses

*(Cláusulas relativas)*

**How the attribute appears in the original text:** Several subordinate clauses are used within a single statement.

**Simplification guideline:** Reduce the number of relative clauses per statement (maximum one).

**Complex segment:** *Se publicó un estudio sobre las fallas activas que atraviesan la región, las cuales podrían generar sismos que afecten las comunidades que habitan en zonas cercanas.*
`EN: A study was published on the active faults crossing the region, which could generate earthquakes affecting the communities living in nearby areas.`

**Simplified segment:** *Se publicó un estudio sobre las fallas activas de la región, con riesgo de generar sismos que afecten a las comunidades cercanas.*
`EN: Three of the four relative clauses are replaced by modifiers, leaving one.`

**Simplified segment (second option):** *Se publicó un estudio sobre las fallas activas de la región. Estas fallas podrían generar sismos y afectar a las comunidades cercanas.*
`EN: The same content, split into two statements with no relative clause.`

---

## 18. Sentences of Formal and Aesthetic Use

*(Otras construcciones oracionales)*

**How the attribute appears in the original text:** Passive, impersonal, absolute, and negative syntactic constructions are used, along with rhetorical questions, exclamative constructions with emphatic definite articles, expressions in indirect discourse, and topic and focus constructions, among others, **in interaction with other attributes that make the text difficult**.

**Simplification guideline:** Modify the use of these constructions when they are employed solely for stylistic or aesthetic reasons.

**Complex segment:** *La deformación de la corteza fue causada por la presión acumulada a lo largo de la falla.*
`EN: The deformation of the crust was caused by the pressure accumulated along the fault.`

**Simplified segment:** *La presión acumulada a lo largo de la falla causó la deformación de la corteza.*
`EN: The passive becomes active, and the agent becomes the subject.`

*Note:* The condition set in bold is part of the attribute definition, not of the guideline: constructions of this kind are annotated when they combine with other sources of difficulty, not whenever they occur. Passive and impersonal constructions are standard in scientific Spanish and are not marked in isolation.

---

## 19. Non-Canonical Constituent Order

*(Orden de constituyentes de la oración)*

**How the attribute appears in the original text:** The SVO order and other prototypical orders of the language are altered.

**Simplification guideline:** Use the SVO order and other prototypical orders of the language by preference.

**Complex segment:** *En la región andina identificaron los geólogos múltiples fallas activas.*
`EN: In the Andean region, geologists identified multiple active faults.`

**Simplified segment:** *Los geólogos identificaron múltiples fallas activas en la región andina.*
`EN: Subject, verb, object, then the locative adjunct.`

*Note:* Spanish permits constituent orders that are ungrammatical in English. The complex example places a fronted adjunct before the verb and the subject after it, an order English cannot reproduce, so the gloss necessarily restores the canonical order and the contrast is visible only in the Spanish.

---

## 20. Common Discourse Markers

*(Marcadores discursivos de uso preferente)*

**How the attribute appears in the original text:** Markers that are uncommon in the cultural context are used.

**Simplification guideline:** Use the markers most frequently used in the cultural context. Use simple markers rather than compound ones.

**Complex segment:** *La actividad sísmica se ha incrementado; no obstante, no se han reportado daños estructurales.*
`EN: Seismic activity has increased; nevertheless, no structural damage has been reported.`

**Simplified segment:** *La actividad sísmica se ha incrementado, pero no se han reportado daños estructurales.*
`EN: The formal marker is replaced by the everyday conjunction, and the semicolon disappears with it.`

*Note:* "Uncommon in the cultural context" refers to frequency in the variety of Spanish used by the intended readership, not to frequency in the language as a whole.

---

## 21. Use of Complex Punctuation Marks

*(Signos de puntuación de uso complejo)*

**How the attribute appears in the original text:** Semicolons, square brackets, dashes, single quotation marks, and angle quotation marks are used.

**Simplification guideline:** Remove the use of semicolons, square brackets, dashes, single quotation marks, and angle quotation marks.

> **Exception:** A semicolon is not replaced by a full stop when the linguistic units it separates are words or phrases, that is, when it separates the items of a lexical enumeration.

**Complex segment:** *El geólogo observó varias capas de ceniza; sin embargo, no todas corresponden al mismo evento eruptivo.*
`EN: The geologist observed several layers of ash; however, not all correspond to the same eruptive event.`

**Simplified segment:** *El geólogo observó varias capas de ceniza. Sin embargo, no todas corresponden al mismo evento eruptivo.*
`EN: The semicolon becomes a full stop and the marker opens a new sentence.`

*Note:* Angle quotation marks (« ») are the primary quotation mark in formal written Spanish and have no English counterpart. Screen readers announce these marks inconsistently, which is the reason for the attribute.
