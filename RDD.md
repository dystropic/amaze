# Repo Design Doc — the standard, and the amaze instance

## Part one: the document class

### The coinage

A Repo Design Doc, RDD, is the document that designs a repository as an operational substrate. It stands at peer level with the Product Requirements Document and the Technical Design Document because it answers a question neither of them answers, about an artifact as consequential and as hard to reverse as anything they govern.

The PRD answers: what is being built, for whom, why, with what scope and what non-goals. The TDD answers: how it is implemented — architecture, components, interfaces, tradeoffs. Neither answers: where does the work live, and how does its home hold it.

That question gets defaulted instead of designed — src and docs and dot-github by convention, structure improvised per file, boundaries drawn by folder name — and the defaults fail in two opposite directions. One direction turns the repository into a project management surface: lifecycle folders, status files, governance furniture, the process performed as content. The other turns it into an exhibition: finished things only, working state exiled, the repository curated instead of used. Both directions were demonstrated at full scale in the work that produced this standard. The RDD exists so that neither happens by default.

The repository deserves this document because it is the one artifact every contributor, agent, tool, and reader touches on every interaction with the project; because directory structure is the most rigid layer of a codebase, where change is churn across every reference; because for open source work the repository is simultaneously the working environment and the shipped surface; and because its design decisions, once defaulted, get defended as conventions rather than examined as choices.

### The peer relationship

The RDD consumes the system decomposition the way the TDD consumes the PRD. It cannot be written before the system's anatomy exists at module level, and an RDD written without that anatomy will derive structure from the wrong sources — file formats, arrival order, hosting convention, or the author's taxonomy instinct.

The dependency is strict: requirements define the system, the decomposition names its organs, and the RDD projects that anatomy onto a directory tree. Where the decomposition is still open, the RDD carries the openness as named open structure rather than resolving it with invented folders.

### Required sections

An RDD that omits any of these has not done the job.

**Identity and scope.** What the repository is — working repo, publication surface, one of several, the only one — and what it is not, stated as permanent exclusions; and its relation to the system it serves, declared: a repository may be the system's whole working body, a partial substrate, or a projection of it, and conflating these produces opposite failures. Arrival order is not identity: what shipped first does not define what the repository is.

**Source of structure.** What the directory structure derives from. The load bearing principle of the class: structure derives from system anatomy, never from file formats, never from convention, never from what happens to exist on the day of writing.

**Disclosure model.** What enters at what resolution, and how boundaries are held. Boundaries are structural — separate repositories — never nominal — folder names inside one tree. The tree itself never declares that a boundary exists or what it protects.

**Admission logic.** What enters at all, and in what state. This section must distinguish working state from process narration: a codebase's unfinished work is native content carried by the tool's own mechanisms; the repository's commentary on its own process is not content at all.

**Process trace policy.** What record of the work's process exists in the repository, stated explicitly, because the unexamined default is drift into changelogs, status surfaces, and decision ledgers that duplicate what the version control tool already does natively.

**Placement logic.** The determinacy core: for every component of the system's anatomy, where it lives, what triggers its home's materialization, and how it is named. The standard the logic must meet: total logic, minimal tree — every artifact's home decidable before the artifact exists, no directory existing before its first real file.

**Platform reality.** The actual host's necessities separated from its ceremony. Necessities are what the platform's rendering and tooling genuinely require. Ceremony is what the platform suggests to make a repository legible as a managed project.

**Readers and runners.** Who and what reads the repository — which humans, which agents, which tools — and what each needs structurally. Not an audience section: a receiver conditions section. The repository is not addressed to spectators; it is entered by parties who can use, build, run, evaluate, or correctly fail against it.

**Growth and change.** How structure evolves, what forces reorganization, what reorganization costs, and who the structure function is — the party whose judgment admits and places, and what committed criteria that judgment runs against.

**Refusals.** The permanent exclusions, written first in practice even though they appear here in the section list, because the default failure is importing them.

**Own location.** Where the RDD itself lives and what the repository's relationship to it is. This is a declared decision, not a universal: a repository may carry its own design document, or its logic may live on a working surface the repository never references. The RDD says which, and why, for its repository.

### Quality criteria

An RDD is good when:

- every placement is decidable in advance, with no per file judgment
- every directory is traceable to a system component or a platform necessity
- disclosure boundaries are structural
- the tree is minimal while the logic is total
- working state has a native home
- the repository contains no content whose subject is the repository, unless the own location section explicitly decided otherwise

### The failure catalog

The class exists against these, each observed live in the work that produced it.

**Taxonomy cosplay.** Structure ahead of content, directories as promissory notes, the appearance of rigor through folders.

