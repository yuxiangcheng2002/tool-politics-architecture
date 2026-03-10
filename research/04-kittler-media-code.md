# Chapter 04: Kittler's Media Materialism — Code, Writing, and the Hardware Behind Software
## From Gramophone to GPU: Architecture's Material Unconscious

> "The general digitalization of channels and information erases the differences among individual media. Sound and image, voice and text are reduced to surface effects, known to consumers as interface. Sense and the senses turn into eyewash. Their media-produced glamour will survive for an interim period as a by-product of the invasion of the digital."
> — Friedrich Kittler, *Gramophone, Film, Typewriter* (1986/1999)

> "Only that which is switchable exists."
> — Friedrich Kittler, attributed

---

## 1. Introduction

Friedrich Kittler's media theory is, at its core, a materialism of inscription. Against the dominant tradition in media studies that focuses on content, meaning, and representation, Kittler insists on the *material substrate* — the physical technologies through which signals are recorded, stored, and transmitted. The meaning is secondary; what matters is the channel, the storage medium, the transmission apparatus, and — especially — the code.

For Kittler, the digital computer represents the apotheosis of this logic: all media are now run through a single universal machine (the Turing machine, physically instantiated as silicon chips), and all signals are rendered as bit patterns — switchable, programmable, reproducible. The "gramophone effect" — the uncanny illusion of presence — becomes the "screen effect": the pixel grid that offers any surface, any image, any world.

This chapter applies Kittler's framework to architectural AI tools, arguing that: (1) the shift from hand drawing to CAD to BIM to AI image generation represents a Kittlerian media succession, with each stage imposing new material constraints on architectural imagination; (2) AI image generation is the terminal point of this succession — the moment when architectural representation becomes entirely bit-pattern, entirely statistical, entirely determined by the logic of the universal machine; (3) the "face" of the digital (the interface) hides the hardware reality that actually determines what is possible; and (4) for Kittler, as for no other theorist, the hardware must be named.

---

## 2. Media Materialism: The Fundamental Argument

### 2.1 Against Hermeneutics

Kittler's polemic target is hermeneutics — the tradition (from Dilthey to Gadamer) that treats cultural objects as texts to be interpreted, meaning to be excavated. For Kittler, hermeneutics is a pre-media illusion: it was possible only before the invention of technical media (gramophone, film, typewriter) that began to store and transmit data independently of human interpretation.

> "Media determine our situation." (*Gramophone, Film, Typewriter*, preface)

This is Kittler's most famous and most misunderstood claim. He is not arguing for technological determinism in the crude sense (technology causes everything). He is arguing that technological media *delimit* what is thinkable, sayable, and representable — they constitute the "conditions of possibility" for cultural production, in a Kantian sense that is also a Foucauldian one.

Kittler's method: instead of asking "what does this medium mean?", ask "what does this medium *do* technically, and how does that technical operation constrain and enable cultural production?"

### 2.2 The Discourse Network / Aufschreibesystem

In *Discourse Networks 1800/1900* (1985), Kittler introduced the concept of the *Aufschreibesystem* (writing-down system, or "notation system") — the ensemble of technologies and practices through which a culture inscribes, stores, and processes its data. In 1800, the Aufschreibesystem was centered on literary writing, alphabetic inscription, the book. In 1900, it was fragmented across gramophone, film, typewriter — each capturing a different aspect of human expression that the book had previously monopolized in impoverished form.

**Applied to architecture**: Architecture has its own Aufschreibesystem — the ensemble of representational technologies through which architectural ideas are inscribed and processed. This system has undergone several major shifts:

| Period | Primary Aufschreibesystem | Key Technology |
|--------|--------------------------|----------------|
| Pre-modern | Hand drawing, manuscript | Pen, paper, scale rule |
| Industrial | Mechanical drafting, blueprint | T-square, drafting machine, diazo printing |
| Post-war | Technical drawing standards, print | Parallel rule, Letraset, xerography |
| Digital 1 | Computer-aided drafting | AutoCAD, plotters, DWG format |
| Digital 2 | Building Information Modeling | Revit, IFC standard, parametric scripts |
| AI | Prompt-to-image generation | CLIP, diffusion models, Discord |

