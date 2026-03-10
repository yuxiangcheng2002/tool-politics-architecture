# Chapter 08: Political Economy of Large Language Models
## Primitive Accumulation, Vendor Capture, and the Hidden Costs of Cognitive Infrastructure

> "The discovery of gold and silver in America, the extirpation, enslavement and entombment in mines of the indigenous population... are all things which characterize the dawn of the era of capitalist production. These idyllic proceedings are the chief moments of primitive accumulation."
> — Karl Marx, *Capital*, Volume I (1867)

> "The so-called primitive accumulation, therefore, is nothing else than the historical process of divorcing the producer from the means of production."
> — Karl Marx, *Capital*, Volume I (1867)

---

## 1. Introduction

The chat interface of ChatGPT presents itself as a service relationship: you ask a question; the model answers; you continue your work. The exchange appears frictionless, non-commercial (at the free tier), and above all, simple — as if a vast and complex industrial system were not operative behind the text box. This simplicity is not accidental; it is the product of deliberate design. The political economy of large language models — the structures of capital accumulation, labor extraction, environmental cost, and market power that sustain these systems — is systematically concealed by the interface that presents their outputs.

This chapter makes that political economy visible. Drawing on Marx's analysis of primitive accumulation, his framework of fixed and variable capital, and the concept of the "prod-user" developed in Yuxiang Cheng's 2025 paper, this chapter examines: the extraction of training data from the commons of human writing; the outsourcing of alignment labor to precarious workers in the Global South; the vendor lock-in mechanisms through which OpenAI and its competitors convert free users into paying subscribers; the structural integration of LLMs into Microsoft's productivity monopoly; the environmental costs of training and inference; and the ongoing legal battles over the expropriation of intellectual property. Together, these elements constitute not a story about technological innovation but about a new form of primitive accumulation — the enclosure of the cognitive commons.

---

## 2. The Prod-User and the Platform Economy

### 2.1 Yuxiang Cheng's Framework

In "Interfacing Language Model" (2025), Yuxiang Cheng develops the concept of the *prod-user* — a subject position that combines production and consumption in a form specific to platform economies. The prod-user does not merely consume the outputs of the LLM; they contribute to its improvement through their use. Every query submitted to ChatGPT, every thumbs-up or thumbs-down rating, every conversation that reveals new patterns of use and failure, contributes to the model's development. The prod-user pays — not only in subscription fees but in data, in feedback, in the intellectual labor of formulating queries and evaluating responses — while remaining largely unconscious of this contribution.

Cheng's framework extends Tiziana Terranova's analysis of "free labor" in internet economies (Terranova, "Free Labor: Producing Culture for the Digital Economy," 2000) and Axel Bruns's concept of "produsage" (Bruns, *Blogs, Wikipedia, Second Life*, 2008). Terranova argued that the internet economy systematically extracts value from users who believe they are simply using services: their content creation, their social connections, their behavioral data, all constitute unpaid labor that sustains platform capitalism. ChatGPT's prod-user relation extends this logic into the domain of cognitive labor: by using the model, users produce the feedback signal (RLHF annotations, preference signals, usage patterns) that makes the model better, thus increasing its commercial value.

### 2.2 OpenAI's Business Model: From Nonprofit to Capped-Profit to For-Profit

The political economy of ChatGPT cannot be understood without understanding the peculiar corporate history of OpenAI. Founded in 2015 as a nonprofit with a mission to "ensure that artificial general intelligence benefits all of humanity," OpenAI transitioned in 2019 to a "capped-profit" structure — investors could receive returns up to 100x their investment, after which excess profits would revert to the nonprofit — a structure without precedent in corporate law. In early 2025, the company announced plans to convert fully to a for-profit public benefit corporation, severing the remaining nonprofit governance structures.

This trajectory — nonprofit → capped-profit → for-profit — is not an incidental corporate evolution; it is a paradigm case of what Wendy Brown has called the "stealth revolution" of market logic into domains previously organized around public goods (Brown, *Undoing the Demos*, 2015). The original nonprofit framing of OpenAI served to attract philanthropic capital, elite scientific talent, and public trust; the subsequent transitions served to attract venture capital at scales ($13 billion from Microsoft, $6.6 billion in additional funding as of 2024) incompatible with nonprofit governance.

The business model that emerged is structured around tiered access:

| Tier | Price | Access Level |
|------|-------|-------------|
| Free (GPT-3.5/4o mini) | $0 | Limited queries, older model |
| Plus (GPT-4o) | $20/month | Priority access, latest model |
| Pro (o1/o3) | $200/month | Frontier reasoning models |
| API (pay-per-token) | Variable | Programmatic access |
| Enterprise | Custom | Organizational deployment |