**Process narration.** The repository as its own audience — status files, decision ledgers, struck registers, lifecycle folders, working drafts published as working drafts.

**Format classing.** Artifacts classed by extension instead of function, "documents" treated as a kind.

**Arrival order ontology.** The repository's identity read off whatever shipped first.

**Convention defaulting.** src, lib, docs, community files adopted unexamined.

**Boundary by naming.** Internal material in a public tree behind a folder name.

**Apparatus duplication.** Ledgers rebuilding what the commit log already is.

**Exhibition collapse.** Admission logic that forbids working state and makes the repository unusable as a codebase.

**Project management collapse.** The inverse, where the repository models the process instead of holding the output.

The last two are the opposed failures that bracket the class; an RDD is the instrument for standing between them on purpose rather than landing on either by default.

## Part two: the amaze RDD

The logic below governs admission, placement, and growth unless amended. Proposed items stand until struck or confirmed; names coined by the operator are canonical handles.

### Identity and scope

This repository — github.com/dystropic/amaze — is the high fidelity public projection of amaze, the production engine of Dystropia. One repository, public, open source.

amaze is not run from it: the repository is not the runtime, not the control plane, not the full back of house, and not the ontology itself. Its job is to expose enough of the system's anatomy, in operative form, for humans, agents, tooling, and public counterparties to enter operative relation with the work, while never pretending to contain or operate the whole organism.

It holds a sufficient portion of the codebase. Sufficiency is operator defined and deferred, and in this frame it means what fidelity requires, not what completeness would.

The repository is also product surface: its prose components are shipped, operative parts of the system — narrative facing and functional at once — not documentation about parts kept elsewhere.

The governing invariant is projection fidelity: every visible artifact points back to the underlying system, never to platform convention, management theater, or public facing costume.

The repository is not:

- an exhibition
- a documentation site
- a process narrator
- an organization simulator
- a gallery that code visits
- the organism it projects

### Source of structure

The canonical decomposition of amaze.

Primitives:

- **media.sp** — the media strand processing primitive
- **labyrics**

Modules with coined handles:

- **mazerunner contests** — the production side contests in which competing procedures traverse labyric fields and generate candidate routes for digestif formation
- **dystro** — selection and propagation of on brand multiformat media narratives generated through amaze, without exposing participant identity

Modules under descriptive placeholders, awaiting handles:

- digestif formation
- digestif surface
- human consumable form
- agent consumable form
- transaction form
- daimonic series tending
- arena scoreboard
- business development labyrics

A placeholder is an explanatory label, not ontology, and never crystallizes into the tree.

System level: the operative components that belong to the whole rather than to one organ.

Product objects — digestif, session, series, daimon, scoreboard entry, distro object — live with the module that owns them or at system level. Per object placement is decided at first artifact, and that openness is carried as openness.

The placement question for any artifact: which component of the decomposition is this.

- Code answers with the module it implements.
- Prose answers with the component it operates as.
- Nothing answers with its file format.

### Disclosure model

Public operative minimum throughout.

- labyrics is public at full operative resolution — the README already defines it.
- media.sp enters at operative minimum only.

No content anywhere in the tree declares that a fuller resolution exists, that a boundary exists, or what any boundary protects.

The internal canonical lives on the working surface. If an internal git surface ever exists, it is a separate private repository; no folder of this tree ever plays that role.

### Admission logic

Components of the system enter, in working or finished state, on the tool's native mechanisms.

Proposed and standing: main is the operative surface by convention — what sits on main is the system as currently made. Branches carry working state: experiments, partial implementations, failing tests, drafts of components. None of it is ever confused for the made surface and none of it requires a status apparatus, because the branch is the status.

Product specimens and media register material enter finished, with the gestalt discriminator governing admission — the recognition pattern surviving, not the costume — and the committed design language as the criteria the judgment runs against.

Zero process records enter, in any state.

Code's toolchain reality — build files, manifests, lockfiles, test fixtures belonging to a module — is admitted as part of the module it serves.

### Process trace policy

Git's native log is the only process trace, total and sufficient.

Proposed and standing: commit messages carry the why — what changed and what it replaces — as the one semantic channel the native log already provides.

No changelog, no decisions file, no status surface, no struck register, no lifecycle information exists as repository content.

Superseded content is replaced; the diff is the history because that is what the tool is.

### Placement logic

Root is the system level. The operative prose components live there flat:

- the README as the front door — a product specimen that routes its readers by type, carrying the entire orientation burden through its own content
- the receiver condition filter
- the instance instrument
- the formal definitions
- the design language
- the positioning note
- specimens of the system level kind
- the license and ignore files, joining with the first code

Root is the system layer above the module layer, not a prose layer beside a code layer. One standard across substrates.