Each shift does not merely change *how* architecture is drawn — it changes what kinds of architectural thinking are possible, what kinds of buildings can be conceived.

### 2.3 "Only That Which Is Switchable Exists"

Kittler's aphorism — "only that which is switchable exists" — is the most concise statement of digital ontology. In the digital regime, something exists as a data object only if it can be represented as a bit pattern and processed by a Turing machine. The entire phenomenological richness of the world is subjected to this condition: if it cannot be digitized, sampled, quantized, it does not exist *in the system*.

For architecture: a building exists in the AI image generation system to the extent that it has been photographed, uploaded, tagged, and incorporated into training data. The millions of unbuilt buildings, the demolished buildings, the buildings too poor or ordinary to be photographed for Dezeen — these do not "exist" in the Kittlerian sense within the diffusion model's ontology. Only what was switchable (digitized, uploaded, scraped) exists.

---

## 3. Gramophone, Film, Typewriter: The Three Channels

### 3.1 The Three Technical Media

Kittler's *Gramophone, Film, Typewriter* (1986) analyzes three late-19th century inventions as three channels corresponding to three aspects of human expression:

- **Gramophone** (Edison, 1877): continuous acoustic signal, stores and reproduces the Real of sound (voice, noise, music) without interpretation
- **Film** (Lumière, 1895): continuous optical signal, stores and reproduces the Real of vision (movement, time) without interpretation
- **Typewriter** (Remington, 1874): discrete symbolic inscription, reroutes writing from handwriting to machine-produced uniform characters, disconnecting the hand from the letter

The gramophone and film capture the *analog* — the continuous real signal. The typewriter inaugurates the *digital* — discrete, switchable symbols.

### 3.2 The Analog/Digital Distinction in Architecture

In pre-digital architectural representation:
- The **hand drawing** is analogous to the gramophone: it captures the architect's hand, their individuality, their material engagement with paper. The line is continuous, variable, expressive.
- The **physical model** is analogous to film: it captures spatial experience in material form, as an analog of the building.

In digital representation:
- **AutoCAD** is the typewriter: discrete lines, exact coordinates, standardized symbols. The architect's hand is replaced by the cursor; individuality is replaced by precision.
- **AI image generation** extends this further: the image is not even the output of discrete coordinates but of statistical sampling in a continuous latent space — paradoxically, a return to the analog-continuous at the surface, but through a digital apparatus underneath.

**The Kittlerian irony**: AI images *look* like analog images — continuous, smooth, photographic. But they are the outputs of purely digital, symbolic operations (diffusion denoising on discrete latent vectors). The analog surface is an effect of the digital machine. This is the "eyewash" Kittler predicted: sense as the by-product of the digital invasion.

---

## 4. The Stack: Layers of Hardware Reality

### 4.1 The Principle of Downward Causation

One of Kittler's key arguments is that hardware determines software, software determines operating system, operating system determines applications, applications determine user experience — and that this chain of downward determination is systematically hidden from users by each software layer.

> "Programmers... will lose in the future the ability of influencing their own work. They work in higher and higher programming languages, which determine the interface between programmers and machines while the machine itself becomes increasingly inaccessible. They operate as users of software packages which behave like black boxes." (*Literature, Media, Information Systems*)

### 4.2 The Full Stack for Midjourney

| Layer | Components | Hidden from User? |
|-------|-----------|-------------------|
| Physical | GPU silicon (NVIDIA), VRAM, cooling, power | Yes (completely) |
| Hardware abstraction | CUDA runtime, driver stack | Yes |
| Compute framework | PyTorch/JAX, tensor operations | Yes |
| Model architecture | U-Net, CLIP, VAE, attention mechanisms | Yes (proprietary) |
| Trained weights | ~865M parameters (SD), undisclosed (MJ) | Yes (proprietary) |
| Inference serving | Midjourney backend, load balancing | Yes |
| API | Midjourney API / Discord bot API | Partially (terms of service) |
| Interface | Discord slash commands, /imagine | Visible but opaque |
| User experience | Prompt box, image grid | User sees this |

