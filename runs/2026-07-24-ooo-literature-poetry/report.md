# Adapting and Infusing Object-Oriented Ontology in Literature and Poetry

Run: `2026-07-24-ooo-literature-poetry` · See `plan.md` for scope/method and
`claims.md` for the evidence ledger.

## 1. Scope note and a retrieval limitation, stated up front

Per this station's protocol, literature searches began with `semantic-scholar`.
That MCP server's upstream host was blocked by this environment's network
policy for the full session (`api.semanticscholar.org` returned `403` /
"policy denial" on every retry — a gateway-level restriction, not an empty
result), so the paper-index leg of retrieval could not run at all this time.
`papersflow` also requires an OAuth authorization this non-interactive
session cannot complete. Per CLAUDE.md, neither is treated as "no literature
exists" — the dossier below rests on general web search instead, which is
in any case the channel the protocol designates as primary for humanities
material. A follow-up run should retry `semantic-scholar` and complete
`papersflow` authorization to cross-check.

A citation-verification pass (see `.claude/skills/citation-verification`)
was run against every source in `claims.md`: every citation below exists
and is cross-corroborated across at least two independent listings
(JSTOR/PhilPapers/PhilArchive/ResearchGate/Project MUSE/publisher pages) —
none is fabricated or unfindable, so nothing here needed moving to a
rejected/fake-citation bin. The caveat that *does* apply, and is carried
through every section below, is narrower: **depth** of verification. This
agent read secondary summaries of these sources, not the primary full text
itself, so quoted passages are quotations *as surfaced by search*, not
independently re-verified against the typeset original. See the next
paragraph for why, and `claims.md` for the per-claim strength rating this
produces (everything here is "single-source" or "speculative," never
"verified" — see that file's key).

A second limitation: direct `WebFetch` of primary sources (JSTOR, Project
MUSE, ResearchGate, Wikipedia, Medium, personal blogs) was refused with
`403` across the board in this session. Everything below is therefore
drawn from search-engine-surfaced summaries and secondary discussion of the
primary texts, not from this agent's own reading of full primary text. Titles,
venues, page numbers, and author attributions are cross-corroborated across
multiple independent search hits where possible; direct quotations are
flagged as such and are quotations *of the source material as surfaced by
search*, not independently re-verified against the typeset original. Treat
page-level claims accordingly — see `claims.md` for per-claim strength.

## 2. The founding debate: *New Literary History* 43.2 (Spring 2012)

The organized encounter between OOO and literary studies has a specific
point of origin: the Spring 2012 issue of *New Literary History* (vol. 43,
no. 2), which paired essays by Graham Harman and Timothy Morton with a
response by Jane Bennett.

- **Graham Harman, "The Well-Wrought Broken Hammer: Object-Oriented Literary
  Criticism"** (*NLH* 43.2, pp. 183–203). The title deliberately echoes
  Cleanth Brooks's New Critical touchstone *The Well Wrought Urn*, staging
  OOO's literary criticism as both heir to and break from New Criticism's
  attention to the autonomous, self-standing "object" of the poem — a
  connection independently drawn by commentators discussing New Criticism
  and OOO side by side.
- **Timothy Morton, "An Object-Oriented Defense of Poetry"** (*NLH* 43.2).
  Reads Percy Bysshe Shelley's *A Defence of Poetry* through OOO. Its
  argument, as surfaced across several summaries: "behind every flow and
  stasis, there is an object that cannot be reduced to anything whatsoever,"
  i.e. the object's essence "can never be fully realized," and objects are
  "prior to their relations." From this, poetry is cast as doing double
  duty — offering "a possible indirect access to the withdrawn object" and
  itself "mirroring the object's form," because OOO's account of causality
  is explicitly *aesthetic*: "causality is aesthetic," so a poem's operation
  on a reader is treated as continuous with, not merely analogous to,
  physical causal interaction between objects.
- **Jane Bennett, "Systems and Things: A Response to Graham Harman and
  Timothy Morton"** (*NLH* 43.2, pp. 225–233). Opens by asking "what are the
  ethical and political stakes of the object-oriented philosophers' fight
  against systems- or process-theories?" Bennett contests Harman's and
  Morton's shared rejection of relationalism, arguing that systems and
  assemblages "enact real change" and can "host an undetermined surplus,"
  which she takes to answer Harman's charge that relational/process
  philosophies cannot account for novelty. She also resists the vocabulary
  of "object" itself, proposing "thing" or "body" as better suited to
  ecological awareness and to evading the politics built into "active
  (manly, American) subjects and passive objects."

This triad is the terminological hinge for everything downstream: it is
where "object-oriented literary criticism" and "object-oriented poetics"
first get named as such, in the literary field's own venue, by the two
central OOO figures.

## 3. Harman's literary criticism: allure, ontography, weird realism

Harman's own later synthesis — the **"Object-Oriented Ontology (OOO)" entry
he wrote for the *Oxford Research Encyclopedia of Literature*** (2019) —
gives OOO literary criticism's clearest official self-description: "OOO is
an intellectual movement in the arts and humanities sharing certain
affinities with both phenomenology and Actor-Network Theory," realist and
"often at odds with existing currents in postmodernism and critical
theory." Its central claim: objects "withdraw from all direct human and
non-human contact, so that relations between things are always indirect and
must be accounted for rather than taken for granted." Technically, OOO
distinguishes **real objects**, **sensual objects**, **real qualities**, and
**sensual qualities** — real objects/qualities are "not directly accessible
to thought, perception, practical use, or even causal relation," reachable
only "by more allusive means." The encyclopedia entry states plainly that
"OOO literary theory has a special fondness for the weird," above all
**H. P. Lovecraft**, whose fiction is read as exemplifying the tension
between objects and their qualities.

This is worked out at book length in **Harman's *Weird Realism: Lovecraft
and Philosophy* (2012)**. As discussed across multiple reviews: Harman
"extracts the basic philosophical concepts underlying Lovecraft's work,"
proposing that Lovecraft stands to speculative realism as Hölderlin stood
to Heidegger or Mallarmé to Derrida — a literary case that *generates*
philosophical vocabulary rather than merely illustrating it pre-formed.
Harman reads Lovecraft as a writer of the gap between "objects and their
qualities" — what Harman calls **ontography**, thought that maps the
"interaction between objects and their qualities" — and finds in
Lovecraft's much-derided stylistic tics (his adjectival excess, his
gestures at the unspeakable, his narrative hesitations before the alien
thing) the literary *technique* for gesturing at withdrawn objects that his
philosophy needed a name for. One reviewer's formulation: "For Harman, art
and metaphor alone can hint at the withdrawn reality of objects. Philosophy
cannot state the real, science cannot exhaust it, praxis cannot touch it.
Only aesthetic allusion brings us close." The specific mechanism Harman
gives this allusive contact is **allure**: the term for the experience in
which "the gulf between a sensual object and its withdrawn real qualities
becomes momentarily apparent" — an event he locates in aesthetic experience,
humor, and metaphor generally, and which several commentators identify as
the load-bearing concept of Harman's literary aesthetics.