The tiered structure encodes a specific ideology of access: the free tier creates product awareness and generates prod-user feedback while providing a deliberately degraded experience; the Plus tier converts engaged users who have experienced the limits of the free tier into subscribers; the Pro tier extracts premium payments from users (typically professionals) whose work depends on frontier capability. The free-to-paid conversion is not accidental; it is engineered through the experience of encountering model capability limits precisely when professional need is highest.

---

## 3. Training Data as Primitive Accumulation

### 3.1 The Web as Enclosure

Marx's analysis of primitive accumulation describes the process by which common land — resources held collectively and used by communities under customary right — was enclosed by capital, converted into private property, and incorporated into the production process. The enclosure of the English commons between the sixteenth and eighteenth centuries displaced rural populations, destroyed subsistence economies, and created the landless proletariat that would staff industrial factories.

The training data of large language models represents a contemporary analog to this process. The internet — Common Crawl, Reddit, Wikipedia, Project Gutenberg, academic preprint archives, news sites, forums, and the accumulated textual production of three decades of digital life — is a commons: a vast repository of human writing produced through individual and collective effort, under the assumption (often mistaken) that it was being shared for human use. OpenAI's training of GPT models on this commons — scraping it, processing it, and encoding it as the weights of a commercial product — represents an enclosure: the conversion of a common resource into private capital.

Common Crawl, the primary training corpus for most frontier LLMs, contains petabytes of web text accumulated since 2011. It includes the writing of journalists, academics, novelists, programmers, amateur bloggers, Reddit posters, and Stack Overflow contributors — none of whom were compensated for their contribution to the training corpus, none of whom consented to their writing's use as training data for commercial systems, and none of whom benefit from the commercial products their writing helped create.

This is primitive accumulation in a precise sense: the "means of production" being appropriated is the general intellect — the collective cognitive labor of the internet era — and its enclosure creates a proprietary cognitive infrastructure controlled by a small number of private corporations.

### 3.2 Books3 and the Literary Commons

A particularly contentious instance of this enclosure is the use of Books3, a corpus of approximately 196,000 copyrighted books assembled from shadow library sources (primarily Bibliotik, a private torrent site for ebooks) and incorporated into training corpora used by OpenAI, Meta, and other LLM developers. Books3 includes published works by living authors — novelists, journalists, academics — without consent or compensation.

The scale of the appropriation is significant: 196,000 books represents a substantial portion of the commercially significant English-language literary canon of the past several decades. The works of professional writers — Sarah Silverman, Paul Tremblay, and others who became plaintiffs in class-action suits — were used to train models that compete directly with the market for their work. An LLM trained on a novelist's complete works can produce prose in their style, summarize their plots, and answer questions about their themes — functions that reduce the market value of engaging the novelist's work directly.

The class-action suit Silverman v. OpenAI (Northern District of California, 2023) and the related cases constituted the first significant legal challenge to the training data accumulation practices of LLM developers. The legal question — whether training on copyrighted works constitutes fair use — remained unresolved as of early 2026, but the political significance is clear: the authors are contesting the terms of an enclosure that has privatized their intellectual labor without compensation.

### 3.3 The NYT v. OpenAI Litigation

The highest-profile legal challenge to LLM training data practices is The New York Times Company v. OpenAI Inc. (Southern District of New York, filed December 2023). The Times' complaint alleges that OpenAI trained GPT models on millions of Times articles, enabling the model to reproduce verbatim text from Times articles, summarize and repackage Times journalism, and compete directly with the Times as a source of information and analysis — all without licensing fees.

The complaint included striking evidence: when prompted in particular ways, GPT-4 would reproduce extended verbatim passages from Times articles, including investigative journalism that represented significant reporting investment. This demonstrates that the model has not merely "learned from" Times content but has, in some sense, memorized it — treating copyrighted journalism as persistent training data rather than a source to be cited.

The litigation raises fundamental questions about the category of "transformative use" in copyright law when applied to statistical learning. Does training a model on copyrighted text constitute the same kind of transformative use as a human learning from reading? Or does the commercial deployment of a model trained on that text constitute reproduction and distribution of derivative works? Courts have not yet established precedent on these questions, but their resolution will determine the legal architecture of the LLM training economy.

---

## 4. RLHF and the Labor of Alignment

### 4.1 What RLHF Does

Reinforcement Learning from Human Feedback (RLHF) is the technique primarily responsible for converting a raw language model — which will produce any statistically plausible completion of any input — into the "helpful, harmless, and honest" assistant that ChatGPT presents as. The process involves human annotators who evaluate model outputs, labeling some as preferable to others; these human preferences become the training signal for a reward model that guides subsequent fine-tuning.

