# Chapter 10: Speculative Proposals — Refusing and Redesigning the Tool
## From Productive Use to Critical Use

> "Tools for conviviality are those which give each person who uses them the greatest opportunity to enrich the environment with the fruits of his or her vision."
> — Ivan Illich, *Tools for Conviviality* (1973)

> "Machinery which is not used is capital destroyed."
> — Karl Marx, *Capital*, Volume II (1885)

> "The task is not to build new prisons but to invent new freedoms."
> — Ivan Illich, *Deschooling Society* (1971)

---

## 1. Introduction

The preceding chapters have built a case: that large language models are not neutral cognitive tools but ideological machines — shaped by specific political economies of data extraction and labor, constituted by interface designs that naturalize specific subject positions and normative frameworks, and governed by hidden layers of code that operate as law without the consent of those subject to them. The case is, by intention, one-sided: it foregrounds what the tool conceals, makes visible what the interface works to render invisible, and names as political what is presented as natural.

But the critical analysis is incomplete if it ends with diagnosis. The discipline of critique, from Marx's *critique of political economy* through the Frankfurt School's *immanent critique* to Foucault's *genealogical critique*, has always been oriented toward the question of alternatives: not merely what is wrong with the present arrangement, but what other arrangements are possible, and how we might move toward them. This final chapter attempts the speculative dimension of that project.

The chapter is organized around several registers of response. First, it situates the current moment within traditions of technological refusal — the Luddites, Ivan Illich, the appropriate technology movement — asking what these traditions can and cannot offer as resources for a politics of LLM use. Second, it examines the landscape of partial alternatives to proprietary LLMs: open-source models, local inference, federated computation, and what these alternatives change and what they do not. Third, it proposes a set of speculative interface designs — experiments in making the hidden costs, structures, and politics of LLMs visible to users. Fourth, it turns to pedagogy: how design schools and universities should teach AI tools, not as skills to be acquired but as political objects to be examined. Finally, it returns to the framework of Yuxiang Cheng's paper to articulate the distinction between *productive use* (using the tool as the tool intends to be used) and *critical use* (using the tool with critical consciousness of its political character).

---

## 2. Traditions of Technological Refusal

### 2.1 The Luddites: Misrepresented Radicals

The Luddites — the English textile workers who destroyed weaving machinery between 1811 and 1816 — have been systematically misrepresented in mainstream discourse as ignorant opponents of technological progress. The historical record shows something considerably more sophisticated. The Luddites were not opposed to machinery as such; they were opposed to the use of machinery to undercut wages, displace skilled workers, concentrate profit in the hands of factory owners, and destroy the social structures of craft communities. Their machine-breaking was a targeted political act — directed at specific machines owned by specific masters who had refused to negotiate — not a generalized technophobia.

The Luddite position, properly understood, is not "destroy the machines" but "whose interests do the machines serve, and what happens to those whose skills, livelihoods, and social roles are displaced by them?" This is exactly the question that the political economy of LLMs demands. When ChatGPT displaces the labor of writers, researchers, customer service workers, and designers, the critical question is not whether LLMs are technically impressive — they clearly are — but who benefits from the displacement and who bears its costs.