## 4. Morton: hyperobjects, ecopoetics, and "ecology without nature"

Timothy Morton — an OOO-affiliated theorist trained as a Romanticist
(Shelley, Mary Shelley) — supplies the object-oriented vocabulary most
widely adopted *inside* ecocriticism and ecopoetics specifically. Morton
coined **hyperobjects** (2010; book-length in *Hyperobjects: Philosophy and
Ecology after the End of the World*, 2013) for "objects so massively
distributed in time and space as to transcend localization," such as
climate change or styrofoam, characterized by five properties repeatedly
cited in summaries: **viscosity, nonlocality, non-temporality (or temporal
undulation), phasing, and interobjectivity**. One review's framing of the
larger project is worth preserving verbatim for how it collapses the
theory/poetry distinction that this dossier is tracking: **"Mortonian
poetics is a species of the genre of object oriented ontology (OOO), which
is itself a kind of poetic realism"**; because Morton is "originally a
scholar of English romantic poetry, his work reads best as poetry, or
perhaps a poetics, as a singular Mortonian vision of the world." Morton's
own earlier book, *Ecology Without Nature* (2007), and the "ecology without
nature" formula it names, is presented as the seed from which his
object-oriented "ecology without matter" and "ecology without the present"
later grew — i.e. Morton's ecopoetics is continuous across his pre-OOO and
OOO-identified writing rather than a break.