RLHF is, in other words, the process of making the model safe, useful, and commercially deployable. Without RLHF, GPT models produce outputs that are frequently offensive, harmful, factually wrong, and strategically misleading. The alignment labor — the human work of reading model outputs and labeling them as good or bad — is not peripheral to the LLM product; it is constitutive of it.

### 4.2 The TIME Magazine Investigation and Global South Labor

In January 2023, TIME Magazine published an investigation revealing that OpenAI had contracted with Kenyan workers, through the outsourcing firm Sama, to label harmful content in ChatGPT's training data. Workers were paid between $1.32 and $2.00 per hour to read and categorize text describing sexual abuse, graphic violence, and hate speech — content that OpenAI needed to filter from the model's outputs.

The investigation described workers experiencing acute psychological distress — symptoms consistent with vicarious trauma — as a consequence of sustained exposure to harmful content. The work was performed under non-disclosure agreements that prevented workers from discussing their tasks publicly. The workers were classified as independent contractors rather than employees, denying them benefits, workplace protections, and mental health support.

This labor arrangement is significant beyond its ethical dimensions (though those are severe). It reveals the fundamental structure of the LLM political economy: the cognitive interface of the product (the helpful, safe, fluent assistant) is produced through the invisible, precarious, psychologically damaging labor of workers in the Global South, whose contribution to the product is systematically concealed by the interface design. The seamless, "safe" conversation experience that users of ChatGPT enjoy is produced by the labor of Kenyan workers paid $2 per hour to process extreme content — a labor relation that is both spatially remote (invisible to users) and constitutive of the product they experience.

This is a precise example of what Kittler meant by media materialism: the material conditions of a medium's production are systematically obscured by the user experience the medium offers. The "clean" interface is possible only because the dirty work of its production has been externalized to a workforce whose conditions of labor are never visible in the output.

### 4.3 The Global Division of Alignment Labor

The Sama arrangement is not an anomaly but a structural feature of LLM development economics. The outsourcing of content moderation and data labeling to low-wage labor markets in Kenya, the Philippines, India, and Venezuela is an industry-wide practice, documented by Adrienne Williams, Milagros Miceli, and Timnit Gebru in "Exploited Labor Behind Artificial Intelligence" (2022). The wages, working conditions, and psychological support provided to these workers vary but are uniformly below the standards that would be required in labor markets where LLM developers are headquartered.

The Global South labor that makes LLMs safe and commercially viable is also disproportionately affected by the economic displacements that LLMs are producing: the automation of data entry, content creation, and customer service tasks hits labor markets already characterized by precarious employment and weak regulatory protection harder than it hits the high-skill, high-wage labor markets where LLM developers operate.

---

## 5. Vendor Lock-in and Market Monopolization

### 5.1 The Lock-in Cycle

The political economy of LLM platforms follows a well-documented pattern in platform economics: attract users with free or subsidized access → generate network effects and dependency → extract subscription revenue from converted users. This pattern is familiar from social media, streaming, and cloud storage; its application to cognitive tools has specific implications that distinguish it from these earlier cases.

Cognitive tool lock-in is deeper than content or social network lock-in because it involves the restructuring of *workflows*. A user who integrates ChatGPT into their professional workflow — using it for drafting, research, code generation, and analysis — has not merely formed a preference for the tool; they have adapted their practice to its capabilities and limitations. Switching costs are high not because of data export difficulties (though those exist) but because of cognitive adaptation: the practitioner has learned to think *with* ChatGPT, to formulate problems in ways that the model can handle, to anticipate its failure modes and work around them. This cognitive adaptation is not easily transferred to alternative tools.

### 5.2 Microsoft/OpenAI Integration: Soft Monopolization

The $13 billion investment by Microsoft in OpenAI, and the subsequent integration of OpenAI's models across Microsoft's product suite under the Copilot brand, represents a structural move toward monopolization of cognitive tool infrastructure that merits sustained critical analysis.

Microsoft's product ecosystem — Windows, Office (Word, Excel, PowerPoint, Outlook), Teams, LinkedIn, GitHub, Azure — constitutes the dominant infrastructure of knowledge work in most corporate and institutional settings worldwide. The integration of Copilot into this ecosystem means that LLM-mediated cognitive assistance is now embedded in the tools that knowledge workers use for their entire professional day. Unlike ChatGPT, which users must consciously navigate to (opening a browser tab, formulating a query), Copilot is ambient — present in the text editor where documents are drafted, the spreadsheet where data is analyzed, the email client where communications are written, the code editor where software is built.