For Kittler, each layer hides the one below. The architect sees only the user experience — the prompt box and the image grid. The entire stack, from GPU silicon to model weights to inference serving, is invisible. The architect experiences the smooth interface while the material reality — the carbon, the silicon, the electricity, the finance — is systematically occluded.

### 4.3 Hardware Determinism in Aesthetic Terms

Kittler would insist that the aesthetic properties of AI-generated architectural images are *determined at the hardware level*:

- **GPU parallelism**: The diffusion model's ability to process all pixels simultaneously in each denoising step produces images with uniform high-resolution texture — different from the variable texture of hand drawing or the selective detail of traditional render
- **VRAM limits**: The maximum image resolution possible at inference is limited by GPU memory — this is why Midjourney v4 defaults to 1024×1024 and requires additional computation for higher resolutions
- **Floating-point arithmetic**: The mathematical operations in the diffusion process (32-bit or 16-bit float) introduce specific kinds of numerical "noise" that manifest as subtle artifacts
- **Quantization effects**: When model weights are quantized (reduced precision) for faster inference, specific visual patterns emerge or disappear

These are not aesthetic choices; they are hardware facts. But they determine, at the most fundamental level, what kinds of images are producible. Kittler would say: to understand why Midjourney images look the way they do, you must understand CUDA, VRAM, and NVIDIA's chip architecture.

---

## 5. Code as Writing: The Executable Dimension

### 5.1 Kittler on Code and Literature

In *Literature, Media, Information Systems*, Kittler argues that programming code represents the most consequential form of "writing" since the invention of the alphabet. Code is writing that *does* — it does not describe actions, it *executes* them.

> "Before these men [Turing, Shannon, von Neumann]... the philosopher of media was one who wrote about writing. Today, he is the programmer who writes programs that write."

This is directly relevant to Yuxiang's framework: the prompt is a form of writing, but it is writing addressed to an executable system. The prompt is not quite code (it is natural language), but it is also not quite descriptive writing (it executes). This ambiguous position — between natural language and code, between description and execution — is what Yuxiang analyses through Austin and Derrida (Chapter 6).

Kittler's addition: the execution itself is always grounded in hardware. The prompt "executes" (in the loose sense) only because there is a physical process — electrons moving through silicon, floating-point operations, matrix multiplications — that receives the text, processes it through the model, and returns an image. The prompt's "performativity" is ultimately a material fact, not a linguistic one.

### 5.2 The Turing Machine and Architectural Universality

Turing's universal computing machine can simulate any other discrete state machine. This is the theoretical basis for the universality of the digital computer: any discrete process can, in principle, be computed. For architecture, this means that any architectural rule-system, any geometric operation, any material simulation, can in principle be run on a computer.

But — and this is Kittler's point — "in principle" always hits against "in practice." What can actually be computed in finite time, with available memory and processing power, is always a constrained subset of what is theoretically possible. The constraints are not logical but material: GPU VRAM, inference time, training data availability, architectural choices in the model.

**For diffusion models**: The Turing-machine universality means that, in principle, a diffusion model could represent any visual distribution. In practice, it represents the distribution of its training data — which is not universal but historically specific, aesthetically biased, geographically skewed.

### 5.3 Software Has No Ontological Status for Kittler

This is perhaps Kittler's most provocative claim: software, strictly speaking, does not exist. There are only hardware processes, and software is the human-readable description of what those hardware processes do. The "software" of Midjourney — the Python scripts, the model architecture definitions — have no being; only the electrical processes in the GPU have actual existence.

This is not a useful engineering claim, but it is a powerful philosophical one: it insists that the material substrate is always the ground of any digital abstraction. The "intelligence" of Midjourney is not a property of software but a description of specific electrical processes in specific chips, consuming specific amounts of power, generating specific amounts of heat.

---

## 6. Gramophone-Film-Typewriter Applied to Architecture's Media History

### 6.1 Architecture's Pre-Digital Media Channels

Following Kittler's tripartite structure, architectural representation before digitization operated through three analogous channels:

- **Drawing** (≈ Typewriter): discrete symbolic inscription on paper — plans, sections, elevations. Discrete (lines, dimensions, symbols), reproducible (blueprint), standardized (drawing conventions).
- **Photograph** (≈ Film): continuous optical registration of the built work — storing the Real of built architecture in a way that drawing could not.
- **Physical model** (≈ Gramophone): analog 3D storage of spatial relationships — preserving the Real of volume, proportion, and relation in a way neither drawing nor photograph could.