Institutionally, this line runs through the **ecopoetics** community
proper, not only through Morton. **Jonathan Skinner**, who founded and
edited the journal *ecopoetics* (2001–2005), frames ecopoetics as a matter
"not merely of theme, but of how certain poetic methods model ecological
processes like complexity, non-linearity, feedback loops, and recycling" —
a poetics of *form modeling ecology* that is a natural adjacent site for
OOO's object-vocabulary even where Skinner's own primary framework is
ecocritical rather than explicitly Harman/Morton-derived. The explicit
convergence point is a documented UC Berkeley seminar, **"Ecopoetics,
Object Relations, and Object-Oriented Ontology,"** moderated by **Nathan
Brown**, bringing together critics and poets (including Julia Fiedorczuk,
Eileen Myles, Devin King, Anthony Camara, and others) to work the seam
between ecopoetics and OOO directly. Brown is also on record as an internal
critic of the OOO side of that seam: his review-essay **"The Nadir of OOO:
From Graham Harman's Tool-Being to Timothy Morton's Realist Magic: Objects,
Ontology, Causality"** (*Parrhesia* 17, 2013, pp. 62–71) diagnoses what he
takes to be conceptual incoherence in the claim that objects are "vacuum
sealed" and non-relational — a caution against importing OOO's
object-vocabulary into ecopoetics uncritically.

## 5. Bogost: alien phenomenology, carpentry, ontography — and an ambivalence toward "the literary"

