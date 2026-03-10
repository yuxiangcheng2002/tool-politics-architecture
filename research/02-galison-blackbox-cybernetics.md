# Chapter 02: Galison's "Ontology of the Enemy" — Cybernetics, the Black Box, and Behaviorist Epistemology
## From Anti-Aircraft Predictors to Diffusion Models

> "The enemy pilot, Wiener argued, must be analyzed as a control system — as a series of past positions from which his future positions could be predicted. The enemy was not a subject with intentions to be understood but a statistical pattern to be extrapolated."
> — Peter Galison, "The Ontology of the Enemy: Norbert Wiener and the Cybernetic Vision" (1994)

---

## 1. Introduction

When Stable Diffusion processes the prompt "a modernist villa surrounded by pine forest, evening light," it does not "understand" the architectural space being imagined. It treats that prompt as a vector in a high-dimensional space, identifies its statistical neighborhood in the latent space trained on millions of image-text pairs, and denoises from Gaussian noise toward that statistical region. The building, the forest, the evening light — all are *statistical patterns*, not objects of understanding.

This chapter examines how this mode of knowing became conceivable — how the "black box," which we now use as a casual metaphor for technical opacity, was forged as a specific epistemological instrument in the crucible of World War II. Peter Galison's "The Ontology of the Enemy: Norbert Wiener and the Cybernetic Vision" (Critical Inquiry, 1994) is the essential archaeological text here. Galison traces how Norbert Wiener's wartime work on anti-aircraft predictors produced the conceptual framework that would become cybernetics — and, downstream, artificial intelligence.

The core argument: the black box is not merely a convenience term for "complicated stuff we don't need to understand." It is an epistemological choice — a deliberate decision to treat complex systems (enemies, neurons, users, buildings) as input-output functions whose internal workings need not be understood. This choice, crystallized in WWII servo-mechanisms, permeates AI system design today.

---

## 2. The Historical Scene: Norbert Wiener and the Predictor Problem

### 2.1 The Problem of Anti-Aircraft Fire

During World War II, the problem of shooting down fast-moving aircraft posed an unprecedented challenge to weapons design. A shell takes time to travel to its target; by the time it arrives, the aircraft has moved. The gunner must therefore aim not where the aircraft *is* but where it *will be* — a prediction problem.

Manual aiming by trained gunners was insufficient against fast aircraft. The Allied response was to build servo-mechanical predictors — automated fire-control systems that would track aircraft trajectory and continuously update the gun's aim vector, extrapolating future positions from past positions.

Wiener, at MIT, was tasked with developing the mathematical theory for optimal prediction. His key insight was to treat the aircraft — and, crucially, the human pilot inside it — as a *statistical process*. The predictor needed to model not just the aircraft's physics (straightforward) but the pilot's evasive maneuvers (much harder). 

### 2.2 The Enemy as Statistical Object

Galison's crucial observation is what Wiener did *conceptually* with the enemy pilot:

> "Wiener proposed treating the pilot-aircraft system as a *servomechanism* — a system that could be characterized entirely by its input-output behavior, without reference to its internal states, intentions, or subjective experience."

The pilot — a human being with intentions, fears, training, tactical judgment — was *mathematically abstracted* into a stationary time series. His past positions, fed into the predictor, generated a probability distribution over his future positions. The pilot's *subjectivity* was irrelevant to the prediction problem; only his *behavior* mattered.

This is the founding move of cybernetics as Galison reads it: the behaviorist reduction of a subject to a statistical pattern, then the enclosure of that reduction in a black-box servo-mechanism that acts on the extracted pattern without reference to underlying causes.

### 2.3 Wiener's Own Discomfort

Galison notes, with characteristic nuance, that Wiener was deeply unsettled by this reduction. In *The Human Use of Human Beings* (1950), Wiener worried explicitly about cybernetic methods applied to human social control — the dehumanization implicit in treating persons as statistical processes. Yet his own mathematical framework made this dehumanization systematic and rigorous.

**Gotcha**: Galison is not writing a simple critique of Wiener-as-villain. He is tracing the *genealogy* of an epistemological formation — how the military-industrial complex generated new ways of knowing that outlasted their original context. Wiener's anxiety about his own work is part of the story.

---

## 3. The Black Box: Epistemological Condition, Not Just Technical Metaphor

### 3.1 Origins of the Term

The "black box" originated in WWII electronics engineering. When a system's components were either too complex, too secret, or too dangerous to inspect during operation, engineers would represent it as a sealed box with known inputs and outputs. You could characterize its behavior (output given input) without needing to understand its internal mechanism.

Crucially: this was not a failure of knowledge but a *methodological choice*. The black box was an epistemological tool — a way of managing complexity by formally bracketing it.

### 3.2 The Black Box as Epistemological Formation