### 6.2 The Digital Compression of Channels

Kittler's argument about digital media: the three channels (gramophone, film, typewriter) are all subsumed under the digital computer, which can simulate all three. The gramophone effect is reproduced by audio software; the film effect by video and 3D rendering; the typewriter by word processing.

In architecture:
- AutoCAD subsumed the drawing channel
- 3D rendering (3ds Max, Maya, Rhino) subsumed the photograph-of-architecture channel
- Digital parametric models (Rhino Grasshopper) subsumed the physical model channel

AI image generation represents a further stage: it subsumed *all three* simultaneously — generating photographic-quality images from statistical patterns without separate modeling, lighting, and photography stages.

### 6.3 What is Lost in the Subsumption

Kittler was not celebratory about this subsumption. The gramophone preserved the Real of the voice — the grain, the breath, the death of the singer — in a way that sheet music (discrete notation) could not. When all channels are run through the digital computer, what is lost is the specificity of each medium's Real.

In architecture: what is lost when all representation is run through the digital is:
- The **hand's knowledge** preserved in drawing (the hand knows things the eye doesn't)
- The **spatial Real** preserved in physical models (the tactile, the gravity-specific, the light-on-material)
- The **photographed Real** of actual buildings (the contingency, the weather, the inhabited mess)

AI image generation produces images that simulate all three while preserving none. The "grain" of the medium — its material specificity — is gone. What remains is a smooth, universal, statistically averaged image-surface: Kittler's "eyewash" perfectly instantiated.

---

## 7. The "Face" of the Black Box: Interface as Concealment

### 7.1 Kittler on the Human-Computer Interface

In *Literature, Media, Information Systems*, Kittler analyzes the graphical user interface (GUI) as a systematic concealment of hardware reality. The desktop metaphor (Xerox PARC, 1973; Apple Macintosh, 1984) replaced the command-line interface with visual icons representing files, folders, documents — a "friendly" spatial metaphor that hid the actual operations of the operating system.

For Kittler, the GUI is ideological in a precise sense: it produces a humanized fiction (the "desktop," the "document," the "folder") that conceals the technical reality of file systems, memory addresses, and processor states. The user operates in the metaphor, not the reality.

### 7.2 Discord as Kittlerian Interface

Midjourney operates through Discord — itself a layer of concealment. The architect types in a chat interface designed for gaming communities, sends a slash command (/imagine), and receives images in a message thread. The interface hides:

1. **The API call**: The Discord message triggers an API call to Midjourney's servers
2. **The compute cluster**: The API call dispatches a job to a GPU cluster
3. **The model execution**: The cluster runs the diffusion model over ~50 denoising steps
4. **The CDN delivery**: The result is stored and served through a CDN
5. **The feedback collection**: The user's selections feed into usage analytics

The Discord interface presents this entire pipeline as a "conversation" — a friendly, social, familiar metaphor. The architect feels like they are talking to a collaborative assistant. They are actually submitting compute jobs to a proprietary GPU cluster through a API wrapped in a social media interface.

### 7.3 The Face and What It Hides

For Kittler (following Heidegger on *Gestell*/enframing), the "face" of technology — the interface — is itself a technological product, designed to conceal the enframing structure. The more user-friendly the interface, the more thoroughly the hardware reality is concealed.

**Midjourney's aestheticized interface** — the image grid, the bold prompt typography, the "magical" effect of images appearing from noise — is an extreme instance of this. The interface aestheticizes its own operation, making the output appear as if it emerged from an enchanted creative process rather than from matrix multiplications in a data center.

---

## 8. Application to Architecture Assignment

### 8.1 The Kittlerian Critique of Architectural AI

Kittler's framework suggests a critique structured around three questions:

1. **What hardware grounds this aesthetics?** Trace the specific GPU chips, data centers, and material infrastructure that produce Midjourney's characteristic image quality. Argue that this hardware is not neutral but shapes the aesthetics in determinate ways.