Ian Bogost's *Alien Phenomenology, or What It's Like to Be a Thing* (2012)
supplies the OOO-adjacent family's most *practice*-oriented vocabulary.
Building on "Husserl's epoché, Harman's theory of vicarious causation, and
Whitehead's panexperientialism," Bogost names three modes: **ontography**
("the authorship of works that reveal the existence and perception of
objects"), **metaphorism** ("the authorship of works that speculate about
the unknowable inner lives of objects"), and **carpentry** ("the
construction of artifacts as a philosophical practice" — "making things
that explain how things make their world"). Notably for a dossier on
literary uptake, Bogost's own relation to "the literary" is *adversarial*
rather than adoptive: coming from a comparative-literature background, he
is reported to oppose ontography to "the 'flowing legato' of the literary,"
which he treats as too committed to "identification and resonance" against
the "jarring staccato of real being" he wants instead. The one partial
exception is telling: Bogost closes the book by invoking a **Charles
Bukowski poem** as something that "reminds us of the awesome plenitude of
the alien everyday" — a single poetic exhibit permitted back in at the
threshold of an otherwise anti-literary argument.

## 6. Bryant: onticology and flat ontology (the least literary of the four)

**Levi Bryant**, who coined the term "object-oriented ontology" itself in
2009 to distinguish it from Harman's "object-oriented philosophy," develops
**onticology** in *The Democracy of Objects* (2011): a "flat ontology"
where "objects of all sorts and at different scales equally exist without
being reducible to other objects," with "no transcendent entities such as
eternal essences outside of dynamic interactions among objects," and where
humans are "objects among the various types of objects that exist," each
with "their own specific powers and capacities." Of the four core OOO
figures surveyed here, Bryant's uptake into literary criticism specifically
is the thinnest in what this search turned up — his influence runs more
toward media studies, STS, and digital humanities than toward reading or
writing poems — which is itself worth recording as a asymmetry in the
field rather than an oversight of this search.

## 7. Creative-practice adaptations: writing *as* an object-oriented method

Two case studies show OOO's vocabulary crossing from criticism into
composition method, not just reading method:

- **Travis Jeppesen's "object-oriented writing."** A literary/visual-art
  practice explicitly named in parallel with OOO and speculative realism,
  aimed at fusing "the creative and critical aspects of literary work into
  a single hybrid form." Method, as reported: "a practice of perceiving and
  writing that attempts to inhabit the object rather than merely react to
  it," locating the writer "within the work of art, rather than outside,"
  attempting "to infest the inanimate art object with human agency via the
  act of writing." The resulting texts "often resemble prose poetry,"
  alongside dramatic monologue and more conventional narrative. In *16
  Sculptures*, Jeppesen re-created sixteen historical artworks in language;
  he later characterized the practice as "bad writing" or "wild writing," in
  which failure is "incorporated into the final results" rather than
  corrected away — a compositional ethic that reads as a working-poet's
  translation of Harman's/OOO's insistence that objects exceed and resist
  any representation of them.
- **Daniel J. Thompson, "Object-Oriented Ontology and the Non-dual in
  Poetry"** (essay). Surfaces as a direct attempt to read poetic practice
  through OOO's real/sensual-object and allure vocabulary, framed around a
  "non-dual" sensibility; full text was not independently retrievable this
  session (site blocked direct fetch), so its specific readings are noted
  here as a lead for a follow-up run rather than summarized in detail — see
  `claims.md`.

## 8. Critical pushback aimed specifically at OOO's literary/humanist use

Two dissenting essays matter for a dossier that wants sources' own terms,
not just OOO's own self-description:

- **Jane Bennett, "Systems and Things"** (§2 above) — the response internal
  to the founding *NLH* debate, contesting OOO's anti-relationalism from a
  vitalist-materialist (*Vibrant Matter*) position.
- **Andrew Cole, "The Call of Things: A Critique of Object-Oriented
  Ontologies"** (*minnesota review* 80, 2013, pp. 106–118). Cole, a
  medievalist, targets OOO, actor-network theory, and Bennett's vitalism
  together, arguing they share "a very strong humanism and a rather
  traditional ontology" precisely where they claim to have escaped
  humanism: each "claim[s] to hear things 'speak,' recording things' voices,
  registering their presence, and heeding their indifference" — which Cole
  calls "just another instance of logocentrism and ontotheology, those
  ancient traditions in which things speak their being." This is the
  sharpest challenge on record to the literary-critical move (common to
  Harman's ontography and to "object-oriented writing" alike) of treating a
  text as *giving voice to* or *allusively touching* an object's withdrawn
  reality — Cole's charge is that this move quietly reinstates the very
  logocentric humanism OOO claims to reject.

## 9. Persian-language reception: thin, but present — and closer to theatre than to lyric poetry

Per CLAUDE.md's instruction never to treat a paper-index null as "no
literature exists," and to preserve Persian titles in original script with
transliteration: general web search located no Persian-language treatment
of OOO applied specifically to *poetry* (شعر). It did locate two
Persian-language academic applications of Harman's هستی‌شناسی شی‌محور
("object-oriented ontology," lit. "object-centered ontology") to other
literary/performance texts, which belong in this dossier as the closest
available evidence of Persian critical uptake and are directly relevant to
this station's theatre/scenography focus:

- **نازنین هنرخواه و علی شیخ‌مهدی، «ساموئل بکت و ظهور شیءگرایی:
  هستی‌شناسی شیءگرا در نمایشنامهٔ بازی بدون کلام»** — transliterated:
  *Nazanin Honarkhah and Ali Sheikh-Mahdi, "Samuel Beckett and the
  Emergence of Thing-ism [شیءگرایی]: Object-Oriented Ontology in the Play
  'Act Without Words.'"* Published in *Journal of Language and Translation
  Studies* (jlts.um.ac.ir). Argument, as surfaced: applies Harman's
  object-oriented philosophy to Beckett's *Act Without Words*, reading
  Beckett's abandonment of anthropocentric dramatic structure as itself
  staging an "object-oriented perspective on human existence" in which
  "humans and objects are equated at different layers of ontology" — i.e.
  treating Beckett's own dramaturgical minimalism as independently arriving
  at something like OOO's flat ontology.
- **نازنین هنرخواه و علی شیخ‌مهدی، «بررسی همزیستی در فیلم "جهان با من
  برقص" بر اساس هستی‌شناسی شی‌محور گراهام هارمن»** — *"Examining
  Cohabitation in the Film 'Dance the World with Me' Based on Graham
  Harman's Object-Oriented Ontology"* (*Journal of Fine Arts: Performing
  Arts and Music*, vol. 28, no. 3, Fall 1402/2023, pp. 57–66). Applies
  Harman's ontology to a film rather than a literary text proper, but by
  the same two authors and method as the Beckett piece, suggesting an
  active small research program applying Harman specifically (not Morton,
  Bryant, or Bogost) to Persian-language performance criticism.

No Persian-language poetry-specific OOO criticism, and no Persian
*translation* of the core OOO/speculative-realism primary texts, surfaced
in this search. This is recorded as a gap for a follow-up run (worth
searching Persian philosophy journals and Nashr-e Nimaj/Ney catalogs
directly; Harman's *ناماده‌باوری* / *Immaterialism* and هستی‌شناسی معطوف
به شیء exist in Persian translation per bookseller listings found, which
suggests translated *terminology* is stabilizing even without a literary
application yet found).

## 10. A working glossary, in the sources' own terms

| Term | Coiner / source | Gloss as used in the literature surveyed |
|---|---|---|
| withdrawal | Harman | objects retreat from all direct contact; relations are always indirect |
| real object / sensual object | Harman | real objects exist independent of relation; sensual objects exist only in relation to some real object |
| allure | Harman | the momentary apparent gulf between a sensual object and its withdrawn real qualities; site of aesthetic/humorous experience |
| ontography | Harman (lit. crit.); also Bogost (practice) | mapping/authoring the interaction between objects and their qualities |
| weird realism | Harman | the philosophical position extracted from reading Lovecraft's stylistic gaps and adjectival excess |
| hyperobject | Morton | an object "massively distributed in time and space," e.g. climate change; viscous, nonlocal, nontemporal/phased, interobjective |
| ecology without nature | Morton | ecological thought that drops "Nature" as a reified background concept |
| onticology / flat ontology | Bryant | all objects, at all scales, exist equally without reduction to one another; no transcendent essences |
| alien phenomenology / metaphorism / carpentry | Bogost | speculating on/constructing artifacts that model an object's "inner life" or perspective |
| object-oriented writing | Jeppesen | writing practice that inhabits rather than describes an art-object, incorporating "failure" as method |
| thing (vs. object) | Bennett (contesting Harman/Morton) | preferred term for evading the subject/object political hierarchy; things/bodies as vital, relational actants |

## 11. What this dossier does not yet establish (honest gaps)

- No primary-text page proofs were pulled directly (site 403s); quotations
  above are search-surfaced and should be spot-checked against the actual
  *NLH* 43.2 offprints, *Weird Realism*, and *Hyperobjects* before being
  treated as exact wording in any publication-grade output.
- Bill Brown's "thing theory" (2001, *Critical Inquiry*) is the acknowledged
  adjacent/precursor lineage to OOO's object-talk in literary studies but
  was not directly retrieved this run — flagged for the next run rather
  than asserted from memory.
- No poetry (as opposed to drama/film) was found with direct Persian OOO
  application; treat §9 as a lead, not a settled finding.
- `semantic-scholar` and `papersflow` were both unavailable this session
  (network policy block / unauthenticated respectively) — a re-run once
  either is restored could surface additional peer-reviewed literature this
  session could not reach.