This ambient presence constitutes a form of soft monopolization: not the elimination of competitors through legal exclusion but the normalization of a specific LLM infrastructure as the default cognitive environment for professional work. When an institution deploys Microsoft 365 with Copilot (at approximately $30 per user per month), it effectively mandates the use of OpenAI's model for all knowledge work within the institution — not through policy but through friction: Copilot is *there*, in the toolbar, at no additional perceived cost, requiring no workflow change to use.

The GitHub Copilot case is particularly striking. GitHub, acquired by Microsoft in 2018, is the dominant infrastructure for collaborative software development. GitHub Copilot, launched in 2021 and now standard in most professional development environments, provides LLM-mediated code completion within the development environment itself. The model was trained on public GitHub repositories — including code released under GPL and other copyleft licenses. The use of GPL-licensed code as training data, and the deployment of a commercial product whose outputs may contain GPL-licensed code fragments, raised significant legal and political questions about the compatibility of LLM training with open-source licensing (Matthew Butterick et al. v. GitHub Inc., 2022).

---

## 6. Environmental Footprint

### 6.1 The Energy Cost of Intelligence

Emma Strubell, Ananya Ganesh, and Andrew McCallum's landmark 2019 paper "Energy and Policy Considerations for Deep Learning in NLP" provided the first systematic accounting of the energy costs of training large NLP models. Training a single large transformer model, they found, could emit as much CO₂ as five cars over their entire lifetimes. Subsequent studies found that this was, if anything, an underestimate: the energy cost of training GPT-4 has been estimated at approximately 50 gigawatt-hours — the equivalent of over 4,000 US households' annual electricity consumption.

Inference costs — the energy required not to train the model but to respond to individual queries — are lower per query but aggregate at enormous scale. Sam Altman, OpenAI's CEO, stated in 2023 that ChatGPT consumed approximately 10 times as much energy per query as a standard Google search. Independent estimates by researchers at UC Riverside suggest that a ChatGPT conversation consumes as much energy as 500 ml of water for cooling. Given that ChatGPT was receiving approximately 10 million queries per day as of early 2023 (and significantly more subsequently), the aggregate environmental cost is substantial.

### 6.2 Water, Cooling, and Invisible Infrastructure

The environmental cost of LLMs is not only energetic; it is hydrological. Data centers, including those running LLM inference, require vast quantities of water for cooling. Microsoft's data centers consumed approximately 1.7 billion gallons of water in 2022 — a figure that increased significantly with the scaling of LLM infrastructure. The water infrastructure for LLM operation is disproportionately sited in water-stressed regions: the Phoenix metropolitan area, where Microsoft and other cloud providers operate large data centers, is experiencing unprecedented groundwater depletion.

The environmental costs of LLM infrastructure are, like the alignment labor costs, systematically externalized from the product experience: the chat interface conceals them. The user who asks ChatGPT a question sees a text response; they do not see the watt-hours consumed, the water evaporated, or the carbon emitted. This concealment is not politically neutral — it allows the environmental costs of LLM infrastructure to be externalized from the product price, borne by communities adjacent to data centers and by the global climate, rather than incorporated into the subscription fee or factored into use decisions.

### 6.3 Geographic Concentration and Sacrifice Zones

The physical infrastructure of LLM computation is geographically concentrated: in Northern Virginia (the largest data center market in the world), in Ireland and Sweden (for European regulatory compliance), and increasingly in regions with cheap electricity — coal-rich regions of the American West, hydropower-adjacent areas of the Pacific Northwest. This geographic concentration creates what Rob Nixon calls "slow violence" (Nixon, *Slow Violence and the Environmentalism of the Poor*, 2011): environmental degradation that is spatially remote from the product's users, temporally extended, and politically invisible.

The communities that host LLM data center infrastructure — often low-income, often communities of color — bear the noise pollution, the water depletion, the heat island effects, and the property tax consequences of industrial-scale computing operations from which they derive no direct benefit and over which they have no democratic control. This is a form of environmental colonialism: the cognitive benefits of LLMs flow to knowledge workers in prosperous cities; the environmental costs flow to communities that are sacrificed to the infrastructure requirements of a technology they may barely use.

---

## 7. Copyright, IP, and Expropriation

### 7.1 The Legal Landscape

The legal battles over LLM training data — Silverman v. OpenAI, NYT v. OpenAI, Andersen v. Stability AI, and the GitHub Copilot class action — constitute a challenge to the property regime of LLM development that remains unresolved. The central legal question — whether training on copyrighted works constitutes fair use — is a question that existing copyright doctrine was not designed to answer, because the category of "machine learning" did not exist when the doctrine was developed.