2. **What media did AI subsume?** Identify what was lost when AI image generation subsumed the three channels of architectural representation (drawing, photography, physical model). Argue that the loss of medium-specificity is a loss of disciplinary knowledge.

3. **What does the interface hide?** Analyze the Discord-based Midjourney interface as a systematic concealment of the material, labor, and political realities of the production process. What does "opening the interface" — looking behind the face — reveal?

### 8.2 Architecture's Media History (Kittlerian Chart)

| Medium | What it Stores | Specificity Preserved | Knowledge Form |
|--------|---------------|----------------------|----------------|
| Hand drawing | Geometric relations + designer's hand | Tactile, proportional | Spatial-relational |
| Physical model | Volumetric relationships | Gravitational, material | Haptic, structural |
| Blueprint | Exact dimensions for construction | Technical precision | Construction logic |
| Architectural photograph | Built reality | Site, time, inhabitation | Documentary |
| CAD (AutoCAD) | Discrete coordinate geometry | Dimensional accuracy | Geometric-technical |
| BIM (Revit) | Parametric, data-rich model | Multi-disciplinary | Systems integration |
| 3D Rendering (V-Ray) | Light simulation on 3D model | Material-optical | Atmospheric-spatial |
| AI Image Generation | Statistical image distribution | Nothing specific | Aesthetic-statistical |

The final row is the critical observation: AI image generation preserves no medium-specific knowledge. It is pure aesthetic surface, disconnected from any specific material base.

### 8.3 The Hardware Argument

For the architecture assignment: make the Kittlerian hardware argument explicit. The claim that AI tools "democratize" architectural visualization conceals a hardware reality:

- The GPU chips required for inference are manufactured by NVIDIA, subject to geopolitical supply chains and export controls
- The data centers that run Midjourney are geographically concentrated (primarily US and EU)
- The energy requirements of large-scale inference are substantial and growing
- The semiconductor manufacturing process involves rare earth minerals with complex extraction politics

"Democratization" occurs at the interface level (low subscription price, easy access) while the hardware layer represents an unprecedented *concentration* of capital and control. Kittler would say: don't be fooled by the face.

---

## 9. Summary

Kittler's media materialism provides the "hardware argument" that complements the other theoretical frameworks in this research. Against hermeneutic and user-experience accounts of AI image generation, Kittler insists: go to the hardware. Understand the silicon, the VRAM, the CUDA cores, the floating-point operations. These material realities determine, at the most fundamental level, what kinds of images are producible, what aesthetic effects are possible, what is the "grammar" of the latent space.

The shift from hand drawing to CAD to BIM to AI image generation represents a Kittlerian media succession — each stage further compressing architectural representation into bit patterns, further subsuming medium-specific knowledge into universal digital processing. AI image generation is the terminal point: the moment when architectural representation becomes pure statistical surface, disconnected from any specific material knowledge.

The interface conceals this. Discord's friendly chat metaphor, the "magical" appearance of images from noise, the subscription model's low prices — all hide the GPU cluster, the energy cost, the training data extraction, the venture capital structure. The Kittlerian move is to strip the interface away and name the hardware reality behind it.

---

## Key References

- Kittler, Friedrich A. *Gramophone, Film, Typewriter* (1986). Trans. Geoffrey Winthrop-Young and Michael Wutz. Stanford University Press, 1999.
- Kittler, Friedrich A. *Literature, Media, Information Systems: Essays*. Ed. John Johnston. G+B Arts International, 1997.
- Kittler, Friedrich A. *Discourse Networks 1800/1900* (1985). Trans. Michael Metteer. Stanford University Press, 1990.
- Winthrop-Young, Geoffrey. *Kittler and the Media*. Polity Press, 2011. [Best secondary introduction]
- Manovich, Lev. *The Language of New Media*. MIT Press, 2001. [Different approach but compatible on "database" logic]
- Galloway, Alexander R. *Protocol: How Control Exists After Decentralization*. MIT Press, 2004. [Complements Kittler on network layer]
- Turing, Alan. "Computing Machinery and Intelligence." *Mind* 59(236), 1950. [The universal machine and imitation game]

---

*Next chapter: Galloway's Interface Effect — the interface as ideology machine*