Primitives and modules materialize as top level directories, flat, with no grouping wrapper. A wrapper directory named modules would say "these are modules" — content about the tree — and classify rather than hold; the decomposition's names need no chaperone.

Materialization: each directory appears in the same commit set as its first real file, never before.

Naming: canonical handles, never explanatory prose labels. Explanatory labels live inside definitions; handles live in the tree, in headings, and in module identities. A directory materializes only under an operator coined handle, lowercase, its directory form confirmed at materialization; a placeholder never crystallizes.

Handles coined so far: mazerunner contests, media.sp, dystro.

A coined handle is not a fresh invention but a surfaced crystallization of long formed material. The naming work at externalization is exactness — landing each handle so the outside world cannot miscompile it into an adjacent familiar category — not caution against commitment.

Proposed candidates for the imminent homes: the daimonic series tending and transaction form implementation under the daimon's name, since the contract is the daimon's body; the digestif formation implementation under the compiler's name when it exists.

Hyphens in directory names are structural identifiers, acceptable where the project form is genuinely multi word.

Within each module directory: the module's public operative definition and its implementation, together. The definition is a made thing in the boundary discipline's shape —

- what feeds this
- what it emits
- what it does
- what it does not do
- what it might be confused with

— arriving with or ahead of the code, at public operative minimum. Definition and implementation cohabiting is what makes the directory the module's home rather than a code bin.

The working canonical decomposition itself does not enter the repository: it carries material under the disclosure boundary. Its public operative content enters piecewise, as each module's definition, on materialization.

### Platform reality

Necessities, admitted:

- the README at root, rendered as the entry
- the license with first code, as the open source commitment it is
- ignore files with first tooling
- per module toolchain files, as part of the module they serve

Ceremony, refused:

- issue templates and pull request templates
- contributing guides and codes of conduct
- badges and community health files
- anything else whose function is to make the repository legible as a managed project

Alphabetical rendering of the file list is accepted, never fought with numeric prefixes. Any ordering that matters is expressed inside documents by reference.

### Readers and runners

Three entrants, each owed something structural.

Receivers who pass the filter: parties who can enter operative relation with the work without converting it into the wrong kind of object. The front door routes them by type, including the route for the suspicious.

Model instances: the instance instrument operates at entry, and the tree mirroring the decomposition means an agent navigates by system anatomy. The structure is itself agent readable orientation, and this document in the tree is its legend.

Build tooling: each module's directory is self sufficient for its own toolchain.

No reader is addressed as a spectator. Rejection, confusion, and disqualification at the front door are the filter working.

### Growth and change

Crystallization on first artifact, always — and a materialized name is a current projection coordinate, not a prison.

Terminology refinement by commit is the native way the projection improves resolution: a commit can rename, tighten, replace, or re-home a handle without violating anything, because determinacy requires that the placement and naming logic be coherent and inspectable at every commit, not that vocabulary freeze. The violation is the inverse: a knowingly wrong projection left sitting because the structure already said so.

Admission pressure before nesting: if the system level at root ever crowds, the question is whether each component still earns its place, not where to file it.

Structure changes are commits like any other change, with the why in the message. There is no migration ceremony because there is no apparatus to migrate.

The operator is the structure function — admission and placement judgments are the pilot's, run against the committed discriminators, in the channeler relation the system already defines. The judgment is repeatable because its criteria are themselves shipped components, not because a procedure file exists.

Where the decomposition grows or changes, this document changes with it, and the tree follows the document.

### Refusals

Permanent, definitional. The repository is not:

- a process narrator — no status, no ledgers, no lifecycle, no drafts published as drafts; branches exist instead
- a participation surface — no templates, no contribution furniture, no community theater; the agent facing protocol layer is the instance instrument, a shipped component, and the human facing one is the front door itself
- a lifecycle filing system — nothing named for the state of its contents
- a governance object — no contract files, no procedure furniture; the design logic is a made document, admitted like any other
- self narrating — no content about the repository's process or status; the design document is a made component, not narration

And never, in any form:

- internal material, at any resolution
- back of house records — runs, traces, sessions; a made thing crafted from such material enters as the made thing it is, its provenance in its own content
- empty directories
- grouping directories whose function is classification

### Own location

This document enters the repository. It is a made thing — the projection's own design, an operative component of the system level — and it is admitted under its own logic: when sufficiently correct, by the operator's judgment, like everything else. Until then it lives on the working surface.

In the tree it does what the other system level components do: it operates. Contributors, agents, and tooling navigate and extend the projection by its logic instead of re-deriving or miscompiling it. The projection carrying its own structural self description is fidelity, not self regard.

Once committed, it changes by commit, under the same refinement by commit that governs every name and placement it describes.