Galison's deeper argument is that the black box was not just a technical device but an *epistemological formation* — a structuring assumption about how knowledge works, what counts as explanation, and what level of description is scientifically adequate.

The behaviorist tradition in psychology (Watson, Skinner) made exactly this move: the organism's internal states (consciousness, intention, memory) are bracketed; only stimulus-response behavior is scientifically legible. Wiener's servo-mechanisms gave this behaviorism a mathematical and engineering form.

**The key claim**: behaviorism + servo-mechanism theory → cybernetics → information theory → AI. The epistemological assumption — that you can treat complex systems as input-output functions without attending to internal states — runs throughout this lineage.

### 3.3 Latour's Reading of the Black Box (Relevant Extension)

Bruno Latour, in *Pandora's Hope* (1999), developed the black box as a sociological concept. For Latour, "blackboxing" is a *verb* — a process by which complex assemblages of human and non-human actors become stabilized, routinized, taken for granted. A successful technology is one whose internal complexity disappears from view, leaving only its inputs and outputs visible.

> "Blackboxing is the way scientific and technical work is made invisible by its own success. When a machine runs efficiently... one need focus only on its inputs and outputs and not on its internal complexity." (*Pandora's Hope*, p. 304)

Latour's move: blackboxing is not just an epistemological condition but a social achievement. The black box *had to be made* — through negotiations, trials, failures, alignments. Deconstruction (opening the black box) reveals the social history inside.

**Applied to Midjourney**: The prompt → image process is a triumphant black box in Latour's sense. The internal complexity — CLIP text encoding, latent diffusion, U-Net denoising, VAE decoding — is invisible to the architect. They see: text in, image out. The black box has been successfully established. Opening it reveals: the training data politics, the aesthetic biases, the labor conditions of annotation, the GPU infrastructure, the venture capital structure of Midjourney LLC.

---

## 4. From AA Predictor to Neural Network: Continuities

### 4.1 The Behavioral Treatment of the "Target"

In the AA predictor: the enemy pilot → statistical time series  
In the diffusion model: the "building" → probability distribution in latent space

The parallel is structural. Wiener's predictor does not understand the pilot's intentions; it models his behavioral patterns statistically. Stable Diffusion does not understand what "a modernist villa" *means* as an architectural concept; it models the statistical neighborhood of that prompt in a high-dimensional space trained on image-text pairs.

Both systems are behaviorist in the precise sense: they operate on extracted behavioral patterns (statistical position sequences; image-text co-occurrence statistics) without recourse to subjective meaning or intention.

### 4.2 Feedback and the Closed Loop

Wiener's predictor operated as a feedback loop: gun fires → shell misses → updated trajectory prediction → next shot corrected. Feedback is the central mechanism of cybernetics — the ability of a system to adjust its behavior based on the gap between actual and desired output.

Diffusion models incorporate feedback in a different but analogous form: the denoising process is iterative, with each step adjusting the latent representation toward the target distribution. More dramatically: reinforcement learning from human feedback (RLHF) and similar techniques used in fine-tuning AI models explicitly use human evaluative feedback to steer model behavior — exactly the closed-loop control structure Wiener described.

**Contemporary analog**: When Midjourney users click U1/U2/U3/U4 (upscale) or V1/V2/V3/V4 (variations), they provide preference signal that (in aggregate) feeds back into model improvement. The architect-user is enrolled as a feedback mechanism in the improvement of the system — a prod-user in Yuxiang's framework, simultaneously consumer and unpaid optimizer.

### 4.3 The Enemy as Training Distribution

One of Galison's most provocative observations: to model the enemy as a statistical process is to treat war as an optimization problem — minimize the gap between predicted and actual enemy position, maximize hit rate. This is precisely the logic of machine learning training:

- **WWII**: Minimize prediction error on enemy trajectories → improve predictor
- **AI Training**: Minimize loss on image-text pair prediction → improve model

The "enemy" of the diffusion model is the noise distribution — the random Gaussian noise that the model must learn to remove in order to reconstruct a coherent image from the training distribution. The iterative denoising process *is* the battle against statistical uncertainty that Wiener's predictor first formalized.

---

## 5. Cybernetics and the "Ontology" of the Enemy

### 5.1 Why "Ontology"?

Galison's title — "The Ontology of the Enemy" — is deliberately provocative. Ontology is the philosophical study of what *is*, what kinds of things exist. By calling Wiener's framework an ontological move, Galison argues that the reduction of the enemy to a statistical process was not just an approximation for engineering purposes but a claim about what the enemy *fundamentally is*.

> "The predictor... demanded a particular ontology: the human being as a control system, a goal-directed servomechanism, a system whose inner states could be ignored in favor of its input-output behavior."

### 5.2 The Architectural Ontology of Diffusion Models

This ontological move recurs in AI image generation. When a diffusion model is trained on architectural images, it constitutes a particular *ontology of architecture* — a claim (implicit, technical, encoded in weights) about what buildings *are*:

- Buildings are combinations of materials, lighting conditions, geometric forms, and atmospheric effects that can be described as high-dimensional probability distributions
- "Architectural quality" is what is statistically frequent in the training distribution of images tagged with high-quality architectural photography
- A "good building" is what the model's latent space has learned to associate with positive text descriptors from Dezeen, Architectural Record, and Instagram

This is not neutral. It is a specific ontology — one that privileges the *photographed* building over the *inhabited* one, the *spectacular* over the *quotidian*, the *photogenic* over the *tactile*. And it is imposed on every architect who uses the tool without their explicit consent or even awareness.

### 5.3 The Human as Servomechanism

Wiener's predictor modeled the enemy as a servomechanism. Galison notes that this same modeling logic was applied — by Wiener himself and by subsequent cyberneticians — to the human brain, to organizations, to economies. If the enemy pilot *is* (functionally, ontologically) a control system, then human beings *generally* are control systems.

Applied to the architect: AI image generation tools implicitly model the architect-user as a control system — a system that inputs prompts and responds to image outputs with preference signals (upscale, variation, regenerate). The architect's "intentions" are black-boxed; only their behavioral outputs (prompt text, selection clicks) enter the system. This is exactly Wiener's move applied to the designer.

---

## 6. The Epistemological Consequences for Architecture

### 6.1 Knowledge Without Understanding

The most consequential feature of the black-box epistemology for architecture: it is possible to produce visually convincing architectural representations without understanding the architecture being represented.

A skilled architectural renderer of the pre-AI era necessarily understood something about the building — structure, materiality, circulation, scale — because rendering required modeling these in 3D software. The process of representation was also a process of disciplinary understanding.

The diffusion model produces architectural images *from statistical patterns* — without any internal representation of structure, materiality, circulation, or scale as architectural concepts. The image looks right because it statistically resembles right-looking architectural images; not because it models the underlying architectural logic.

**This is a direct consequence of the black-box epistemology**: if you only need to match input-output behavior (prompt → convincing image), you don't need to model internal states (architectural program, structural logic, spatial experience).

### 6.2 The Loss of Disciplinary Feedback

Traditional architectural representation — hand drawing, physical model, CAD/BIM rendering — required engaging with the discipline's internal logic. Errors were disciplinarily meaningful: a wall thickness that was structurally wrong looked wrong in the model; a perspective that misrepresented spatial experience was recognizable as false by a trained eye.

AI-generated architectural images fail in disciplinarily incoherent ways. A Midjourney image of a building might show:
- Structurally impossible cantilevers (not flagged because the model has learned that dramatic cantilevers are aesthetically valued)
- Windows that don't correspond to interior spaces
- Materials that are photorealistic but thermally impossible
- Scale figures that make the building feel grand but are physically incorrect

These errors are invisible *from the outside* — they look fine in the image — but would be catastrophic in an actual building. The black-box epistemology severs the feedback between representation and disciplinary knowledge.

### 6.3 Architecture as Behaviorist Field

More broadly: if AI image generation becomes the primary representational medium of architecture, it imposes a behaviorist epistemology on the field. Buildings become (in the eyes of the tool) input-output functions: prompt in, image out. The "good building" is the one whose statistical neighborhood in latent space corresponds to visually attractive patterns. The building's performance — spatial, structural, environmental, social — is irrelevant to the representational machine.

This is the cybernetic inheritance in its purest architectural form: the building becomes an "enemy" to be modeled statistically, a pattern to be predicted and reproduced, not a site of dwelling, structure, and social life to be designed.

---

## 7. Galison's Method and Its Limits

### 7.1 Galison as Historian of Science

Galison's essay is written as a history of ideas and practices, not as critique in the political-economic sense. He traces the genealogy of the black-box concept without necessarily prescribing what to do about it. This is both a strength (rigorous historical specificity) and a limitation (no normative horizon).

For Yuxiang's framework: Galison provides the genealogical depth — the *where did this come from* — that grounds the critique of AI tools. Without Galison, we might naturalize the behavioral treatment of complex systems as simply how computers work. With Galison, we see it as a historically specific choice made in the specific context of WWII military research, with its particular ideological and practical commitments.

### 7.2 What Galison Doesn't Say

Galison does not discuss AI image generation (his essay predates the current wave). He also does not extend his analysis to the *users* of cybernetic systems — how the epistemology of the black box shapes subjectivity. That extension is Galloway's contribution (Chapter 5) and partly Lacan's (Chapter 3).

**For the architecture assignment**: Use Galison to establish the genealogical claim that black-box epistemology is not inevitable but historically produced. Then use Latour to show how this black box must be *opened* to reveal its social history. Then use Galloway and Kittler to analyze what the opened box contains.

---

## 8. Application to Architecture Assignment

### 8.1 Midjourney as Black Box

Midjourney is a paradigmatic black box in all three senses:

1. **Technical**: The architecture (model, weights, fine-tuning) is proprietary and undisclosed
2. **Epistemological**: Users need only specify inputs (prompt, parameters) and evaluate outputs; internal processing is irrelevant
3. **Social (Latour)**: The black box *has been successfully made* — users don't ask how it works; the box has become a stable, taken-for-granted tool in architectural workflows

**Opening the box** (deconstruction in Latour's sense) reveals:
- CLIP text encoder from OpenAI (itself a black box)
- Latent diffusion model (Rombach et al., 2022) architecture
- Training data (undisclosed for Midjourney, approximately LAION-5B + curated subset)
- Midjourney-specific fine-tuning on "aesthetic" images (curated dataset of "good" art)
- RLHF or similar feedback mechanisms (plausibly used, undisclosed)
- Multiple GPU clusters (undisclosed location, ownership)
- Venture capital structure (Midjourney LLC, series not publicly disclosed)

### 8.2 The Behaviorist Architect

The diffusion model's behaviorist epistemology shapes the architect-user through the interface:
- The architect does not need to understand the building; they need to produce a prompt
- The architect does not evaluate spatial quality; they evaluate image quality
- The architect does not make structural decisions; they select aesthetic variants
- The architect does not engage the discipline; they manage a black box

This is the cybernetic formation in architectural practice: the architect-as-servomechanism, whose meaningful inputs are prompts and whose outputs are curated images.

### 8.3 A Table of Epistemological Comparisons

| System | Input | Black Box | Output | "Enemy" |
|--------|-------|-----------|--------|---------|
| Wiener AA Predictor | Aircraft past positions | Servo-mechanism | Gun aim vector | Enemy pilot as statistical process |
| Midjourney | Text prompt | Diffusion model | Image | "Good architecture" as statistical distribution |
| Traditional Rendering | 3D model + lights + camera | Renderer (open) | Image | Physical light simulation (understood) |
| BIM Model | Parametric inputs | Software (partially open) | Drawing set | Building as data model (understood) |

Note how in traditional rendering and BIM, the "black box" is open or semi-open — the architect can interrogate how the output was produced. In Midjourney, the box is sealed.

---

## 9. Summary

Galison's "Ontology of the Enemy" is essential reading for understanding AI image generation in architecture because it traces the genealogical origin of the black-box epistemology that underlies AI systems. Wiener's WWII work on anti-aircraft predictors produced a powerful methodological formation: treat complex systems (enemy pilots, neural processes, users) as input-output functions, model their behavior statistically, and enclose the model in a servo-mechanism that acts without reference to internal states or subjective meanings.

This formation — behaviorist, statistical, operational — is structurally identical to the epistemology of modern AI systems, including diffusion models for architectural visualization. The "building" in Midjourney is exactly the enemy pilot in Wiener's predictor: a statistical pattern to be matched, not an object of understanding to be grasped.

The consequences for architecture are profound: a representational tool that cannot engage with the discipline's internal logic (spatial experience, structural integrity, program, context) is also a tool that cannot produce representations adequate to architectural judgment. It produces images that are statistically consistent with "good architecture" while being structurally indifferent to what makes architecture good.

The critical move, following Galison and Latour, is to *open the black box* — to make visible the historical, social, and technical conditions of the diffusion model's production, and to refuse the epistemological reduction of architecture to statistical pattern-matching.

---

## Key References

- Galison, Peter. "The Ontology of the Enemy: Norbert Wiener and the Cybernetic Vision." *Critical Inquiry* 21(1), Autumn 1994, pp. 228-266.
- Wiener, Norbert. *Cybernetics: Or Control and Communication in the Animal and the Machine* (1948). MIT Press, 1961.
- Wiener, Norbert. *The Human Use of Human Beings: Cybernetics and Society* (1950). Da Capo Press, 1988.
- Latour, Bruno. *Pandora's Hope: Essays on the Reality of Science Studies*. Harvard University Press, 1999. Chapter 7: "On the Partial Existence of Existing and Non-existing Objects," and discussion of blackboxing throughout.
- Rombach, Robin, et al. "High-Resolution Image Synthesis with Latent Diffusion Models." *CVPR 2022*. [Technical paper for Stable Diffusion architecture]
- Skinner, B.F. "Behaviorism at Fifty." *Science* 140(3570), 1963. [For behaviorist context]

---

*Next chapter: Lacan's Seminar II — Psychoanalysis, Cybernetics, and the Imaginary Machine*