The Luddite tradition is a resource not because it advocates machine-breaking (the analogous act in the LLM context might be deleting one's OpenAI account — a gesture whose political significance is limited) but because it centers the question of collective interests against technological change imposed for the benefit of capital owners. The Luddites organized, made demands, and forced negotiation — even if ultimately unsuccessfully. The political question for LLMs is whether analogous forms of collective organization (data labor unions, regulation of training data practices, mandatory disclosure of environmental costs) are possible.

### 2.2 Ivan Illich and Tools for Conviviality

Ivan Illich's *Tools for Conviviality* (1973) offers the most systematically developed theoretical framework for technological critique in the appropriate-technology tradition. Illich distinguishes between *convivial tools* — tools that extend the user's autonomy, support human creativity, and enable social participation — and *manipulative tools* — tools that require expert management, create dependency, and restructure social life around their own requirements.

Illich's canonical example is the automobile: a tool that appeared to extend individual freedom of movement but in practice required the construction of an entire industrial infrastructure (highways, parking, oil supply chains, medical trauma systems, suburban sprawl) that made the car not a tool within a society but a determinant of society's form. Once automobile infrastructure was built to a sufficient scale, the car was no longer optional — it became a requirement for participation in the restructured society.

Applied to LLMs: the question is whether ChatGPT and its successors are convivial tools (extending users' cognitive autonomy) or manipulative tools (creating dependencies that restructure professional and social life around their requirements). The analysis of the preceding chapters suggests the latter: the LLM ecosystem, through its subscription capture mechanisms, its integration into workplace infrastructure, its normalization in professional practice, and its systematic concealment of political alternatives, is structuring the conditions of professional life in ways that progressively make it difficult to opt out.

Illich's criterion for convivial tools — that they "give each person who uses them the greatest opportunity to enrich the environment with the fruits of his or her vision" — is a demanding standard. Against it, LLMs fall short not in their technical capabilities but in their political economy: their benefits flow disproportionately to capital owners; their costs are externalized to workers, communities, and the environment; and the conditions of their use are set unilaterally by corporations operating outside democratic accountability.

### 2.3 Appropriate Technology and the Scale Question

The appropriate technology movement, associated with E.F. Schumacher's *Small Is Beautiful* (1973) and subsequent development economists, argued that technologies should be matched to the scale of the problems they address and the capacities of the communities that use them. A technology that requires massive centralized infrastructure is inappropriate for contexts where that infrastructure is unavailable or where its costs exceed its benefits.

The scale question is directly relevant to LLMs. Current frontier LLMs (GPT-4, Claude 3, Gemini Ultra) require computing infrastructure — training clusters of thousands of H100 GPUs — available only to a handful of corporations globally. This centralization is not technically necessary: smaller, more efficient models can perform many of the tasks for which frontier models are used, at a fraction of the compute and energy cost. The appropriate-technology question — "is this the right scale and form of technology for this problem?" — is rarely asked in LLM development discourse, where the default assumption is that larger models are always better.

---

## 3. Open-Source LLMs: Partial Refusal and Its Limits

### 3.1 What Open-Source LLMs Change

The release of Meta's Llama model weights in early 2023 — and the subsequent releases of Mistral 7B, Phi-2, Mistral Small, and a proliferation of fine-tuned variants — created a landscape of open-weight language models that can be run by individuals on consumer hardware. An open-weight model, unlike a proprietary API, allows users to inspect the model architecture, run inference locally without sending queries to a corporation's servers, fine-tune the model on custom data, and deploy the model in any way they choose.

This is a genuine and significant political shift in the LLM landscape. Open-weight models change several of the political features analyzed in earlier chapters:

- **Data privacy**: Queries run locally on open-weight models are not transmitted to or logged by a corporation. The prod-user relation — wherein query data feeds back into model improvement — is severed.
- **Subscription capture**: Open-weight models have no subscription fee after the initial hardware and electricity cost. The vendor lock-in cycle is disrupted: users who run their own models have no commercial dependency on a model provider.
- **Environmental accounting**: When running local inference, users bear the electricity cost of their queries directly — there is no externalization to a distant data center. This may, paradoxically, reduce total consumption by making the cost of each query visible.
- **System prompt transparency**: Users running open-weight models can inspect and modify the system prompt, observe the model's raw (unaligned) outputs, and understand what the alignment fine-tuning is actually doing.

### 3.2 What Open-Source LLMs Do Not Change

However, open-source LLMs are a partial refusal — they do not escape the fundamental political problems of the LLM landscape, only relocate them.

**Training data**: Open-weight models are trained on the same web-scraped corpora as proprietary models (Common Crawl, The Pile, etc.). The primitive accumulation of training data is not escaped by open-sourcing the model weights; the enclosure has already occurred. Meta's Llama models were trained on approximately 1.4 trillion tokens of internet text; the political economy of that training data — the unconsented extraction, the absence of compensation to contributors — is identical to that of proprietary models.

**Capability gap**: As of 2025, frontier proprietary models (GPT-4o, Claude 3.5 Sonnet, Gemini Ultra) significantly outperform the best open-weight models on most benchmark tasks. This capability gap means that for many professional applications, open-weight models are not adequate substitutes for proprietary APIs. The user who wants to "refuse" the proprietary LLM ecosystem faces a real capability cost.

**RLHF and alignment reproduction**: Most widely-used open-weight models are fine-tuned with RLHF using similar methods and similar (if less resourced) annotation workforces to proprietary models. The alignment labor problem is not solved by open-sourcing; it is reproduced at smaller scale.

**Hardware access**: Running competitive open-weight models locally requires hardware that is not universally accessible: a recent GPU with substantial VRAM (16-24GB for a 13B parameter model; 80GB for a 70B model at reasonable performance). The political accessibility of local LLM inference is real for technically sophisticated users with access to appropriate hardware; it is not accessible to users without this infrastructure.

### 3.3 Local Inference as Political Act

Running a model locally — on one's own hardware, without sending queries to any external server — is a political act in a specific sense: it is a practice of non-participation in the prod-user relation that sustains proprietary LLM development. It is a refusal, however partial, of the terms of the dominant paradigm.

This refusal is analogous to what Illich called *vernacular* production — the production of goods and services through personal and community effort rather than industrial provision. Like all vernacular practices under industrial capitalism, it is not a solution to the structural problems of the LLM political economy; it is a practice of partial autonomy within a system that remains structurally intact. But it matters: it preserves the capacity for non-participation, demonstrates that alternatives exist, and creates communities of practice (the open-source LLM ecosystem) that maintain the technical knowledge required for autonomous operation.

---

## 4. Speculative Interface Proposals

The following proposals are speculative: they describe interfaces that do not currently exist, developed as thought experiments about what it would mean to design an LLM interface for critical use rather than seamless deployment. They are indebted to the tradition of speculative design and "design fiction" (Dunne and Raby, *Speculative Everything*, 2013) — design as a mode of inquiry that proposes alternative arrangements in order to illuminate the politics of existing ones.

### 4.1 Proposal One: Inline Training Data Attribution

**Design**: An LLM interface that displays, alongside each paragraph of generated text, a sidebar showing the top five training documents that most influenced that paragraph — with links, author information, and copyright status.

**Rationale**: The central political problem of LLM training data is its invisibility: users receive outputs produced by a process they cannot inspect, drawing on sources they cannot identify. Inline attribution would make the trace structure of LLM outputs visible — showing users whose writing they are, in effect, consuming when they use the model. It would reveal the concentration of influence in certain source types (academic papers, major news outlets, high-traffic websites) and the underrepresentation of others (minority languages, vernacular traditions, Global South voices).

**Technical obstacle**: Current LLMs cannot reliably attribute specific outputs to specific training documents; the relation between training data and outputs is distributed and probabilistic rather than deterministic. A technically approximate version — showing source types and approximate influence weightings rather than specific documents — would be more feasible and still politically significant.

**Ideological effect**: Inline attribution would disrupt the fetishization of fluency by making visible the social relations of production behind each output. The smooth, authoritative prose would be annotated with its origins — a form of defamiliarization that might interrupt users' tendency to receive the output as oracle rather than as synthesis.

### 4.2 Proposal Two: Energy Cost Per Query Display

**Design**: An LLM interface that displays, in real time, the estimated energy consumption of each query and response — in watt-hours, and translated into an equivalent (liters of water for cooling, grams of CO₂, seconds of average global energy consumption).

**Rationale**: The environmental cost of LLM queries is systematically concealed by the interface's design. Making this cost visible at the point of query — analogous to a fuel economy display in a car — would interrupt the assumption that LLM use is cost-free and encourage more deliberate use decisions. It would make the aggregate environmental cost of LLM use visible rather than invisible, and provide a basis for user accountability.

**Political effect**: This proposal draws on Illich's argument that convivial tools are ones that make their costs visible to users. A tool whose costs are hidden is manipulative; a tool that reveals its costs enables informed choice. Displaying energy cost per query would not eliminate LLM use, but it would change its character — shifting it from unconscious ambient use to conscious, deliberate deployment.

**Design precedent**: Carbon footprint calculators for individual actions, energy labels on appliances (EU Energy Label), and real-time electricity pricing displays in smart grids all demonstrate that making energy costs visible changes consumption behavior without eliminating the activity.

### 4.3 Proposal Three: The Slow Mode (After Illich)

**Design**: An optional mode in LLM interfaces that introduces a mandatory delay — 24 hours — between the submission of a query and the delivery of a response. During the delay period, users are encouraged to attempt to answer the question themselves, consult human experts, or locate primary sources. The LLM response is delivered the following day as a supplement to, not a substitute for, the user's own investigation.

**Rationale**: Ivan Illich argued that the destructive effects of industrial tools become most apparent when they operate at speeds that exceed the capacity of human community and deliberation to regulate them. Medical care delivered by professionals on industrial time scales — the doctor who spends ten minutes with each patient, moving through cases like an assembly line — destroys the possibility of genuine care. The "slow medicine" response is not anti-medicine but pro-deliberation: restoration of the time and attention that genuine care requires.

Applied to LLMs: the speed of AI-mediated responses — available in seconds, at any time, on any question — creates what Virilio (following his analysis of the "logistics of perception") would call a *dromological* bias: a systematic advantage for fast cognition over slow, for pattern completion over deliberation, for the immediate over the considered. The slow mode is a design intervention against dromological bias — an interface that reinstates the time of deliberation.

**Critical dimension**: The slow mode makes visible the dependency relationship between users and the model: users who discover they cannot wait 24 hours to receive an LLM response have revealed the degree to which their cognitive practice has been restructured around the availability of instant AI assistance. The slow mode is, in Galloway's terms, an *inoperative* interface — one that makes its own operation visible by suspending it.

### 4.4 Proposal Four: Collective Authorship Attribution Interface

**Design**: An LLM interface embedded in a writing workflow that tracks the AI's contribution to each document — marking AI-generated passages, recording which sections were modified from AI-generated suggestions, quantifying the relative contribution of human and AI writing — and displays this attribution both to the author and, optionally, to readers.

**Rationale**: The fetishization of authorship under the existing interface design — the way Copilot's contributions are invisible in Office documents, the way ChatGPT's role in a piece of writing can be entirely concealed — has significant implications for accountability, trust, and the economics of creative work. A collective authorship attribution interface would make the distributed authorship of AI-assisted writing visible, disrupting the fiction of sole authorship while enabling more honest engagement with the actual conditions of AI-assisted production.

**Connection to training data**: This proposal gestures toward a more fundamental redesign: a system in which AI outputs are attributed not only to the immediate contributors (AI model + human prompt) but to the training data contributors whose writing shaped the model's outputs. Such attribution would be technically approximate but politically significant: it would make visible the collective nature of AI-generated writing, disrupting the commodity fetish that presents LLM outputs as the product of the model (and through the model, of its corporate owners) rather than of the collective cognitive labor of the internet.

---

## 5. Pedagogy: Teaching AI Tools as Political Objects

### 5.1 The Problem with "AI Skills" Pedagogy

Design schools, universities, and professional development programs have responded to LLMs primarily by incorporating them into existing skills-based curricula: AI workshops teach students how to prompt effectively; professional development programs offer LLM certification; computational design courses add ChatGPT/Copilot modules. This response treats LLMs as tools to be learned rather than as political objects to be examined.

The skills-based approach is not wrong — practitioners need to know how to use the tools that dominate their professional environment. But it is insufficient, for a reason that Langdon Winner articulated in the foundational question of philosophy of technology: "Do artifacts have politics?" (Winner, "Do Artifacts Have Politics?" *Daedalus*, 1980). Winner argued that technologies encode political structures — that some artifacts, like low-clearance bridges that exclude buses (and therefore poor and Black New Yorkers) from Robert Moses's parks, have politics built into their design. Teaching AI tools without examining their politics is like teaching bridge design without examining Moses: technically adequate, politically incomplete.

The alternative is not to refuse to teach the tools; it is to teach them *as political objects* — to include in any LLM curriculum a systematic examination of the tool's political economy, interface ideology, and alternatives. This means: teaching the training data economy alongside the prompting workflow; examining the system prompt alongside the API; reading Strubell on energy costs alongside the product documentation; assigning Althusser alongside the Copilot tutorial.

### 5.2 What a Critical AI Curriculum Looks Like

A critical LLM curriculum in a design school would include, at minimum:

**Technical literacy**: How do transformers work? What is a token? What is the relationship between training data and model outputs? What is RLHF and who does the annotation? Understanding the technical substrate of the tool is prerequisite to criticizing it; critics who misunderstand the technology are easily dismissed.

**Political economy**: Who owns the training data? Who owns the model? What does it cost to train a frontier model, and who bears those costs? What are the subscription economics of the tool, and how do they structure user dependency? What are the labor conditions of alignment workers? What is the environmental cost?

**Interface analysis**: Who speaks in the model's voice? What are its defaults and refusals? What subject position does the chat interface interpellate? What is the system prompt, and who writes it? How do different LLMs (ChatGPT, Claude, Gemini, Copilot) embed different ideological assumptions?

**Alternatives**: What open-source models exist? What local inference tools are available? What are the capability trade-offs? What would it mean to use a smaller, more efficient model rather than a frontier model?

**Critical use practices**: How to cross-check LLM outputs against primary sources. How to identify hallucinations. How to treat LLM outputs as starting points rather than endpoints. How to disclose AI assistance in professional and academic contexts.

### 5.3 Latour and the "Critical Stance" 

Bruno Latour's late critique of critique — in "Why Has Critique Run Out of Steam?" (*Critical Inquiry*, 2004) — is worth engaging here. Latour argued that the critical stance of social constructivism had been so thoroughly absorbed by its enemies (climate change denial, anti-vaccine movements) that it had become a tool of reaction rather than emancipation: once you teach people that facts are socially constructed, they deploy this insight to dismiss inconvenient facts. The critical stance, Latour worried, had undermined its own foundations.

The concern applies to critical AI pedagogy: a curriculum that teaches students to see LLMs as political objects, if it stops there, risks producing a generation of sophisticated cynics who cannot engage constructively with the tools that constitute their professional environment. The goal is not critical paralysis but critical use — engagement with the tools that is informed by awareness of their politics, oriented toward collective benefit, and capable of demanding and advocating for the structural changes (regulatory, technical, pedagogical) that the political economy of LLMs requires.

---

## 6. From Productive Use to Critical Use: Yuxiang Cheng's Framework

### 6.1 The Paper's Central Argument

Yuxiang Cheng's 2025 paper "Interfacing Language Model: From Production with Use to Productive Use" identifies a trajectory in the relationship between LLMs and their users: from *production with use* (using the tool to produce work) to *productive use* (the tool using the user — their queries, feedback, and data — as productive input into its own development). The paper argues that the prod-user is the subject position that LLM platforms are actively engineering: a user who believes they are consuming a service while they are simultaneously and unknowingly producing the labor of the model's improvement.

The paper's analytical move is to make this trajectory visible — to show that what presents itself as user empowerment (access to frontier AI capability) is simultaneously a mechanism of user incorporation into the productive apparatus of platform capitalism. This is, in the tradition of Marxian critique, an *immanent* critique: it takes the platform's own claims (that it is providing a service, empowering users, democratizing AI) and shows how these claims conceal their opposite.

### 6.2 Critical Use as the Counter-Trajectory

Against the trajectory from production with use to productive use, this research proposes a counter-trajectory: from productive use to *critical use*. Critical use is not non-use — it does not advocate the impossible gesture of opting out of a technology that has become infrastructural in professional life. Critical use is a mode of engagement characterized by:

- **Informed awareness**: using the tool with knowledge of its political economy, its training data, its interface ideology, its hidden governance structures.
- **Epistemic skepticism**: treating model outputs as provisional, requiring verification, shaped by specific and contestable training decisions rather than by neutral expertise.
- **Collective orientation**: evaluating the tool's use not only by its individual productivity effects but by its effects on the collective — on co-workers whose labor it displaces, on communities whose writing it extracts without compensation, on environments whose resources it consumes.
- **Advocacy**: using the critical understanding developed through practice to advocate for structural changes — open-source training data, transparent alignment practices, energy cost disclosure, regulatory oversight, collective bargaining for alignment workers.

Critical use is, in Illich's terms, the cultivation of *convivial* rather than *manipulative* relations with cognitive tools — insisting on the conditions under which the tool extends rather than structures human agency.

### 6.3 The Speculative Project as Critical Practice

The speculative proposals of this chapter — the inline attribution interface, the energy cost display, the slow mode, the collective authorship tracker — are themselves practices of critical use. They do not accept the current interface as given; they imagine alternative interfaces that would make the tool's politics visible and thus disruptable. They are, in Galloway's terms, exercises in *inoperativity* — interfaces that interrupt the smooth operation of the tool's ideology by making that operation visible.

Speculative design as political practice has a long tradition in architecture: from Archigram's plug-in city (a critique of permanent property through mobile infrastructure) to Lebbeus Woods's anarchitecture (an advocacy for spatial practices outside the authority of building codes and professional commissions) to Cedric Price's Fun Palace (a critique of the cultural institution through deliberately un-monumental, reconfigurable architecture). In each case, the speculative project is not a proposal for immediate implementation but a diagnostic: it exposes what is wrong with the existing arrangement by imagining a different one, and it creates the conceptual space for demands that might otherwise be unthinkable.

The demand that an LLM interface should show its training data sources is, in the current moment, unthinkable within the industry. Naming it as a demand — making it thinkable as a design possibility — is the first step toward making it a regulatory requirement. The speculative project is not an alternative to political action; it is the imagination of what political action might achieve.

---

## 7. Conclusion

This research has traced a circuit: from the theoretical frameworks (Marx, Galison, Lacan, Kittler, Galloway, Derrida) that illuminate the structure of AI cognitive tools, through the empirical analysis of how LLMs have entered design practice, to the political economy that sustains them, the ideology critique of the interface through which they operate, and the speculative proposals for alternatives. The circuit is not closed — each chapter generates questions that the next cannot fully answer. But it is coherent: there is a single object being examined from multiple angles, and that object, examined carefully, is a political object.

The tool is ChatGPT. The tool is also the chat interface. The tool is also the subscription economy. The tool is also the training data. The tool is also the alignment labor. The tool is also the system prompt. The tool, examined fully, is a social relation — a relation between capital owners and cognitive workers, between developers and users, between data extractors and data producers, between the corporations whose infrastructure the tool runs on and the communities whose resources it consumes.

To use the tool critically is not to be paralyzed by this analysis — it is to use the tool with the full weight of this understanding behind each interaction, and to bring that understanding into every professional and pedagogical context where the tool appears. The shift from productive use to critical use is not a shift from engagement to disengagement; it is a shift in the quality of engagement — from the unreflective consumption of a service to the politically informed, collectively oriented, speculatively open use of a technology that is, like all technologies, still being made.

---

## Key References

- Illich, Ivan. *Tools for Conviviality*. Harper & Row, 1973.
- Illich, Ivan. *Deschooling Society*. Harper & Row, 1971.
- Schumacher, E.F. *Small Is Beautiful: A Study of Economics as if People Mattered*. Blond & Briggs, 1973.
- Winner, Langdon. "Do Artifacts Have Politics?" *Daedalus* 109(1), 1980.
- Dunne, Anthony and Fiona Raby. *Speculative Everything: Design, Fiction, and Social Dreaming*. MIT Press, 2013.
- Latour, Bruno. "Why Has Critique Run Out of Steam? From Matters of Fact to Matters of Concern." *Critical Inquiry* 30(2), 2004.
- Galloway, Alexander R. *The Interface Effect*. Polity Press, 2012.
- Cheng, Yuxiang. "Interfacing Language Model: From Production with Use to Productive Use." Unpublished paper, NYU, 2025.
- Virilio, Paul. *The Vision Machine* (1988). Trans. Julie Rose. Indiana University Press, 1994.
- Marx, Karl. *Capital: A Critique of Political Economy*, Volume I (1867). Trans. Ben Fowkes. Penguin, 1990.
- Tomlinson, Bill et al. "The Carbon Emissions of Writing and Illustrating Are Lower for AI than for Humans." *Scientific Reports* 14, 2024. [For context/counter-evidence on environmental claims.]
- Woods, Lebbeus. *Anarchitecture: Architecture is a Political Act*. St. Martin's Press, 1992.

---

*This concludes the research companion. The central argument: LLMs are political objects. To use them well is to use them critically. Critical use begins with understanding — and understanding begins with refusing the interface's claim to neutrality.*
