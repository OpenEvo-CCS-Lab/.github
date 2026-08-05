# OpenEvo CCS Lab
#### Understanding the cultural computation of education

[![OpenEvo Lab](https://img.shields.io/badge/OpenEvo%20Lab-openevo.eva.mpg.de-teal)](http://openevo.eva.mpg.de)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC--BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Namespace](https://img.shields.io/badge/Namespace-w3id.org%2Fopenevo-purple)](https://w3id.org/openevo/)
[![FAIR](https://img.shields.io/badge/FAIR-Findable%20Accessible%20Interoperable%20Reusable-green)](https://www.go-fair.org/fair-principles/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)](https://github.com/openevo-ccs)

---

> **🔒 Most of this ecosystem is in private development.** We're a small, active lab restructuring
> our shared architecture (ontology, knowledge graphs, curriculum data models) and want room to
> iterate without every in-progress branch being publicly visible. The repos below stay public
> because they're either finished reference material or public-facing infrastructure (the
> ConceptBase Explorer app, the `w3id.org/openevo` namespace, the shared kernel ontology). More
> repositories will re-open as their content and tooling reach a stable, citable state — nothing
> is abandoned, just incubating.

## 📘 What is OpenEvo?

Every curriculum is a claim about the future — a document that says, in effect, "this is what our children should come to know, value, and be able to do." Multiply that claim across thousands of school systems, subjects, grade levels, languages, and cultural traditions, and you get one of the largest, least-mapped bodies of applied cultural knowledge in the world.

**OpenEvo** is a research lab studying that body of knowledge computationally. We treat curricula — standards documents, learning progressions, competency frameworks, textbooks — as **cultural models**: structured, evolving representations of a society's understanding of learning, development, and human nature. Our work asks how the precision and scale of computational methods (ontologies, knowledge graphs, natural language processing, topic modelling) can help us describe, compare, and improve these models, without losing sight of the human complexity and lived context they are meant to serve.

This organization is the GitHub home for that work: an evolving ecosystem of linked data, ontologies, tools, and datasets, anchored by a shared kernel (upper ontology, identifier scheme, cross-repo governance) in **[openevo-core](https://github.com/openevo-ccs/openevo-core)**, with **ConceptBase** as its original and most mature Foundational Repo.

Learn more about the lab at [openevo.eva.mpg.de](http://openevo.eva.mpg.de).

---

## 🧬 Why Computational Curriculum Studies?

**Computational Curriculum Studies (CCS)** is an emerging field at the intersection of curriculum theory, learning sciences, cultural evolution, and computational social science.

**In plain terms:** curriculum design has always been a deeply human, deeply local activity — shaped by pedagogical tradition, disciplinary politics, and cultural values that rarely get made explicit. At the same time, curriculum documents are increasingly born digital, standardized, and interconnected: national frameworks, competency taxonomies, and learning-progression models are published as structured text, indexed, and — increasingly — read by algorithms as much as by people. This creates both a risk and an opportunity. The risk is that computational tools flatten curricula into shallow keyword matches, erasing exactly the cultural nuance that makes them meaningful. The opportunity is that, done rigorously, the same methods can make curriculum design more *transparent*, *comparable*, and *self-aware* — surfacing hidden assumptions, gaps, and points of genuine disciplinary disagreement that close reading alone struggles to detect at scale.

**In more technical terms:** CCS treats curriculum policy artifacts as instances of formalizable knowledge structures (concepts, competencies, progressions, alignments) that can be represented in machine-readable ontologies, compared computationally via semantic alignment (e.g. SKOS matching), and analyzed using methods from corpus linguistics and unsupervised learning (e.g. topic modelling) — while remaining explicit, at every step, about where formalization ends and interpretive, theory-laden judgment begins.

Our own research focus within this broader field is on interdisciplinary structures of knowledge grounded in **evolutionary anthropology** and everyday human experience — how concepts like selection, variation, agency, culture, and transmission show up (or fail to show up) coherently across biology, social studies, and computer science curricula, from early childhood through secondary education.

---

## 🧩 ConceptBase

**[ConceptBase](https://github.com/openevo-ccs/conceptbase)** is one of nine co-equal **Foundational Repos** sharing [openevo-core](https://github.com/openevo-ccs/openevo-core)'s kernel — the richest and most mature today, hosting the shared ontology instances, controlled vocabularies, and JSON Schemas that let independently maintained curriculum repositories (Learning Progression Models, Strands, competency frameworks) describe their content in a common, interoperable language.

**In plain terms:** think of ConceptBase as a shared dictionary and grammar, not a single master curriculum. It doesn't tell anyone which curriculum is "correct" — it gives independent projects, built by different teams with different theoretical commitments, a common structure so their work can be *compared, linked, and reasoned over together*, the way `schema.org` lets independent websites describe products or events in a way search engines can all understand.

**In more technical terms:** ConceptBase is a Git-native, version-controlled registry of ontology instances (`oe:Concept`, `oe:LPM`, `oe:Strand`, and related classes), controlled vocabularies, and cross-vocabulary alignment records (`skos:closeMatch`, `skos:relatedMatch`, etc.), profiled against existing standards — SKOS, IEEE LOM, schema.org, and 1EdTech CASE — rather than reinventing them. Every entity is openly licensed, persistently identified, and structured for both human review (YAML, pull requests, RFC governance) and machine consumption (flat JSON, with JSON-LD/RDF/SPARQL support on the roadmap).

The shared upper ontology, identifier scheme, and cross-repo governance process that ConceptBase and its sibling Foundational Repos build on live in **[openevo-core](https://github.com/openevo-ccs/openevo-core)**, the ecosystem's kernel — see that repo for the full Foundational/Project architecture, including the other eight Foundational Repos.

### The `w3id.org/openevo` namespace, briefly

Every concept, competency, and vocabulary in ConceptBase has a **permanent web address** under `w3id.org/openevo/` — for example, `w3id.org/openevo/concept/OE-CONCEPT-000213`.

**In plain terms:** this is like an ISBN for an idea. Anyone, anywhere, can cite "Selection as defined by ConceptBase" using a link that will keep working indefinitely — even if we move servers, rebuild our website, or change tools — because [w3id.org](https://w3id.org) is a permanent redirection service designed exactly for this purpose. That matters for a research field: a citation in a 2026 paper should still resolve correctly in 2036.

---

## 🎯 Our Aim: Coherence across grades, subjects, and cultures

Curriculum incoherence is a well-documented, everyday problem: a concept taught in Grade 4 science may never be revisited in Grade 8; a term used one way in biology standards may mean something subtly different — or contradictory — in a computer-science AI-literacy framework next door. Multiply that across countries, languages, and educational traditions, and coherence becomes not just a design nicety but a genuine research and policy challenge.

OpenEvo's aim is to increase both:

- **Vertical coherence** — whether a concept develops sensibly in sophistication as students move through grade bands (K–2 → 3–5 → 6–8 → 9–12 and beyond), rather than appearing and disappearing arbitrarily.
- **Horizontal coherence** — whether related concepts reinforce each other *across* subject areas at the same grade level (biology, social studies, computer science, and beyond), rather than being taught as isolated, disconnected facts.

...across cultures and contexts around the world — not by imposing a single "correct" curriculum, but by enabling an **open, FAIR digital ecosystem of curriculum meta-modelling tools**.

**In plain terms:** a curriculum policy document is already a *model* — a society's model of what a learner should become. Our tools are **meta-models**: models *of* those models. Meta-modelling lets us represent, side by side, the different cultural assumptions embedded in different curricula, so researchers, policymakers, and educators can see clearly where systems align, where they diverge, and why — a form of comparative, computational curriculum literacy that hasn't existed at this scale before.

**In more technical terms:** this means building shared ontologies and schemas (FAIR: Findable, Accessible, Interoperable, Reusable) that different Learning Progression Models can be validated against, alignment records (SKOS-based) that make cross-vocabulary and cross-system comparison an explicit, citable data structure rather than an implicit assumption, and open tooling (the ConceptBase and its companion apps) that make this infrastructure usable by non-specialists, not only ontology engineers.

---

## 🇩🇪 German-Language Research: *Eva & Buch*

Alongside our English-language reference work, OpenEvo maintains a growing body of **German-language curriculum research**, supporting Dr. Susan Hanisch's forthcoming (2027) book on teaching **evolutionary anthropology as an interdisciplinary theme** in German schools.

The **[`eva_buch`](https://github.com/openevo-ccs/eva_buch)** repository hosts a rich supplemental dataset: a **topic-modelling analysis of German curriculum documents**, mapping where and how evolutionary-anthropological themes (and related interdisciplinary concepts) surface — or are absent — across German subject curricula.

Explore the data visually, with interactive charts and topic browsers, in the **[eva_buch app](https://openevo-ccs.github.io/eva_buch/)**.

This work is a concrete example of CCS methods applied to a real, high-stakes curricular question: how do we teach students that they are, themselves, products and agents of cultural and biological evolution — and where in a national curriculum does that story already have room to be told?

Our **[EvoMentor_DE](https://github.com/openevo-ccs/EvoMentor_DE)** repository is the German-language digital ecosystem built around the same theme, for direct classroom integration.

---

## 🧪 NetLogo Models

**[netlogo](https://github.com/openevo-ccs/netlogo)** is our growing collection of agent-based NetLogo models for teaching evolutionary and behavioral concepts interactively — built for direct classroom use alongside the Learning Progression Maps in our (currently private) curriculum repositories.

---

## 🌍 Get Involved

Curriculum shapes lives and communities — and yet the models behind it are rarely made explicit, let alone open to scrutiny or comparison. We think that should change, and we'd like your help changing it.

Whether you are an **educational researcher** studying learning progressions, a **policymaker** designing or revising standards, an **educator** navigating what a curriculum actually asks of you and your students, or simply a **curious student** who has ever wondered why your school taught things in the order it did — there is a way to contribute:

- 🔍 **Explore** [openevo-core](https://github.com/openevo-ccs/openevo-core) or the [eva_buch app](https://openevo-ccs.github.io/eva_buch/) and see how your own curriculum's concepts map (or don't) onto others.
- 🧭 **Propose** a new controlled vocabulary or alignment via ConceptBase's RFC-based governance process — every substantive change to the shared ontology is proposed, reviewed, and documented, not decided unilaterally.
- 🌐 **Translate** — multilingual concept labels and definitions are an open, active need across the ecosystem.
- 💬 **Ask questions** by opening an issue in any repository below, or reach out directly.

Curriculum- and Learning-Progression-Model-specific repositories are currently in private development while we restructure — reach out if you'd like early access to that work.

---

## 🗂️ Explore the Ecosystem

**Public repos:**

| Repository | What it is |
|---|---|
| **[conceptbase](https://github.com/openevo-ccs/conceptbase)** | ConceptBase — a Foundational Repo: concept/LPM/strand ontology instances, schemas, vocabularies, and the ConceptBase Explorer app |
| **[openevo-core](https://github.com/openevo-ccs/openevo-core)** | The shared kernel — upper ontology, identifier scheme, cross-repo RFC process, and the `w3id.org/openevo` namespace root |
| **[eva_buch](https://github.com/openevo-ccs/eva_buch)** | German-language topic modelling dataset and interactive visualizations supporting Susan Hanisch's forthcoming (2027) book on teaching evolutionary anthropology |
| **[EvoMentor_DE](https://github.com/openevo-ccs/EvoMentor_DE)** | German-language digital ecosystem for evolutionary-anthropology curriculum integration |
| **[netlogo](https://github.com/openevo-ccs/netlogo)** | Agent-based NetLogo models for teaching evolutionary and behavioral concepts |
| **[w3id.org](https://github.com/openevo-ccs/w3id.org)** | Our fork of the shared `w3id.org` permanent-identifier registry, used to submit namespace changes upstream |

### 🌱 In development

The rest of the ecosystem's architecture, named here so the shape is visible even while the content
itself is still private — see the note at the top of this page:

- **Foundational Repos** (nine co-equal repos sharing `openevo-core`'s kernel; ConceptBase, above, is
  the only one currently public): CompetencyBase · TeachingBase · ProjectBase · LiteratureBase ·
  HumanBase · TheoryBase · QuestionBase · MethodsBase
- **Project Repos** (Learning Progression Models, field-knowledge graphs, applications, and
  theory-grounding repos that assemble Foundational content by reference) — a representative few:
  `bio-core-k12` and `oe-interdisciplinary-k12` (the two reference LPMs), `ccs-graph` (field-specific
  interpretation over base facts), `curriculum-evolution` (the theoretical grounding this lab's work
  builds on), and `openlpm` (a white-label platform meant for outside research groups to fork and run
  their own LPMs, staying interoperable with this ecosystem — reach out if that's you; still early)

Nothing here is abandoned — this organization's `.github` profile reflects a small, active lab
restructuring shared architecture, not a finished product with a hidden roadmap.

---

## 📖 License

Unless otherwise noted, **content** across this organization (ontologies, schemas, vocabularies, datasets, documentation, and this README) is licensed under **[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)** — free to share and adapt for non-commercial purposes, with attribution, under the same license. **Code and tooling** (build pipelines, validation scripts, apps) are typically licensed separately under **MIT** where noted in the relevant repository. Always check the individual repository's `LICENSE` file(s) for specifics, as licensing is applied per-repository.

---

## 📫 Contact

This organization is administered by:

**Dustin Eirdosh** — GitHub: [@dustineirdosh](https://github.com/dustineirdosh)

OpenEvo Computational Curriculum Studies (CCS) Lab — [openevo.eva.mpg.de](http://openevo.eva.mpg.de)