The standard fair use analysis (under 17 U.S.C. § 107) considers four factors: the purpose and character of the use (commercial vs. educational, transformative vs. reproductive); the nature of the copyrighted work; the amount and substantiality of the portion used; and the effect on the market for the original work. LLM training is ambiguous on all four factors: it is commercial; it uses entire copyrighted works; it may or may not be transformative; and its market effects are contested.

The more interesting question, from a political economy perspective, is not what current copyright law says but what the legal resolution of these cases will mean for the LLM training economy. If courts find that training on copyrighted works requires licensing, the cost of training frontier models increases dramatically — a constraint that favors incumbent developers (who already have trained models) over new entrants, and that creates pressure for licensing arrangements that may further concentrate ownership of training data.

### 7.2 The Open Web's Enclosure

Beyond the formal copyright cases, the broader political economy of training data is characterized by an accelerating enclosure of previously open internet content. As awareness of training data extraction has grown, content producers have begun implementing technical measures to prevent scraping (via robots.txt restrictions, rate limiting, and pay-walled access), and have begun negotiating licensing deals with LLM developers.

The AP, Reuters, and several major newspaper groups have reached licensing agreements with OpenAI, Google, and other LLM developers. These deals typically involve payment of between $1 million and $5 million per year for access to news archives — a figure that researchers at Columbia Journalism Review have characterized as significantly below the fair market value of the content licensed.

The enclosure dynamic thus operates in two directions simultaneously: LLM developers have enclosed the open web commons through historical training data extraction; and content producers, recognizing this, are now re-enclosing their content behind licensing walls and paywalls. The result is a progressive privatization of the textual commons, accelerated by the LLM economy, in which both the training data and the trained models are private property.

---

## 8. Summary

The political economy of large language models is not a supplement to their technical analysis; it is its foundation. The seamless, helpful interface of ChatGPT is produced through: the extraction of training data from the human cognitive commons without consent or compensation; the outsourced alignment labor of precarious workers in the Global South; the tiered subscription structure that converts free users into paying subscribers; the structural integration of LLM capabilities into Microsoft's productivity monopoly; the environmental costs borne by communities adjacent to data center infrastructure; and the ongoing legal expropriation of intellectual property that the copyright system exists, at least nominally, to protect.

These are not accidental features of a technology in its early stages — they are structural features of a political economy that organizes the development of cognitive infrastructure for private profit extraction. Understanding them is prerequisite to the critical practice that Chapter 10 will develop: not abandonment of the tools, which is neither possible nor sufficient, but a politics of refusal, transparency, and collective alternatives.

The chat interface is, in this light, not just an interface but a concealment device — its simplicity and pleasantness systematically obscure the complex, costly, and often unjust political economy that produces each response. To use the tool critically is to keep that political economy in view even as the interface works to render it invisible.

---

## Key References

- Marx, Karl. *Capital: A Critique of Political Economy*, Volume I (1867). Trans. Ben Fowkes. Penguin, 1990.
- Marx, Karl. *Grundrisse* (1857-58). Trans. Martin Nicolaus. Penguin, 1973.
- Cheng, Yuxiang. "Interfacing Language Model: From Production with Use to Productive Use." Unpublished paper, NYU, 2025.
- Terranova, Tiziana. "Free Labor: Producing Culture for the Digital Economy." *Social Text* 18(2), 2000.
- Strubell, Emma, Ananya Ganesh, and Andrew McCallum. "Energy and Policy Considerations for Deep Learning in NLP." *Proceedings of the 57th ACL*, 2019.
- TIME Magazine. "OpenAI Used Kenyan Workers on Less Than $2 Per Hour to Make ChatGPT Less Toxic." January 18, 2023.
- Williams, Adrienne, Milagros Miceli, and Timnit Gebru. "Exploited Labor Behind Artificial Intelligence." *NOEMA*, 2022.
- Brown, Wendy. *Undoing the Demos: Neoliberalism's Stealth Revolution*. Zone Books, 2015.
- Nixon, Rob. *Slow Violence and the Environmentalism of the Poor*. Harvard University Press, 2011.
- Kittler, Friedrich. *Gramophone, Film, Typewriter* (1986). Trans. Geoffrey Winthrop-Young and Michael Wutz. Stanford University Press, 1999.
- *The New York Times Company v. OpenAI Inc., Microsoft Corp.* Case No. 1:23-cv-11195 (S.D.N.Y., filed December 27, 2023).

---

*Next chapter: The Chat Interface as Ideology Machine — how the design of the text box encodes and naturalizes a specific politics of knowledge.*
