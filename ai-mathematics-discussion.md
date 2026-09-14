---
first_published: 2026-09-12
last_revised: 2026-09-14
---

# zh

## 从一个突然出现的答案开始
<!-- aside: opening -->

Navier–Stokes 方程描述水和空气等流体的运动。三维不可压缩方程的解能否始终保持光滑，是七个千禧年大奖难题之一。问题既属于偏微分方程，也牵连飞机设计、天气预报和血液流动。所谓有限时间奇异性，是指一个从光滑状态开始的解，在有限时间内出现速度发散等现象。黏性通常会抑制这种失控，非线性却可能把能量不断推向更小的尺度；两种作用如何平衡，正是问题长期困难的原因。

2026 年 9 月的第一周，OpenAI 把这道问题带进了一场关于 AI 数学能力的公开竞赛。按照公司的说明，8 月 28 日起，内部训练中的新模型显示出很强的数学能力。9 月 1 日，团队听到两个千禧年问题可能已经被解决的传闻，于是让近一百个智能体并行探索未解问题。约五十小时后，系统先得到无外力 Euler 方程的结果。Euler 方程可以看作忽略黏性的流体模型；这条路线随后把研究资源引向 Navier–Stokes。

OpenAI 说，智能体在 9 月 5 日得到 Navier–Stokes 的解析解答，距离启动约 88 小时。之后，团队累计投入约 17 小时在 Lean 中完成形式化和核验，并于 9 月 8 日公开论文与代码。Lean 是一种交互式定理证明工具；形式化证明以明确的命题、依赖和检查规则呈现，可以由可信内核重复检查。OpenAI 将这项工作描述为在所声明的范围内解决 Navier–Stokes 千禧年问题，同时把它作为模型能力和研究速度的公开记录。

只看这条时间线，新闻的核心很清楚：一个长期未解的问题出现了新的、可以继续检查的结果，而且形式化材料随论文一起公开。争论从另一条研究时间线进入公共记录开始。

## 同一周，另一条研究线进入公共记录

Tristan Buckmaster 和 Antonin Alpöge 此前已经围绕流体方程工作了很长时间。Buckmaster 的公开陈述说，他们在 8 月 15 日取得了关于带光滑外力的 Boussinesq 方程和 Euler 方程的进展，并把数月的研究对话、提示和材料保存在 Codex 会话中。对普通读者来说，这些会话更像研究过程的工作台：它们记录问题怎样被提出、线索怎样被试探，承担的是过程记录的作用。

9 月 3 日，关于大型语言模型可能解决重大开放问题的传闻开始流传。Buckmaster 随后联系 OpenAI，并在 9 月 6 日的两次通话中询问：内部系统是否访问过他和 Alpöge 在此前两个月留下的未公开研究，或者是否曾把这些材料用于训练。Buckmaster 公布的文书记录了这些问题和通话内容。9 月 7 日，他和 Alpöge 提前公开了不可压缩多孔介质方程、二维 Boussinesq 方程和三维不可压缩 Euler 方程的三个有限时间爆破结果，以及对应的 Lean 形式化。这些结果研究的是相邻方程，属于同一条流体奇异性研究路线；提前公开也让他们的贡献和时间戳进入了同一份公共记录。

公开文书还记载了优先权与署名安排的争议，包括是否应把 Anthropic 的员工 Levent Alpöge 列入联合发布。9 月 10 日，OpenAI 更新说明，称 Buckmaster 之前两个月的 Codex 提示不可能影响内部系统或训练，也称研究人员和智能体在对方成果公开前没有看到这些成果；公司同时表示，完成项目和 Lean 核验后曾希望安排并行发布，并承认对方在带外力 Euler 结果上的优先权。

双方在数据隔离、优先权和署名安排上的公开说法并不相同。要判断这些说法，需要访问日志、训练数据来历、通信记录、版本时间戳和能够由独立方检查的审计材料。争议的焦点因此从证明本身扩展到研究者能否在公平的条件下保存、说明和发表自己的工作。

## Tao 的介绍与联合声明把问题带到更大的背景

9 月 7 日，Terry Tao 介绍 Alpöge–Buckmaster 的工作时，称其为令人振奋的新进展，并解释了三个有限时间爆破结果与无外力 Navier–Stokes 之间的关系。他也提到，最初的证明文字非常难读，作者正在把它改写成专业论文；在这个过程中，解题、理解证明结构和提炼可复用的方法并不在同一个时间尺度上。

9 月 11 日，Tao 发布了题为《A Severe Misalignment of AI in Mathematics》的联合声明，初始签署者包括 25 位菲尔兹奖得主。声明把概念理解和数学洞见放在共同体最重视的位置，把解题描述为获得这些理解的工具或代理。它同时批评 AI 公司把著名开放问题当作 benchmark，担心竞赛会把发布速度推到前面，挤压认真写作、方法提炼、先行工作引用和知识整合。

声明发布在 OpenAI 公开论文后三天，因而自然进入同一场讨论。声明文字面上讨论的是更广泛的 AI 数学实践，并没有对某一篇论文作出数学裁定。它提出的中心因果链却与当前事件相连：当一个答案被当作模型能力的公开成绩，速度和轰动性会不会压过解释、归属和共同体吸收结果所需的时间？这使后面的判断必须把数学、传承和研究过程分开。

## 为什么要把同一场事件拆成三个问题

这一周的材料之所以容易混在一起，是因为一个结果、一次发布和一场伦理争议几乎同时出现。把它们放在一起讨论很自然，给它们使用同一套证据却会失去重点。因此需要分别回答三个问题：

- 这个形式化结果在什么范围内成立？
- 一个正确结果怎样成为可以被别人理解、引用和继续发展的共同知识？
- 结果有价值，是否足以说明产生和发布它的过程也恰当？

第一个问题需要论文、形式化命题、证明项、依赖关系、内核检查和复现。第二个问题需要时间、解释、引用、教学和后续研究。第三个问题需要数据边界、通信、署名、优先权和独立审计。三者可以同时推进，却不能由其中一项替代另外两项。

## 第一问：形式化的结果在什么范围内成立

形式化把自然语言里的命题、变量、假设、依赖和证明写成检查器能够处理的对象。若论文中的主张与形式命题逐项对应，依赖关系公开，内核确实接受证明项，其他人也能按相同条件重现检查，那么结论就在所声明的范围内获得了明确的正确性边界。它有没有揭示新的结构、是否容易阅读、能否进入教材，则需要另一组证据。

SAT 提供了一个很小、但很有力的参照。面对一个固定的布尔实例，求解器可以给出一个满足赋值；若断言实例不可满足，则可以给出一份独立检查器能够验证的证书。证书通过以后，工程系统可以在这个范围内排除一个设计、确认一组约束，或者继续下一步计算。使用者不必先理解求解器搜索过的每一条路径，证书也不必先被提炼成优雅理论，结果才有用。

形式化的 AI 证明沿着同一条逻辑链走得更远：它给出精确命题、证明对象、依赖和内核检查结果。若自然语言和形式命题忠实对应，证明没有隐藏缺口，检查在公开的基础上可以重现，那么这个结果在其范围内就具有可使用的正确性。它还可能需要很长时间才能被人类读懂，结构解释、方法推广和教材化也许要在之后完成；这些工作的延后不改变已经建立的形式证据。

正确性和知识理解，是两种可以并行发展的贡献。不能因为一个形式化结果尚未在几天内变成教材，就把它的科学价值归零。若相同范围、相同形式状态的结果由人类提出，研究共同体会给它数月乃至数年的核查和消化时间；仅仅因为来源是 AI，就要求它在几天内同时交出完整的概念解释，否则不承认结果，这就把来源置于作品之上，形成了双重标准。对形式化不忠实、依赖有缺口、论文难读或归属不准确的批评都可以成立，但批评应当指向这些具体问题。

关于把形式化结论做成可调用、边界清楚的数学组件，我们在另一篇文章中展开讨论，这里只保留它与本节的连接：结果先要有可检查的边界，之后才谈如何被稳定地复用。
<!-- aside: contextual -->

## 第二问：知识传承如何发生

联合声明强调认真写作、方法解释、准确归属、教学和后续研究，这些要求确实构成数学共同体的长期基础。一个结果进入文献、课堂和后续工作之后，才会逐步成为别人能够理解和继续发展的共同知识。作者公开结果以后，仍然要为这段路承担责任。

知识传承是独立的贡献，也是结果进入共同知识的过程。它不需要被设成使用正确结果的前置许可。一个经过可靠检查的结论，可以先在清楚的范围内被引用、复现和调用；与此同时，人们再花时间解释它的证明结构、寻找更好的表述、发现可以推广的方法。对于数学来说，留下可传承的知识是一项功能，留下边界清楚、可以可靠复用的组件是另一项功能。两者可以彼此加强，完成的时间也可以不同。

庞加莱猜想提供了一个具体的时间尺度。Perelman 的第一篇相关预印本发表于 2002 年 11 月 11 日，随后两篇材料在 2003 年 3 月和 7 月出现；从第一篇预印本到初始材料基本齐备，已经过去约八个月。此后，Hamilton、Kleiner、Lott、Tian 等人的核查、解说和整理继续推进。到 2006 年，距离第一篇预印本约三年半，这项证明才逐步形成共同体可以公开依靠的理解。它在最初几天没有完成教材化，并没有抹去它当时已经带来的数学内容。

OpenAI 在 9 月 8 日公开论文和形式化材料，到本文 9 月 14 日修订时只有六天。六天足以让读者看到论文和代码，远不足以让共同体完成所有核查、解释和结构提取。我们可以批评发布中的文字是否清楚、相关工作是否完整，也可以要求后续论文把证明写得更容易阅读。尚未完成的传承工作，不能倒过来成为结论没有价值的证明。

如果一个人类作者提交同样的形式化结果，我们会把理解和教材化看作需要时间的后续工作。对 AI 参与的结果也应保留同样的时间尺度。评价应当随着证据推进：先看命题是否成立，再看解释是否可靠，最后看它能否进入更广的数学知识体系。
<!-- aside: poincare -->

## 第三问：数学价值与研究过程是否是同一件事

一个结果的数学价值，与它是怎样产生和发布的，是两组不同的问题。模型公司即使带有商业目标，也可能完成科学上有用的工作；动机不会自动抹去结论的价值。反过来，结论即使正确，也不能替过程中的数据使用、署名或优先权问题提供豁免。

就这次事件而言，需要分别追问：未公开的 Codex 材料是否被访问或用于训练；研究者的提示和数据是否与内部系统隔离；贡献和作者名单是否准确；在得知相关研究存在以后，是否仍然提供了公平的并行发布安排；谁掌握了决定公开时间的权力。Buckmaster 的文书与 OpenAI 的更新给出了不同叙述，公开材料可以确认争议存在，却还不足以独立裁定每一项事实。

如果一家公司为了抢先发布而使用了未公开研究，或者让研究者在数据边界和署名上处于明显弱势，即使最后的数学结论正确，也属于研究治理失败。如果日志、训练数据来历、时间戳、通信和独立审计显示系统保持了隔离，研究者仍然有权追问优先权和署名如何被处理。数学证据和过程证据各自回答自己的问题。

因此，判断一个结果有没有价值，和判断一次发布是否恰当，应当分别进行。前者要看论文、形式代码、依赖和复现；后者要看访问日志、数据来历、通信记录、署名安排和可供独立第三方检查的审计。把其中一组证据拿来替代另一组，都会让讨论偏离问题本身。

## 从结果到共同知识：一条可追溯的科学流程
<!-- aside: programme -->

一个新的机器辅助结果可以沿着一条连续的科学流程前进。流程中的每一步都增加一种可信度，也都留下可以被后来者检查的记录：

- 先固定命题、适用范围、形式证明、依赖关系、公理状态和可复现的检查方式。
- 再把形式对象写成研究者能够顺畅阅读的论文，交代问题背景、先行工作、例子和证明路线。
- 将论文和代码作为公开预印本发布，接受外部审评，记录问题、修订和更正。
- 让论文、形式代码、版本时间戳、引用和公开讨论保持在同一条可追溯记录上。
- 最后由综述、课堂、教材和后续研究逐步提取结构，让结果既能被理解，也能被可靠复用。

这些阶段可以随着工作推进分别完成，不需要等到所有工作结束才开始。形式结果可以先成为可核验、可引用的记录，知识传承随后继续；论文的可读性和外部审评也可以在公开之后不断提高。不同阶段有不同的证据，公开文本应当把已经完成的部分和仍在进行的工作写清楚。

## 让发现、核验与传承各得其时

这场事件让几个常被混在一起的判断重新分开：一个结论是否正确，一个结论是否已经被共同体充分理解，以及一次研究过程是否尊重了参与者和公共规则。它们彼此相关，却各自需要证据，也各自有自己的时间。

我们会继续把每个结果沿着同一条链推进：固定命题和形式边界，完成可重复的内核检查，把证明写成人类能够阅读的论文，公开预印本并接受外部审评，再把修订、解释和后续应用留在可追溯的版本记录中。这样做同时保留了知识的初版，也给它进入共同知识和可靠复用留下道路。

数学成果可以以两种方式长久留下来：成为人类能够理解、教学和传承的知识，也成为边界清楚、能够在后续工作中可靠调用的组件。科学的发展需要这两种时间，也需要让它们在同一份诚实的记录中相遇。新技术改变发现和核验的速度，科学共同体要做的，是把这种速度转化为能够被检查、被解释、被传给后来者的成果。

# en

## It began with an answer that appeared almost overnight
<!-- aside: opening -->

The Navier–Stokes equations describe the motion of fluids such as water and air. Whether smooth solutions of the three-dimensional incompressible equations remain smooth is one of the seven Millennium Prize Problems. It belongs to the theory of partial differential equations, yet it also touches aircraft design, weather prediction, and the study of blood flow. A finite-time singularity is a loss of regularity, such as an unbounded velocity, that develops from initially smooth data in finite time. Viscosity tends to damp this instability, while nonlinear interactions can concentrate energy at ever smaller scales; the tension between them is what makes the problem so difficult.

In the first week of September 2026, OpenAI brought this problem into a public contest over AI mathematical ability. According to the company’s account, an internal model under training began showing unusually strong mathematical performance on August 28. On September 1, the team heard reports that two Millennium Problems might have been solved and began testing the system on open problems and other high-impact questions. Nearly one hundred agents worked in parallel for about fifty hours. Their first result concerned the unforced Euler equations, an inviscid model of fluid motion, and the team then shifted its resources toward Navier–Stokes.

OpenAI says that the agents reached an analytic answer for Navier–Stokes on September 5, about 88 hours after the effort began. The team then spent a reported 17 hours in total formalizing and checking the result in Lean, and released a paper and code on September 8. Lean is an interactive theorem prover. A formal proof presents its proposition, dependencies, and checking rules in a form that a trusted kernel can check again. OpenAI described the work as solving the Millennium problem within its stated formulation and presented the release as a public record of model capability and research speed.

On that timeline, the news is easy to understand: a long-standing problem had produced a new result that others could continue to check, and formal material was released with the paper. The controversy entered when a second research timeline reached the public record in the same week.

## A second research timeline entered the public record

Tristan Buckmaster and Antonin Alpöge had already been working on fluid equations for a long time. In a public statement, Buckmaster said that on August 15 they had made progress on the Boussinesq and Euler equations with smooth forcing, and that months of research conversations, prompts, and materials had been kept in Codex sessions. For a reader, those sessions are best understood as a workbench for a research process: they record how questions were posed and how lines of attack were tested.

On September 3, reports began circulating that a large language model might have solved a major open problem. Buckmaster then contacted OpenAI. In two calls on September 6, he asked whether the internal system had accessed the unpublished work he and Alpöge had left in Codex during the previous two months, or whether those materials had been used for training. The document he published records the questions and the calls. On September 7, he and Alpöge released three finite-time blow-up results, for the incompressible porous-medium equation, the two-dimensional Boussinesq equation, and the three-dimensional incompressible Euler equation, together with Lean formalizations. These results concern neighboring equations in the same line of fluid-singularity research; the early release placed their work and its timestamp in the same public record.

The public document also records a dispute over priority and authorship, including whether Anthropic employee Levent Alpöge should be included in a joint release. In an update on September 10, OpenAI said that Buckmaster’s Codex prompts from the previous two months could not have affected its internal system or training, and that its researchers and agents had not seen the other results before their release. The company also said that, after completing the project and Lean verification, it had hoped to arrange a parallel release and acknowledged the other researchers’ priority for the forced Euler result.

The public accounts differ on data isolation, priority, and authorship. Deciding between them requires access logs, training-data provenance, communications, version timestamps, and audit material that an independent party can inspect. The dispute therefore reaches beyond the proof itself to the question of whether researchers can preserve, explain, and publish their work under fair conditions.

## Tao’s presentation and the joint declaration widened the setting

On September 7, Terry Tao introduced the Alpöge–Buckmaster work as an exciting development and explained how its three finite-time blow-up results relate to the unforced Navier–Stokes problem. He also noted that the first proof texts were extremely difficult to read and that the authors were rewriting them as a professional paper. Solving a problem, understanding the structure of a proof, and extracting methods that others can reuse do not happen on the same timetable.

On September 11, Tao published the joint statement titled “A Severe Misalignment of AI in Mathematics,” initially signed by 25 Fields Medalists. The statement places conceptual understanding and mathematical insight at the center of what the community values. It describes problem solving as a tool or proxy for reaching those goals. It also criticizes the use of famous open problems as AI benchmarks, warning that competition can push rapid announcements ahead of careful writing, method extraction, citation of prior work, and integration into shared mathematical knowledge.

The statement appeared three days after OpenAI released its paper, so it naturally became part of the same public conversation. Its text addresses a broader pattern of AI practice and does not issue a mathematical ruling on any particular paper. Its central causal question nevertheless meets this event directly: when an answer is presented as a public measure of model ability, can speed and spectacle outrun the time needed for explanation, attribution, and communal understanding? The later analysis therefore has to separate mathematics, transmission, and research process.

## Why the same episode contains three different questions

The week’s materials are easy to conflate because a result, a release, and an ethical dispute appeared almost at once. Bringing them into one conversation is natural; asking one kind of evidence to settle all of them is not. The discussion therefore needs to answer three separate questions:

- Within what scope is the formalized result correct?
- How does a correct result become knowledge that others can understand, cite, and extend?
- Can a valuable result still have been produced or released through an inappropriate process?

The first question calls for the paper, formal proposition, proof term, dependencies, kernel check, and reproduction. The second calls for time, explanation, citation, teaching, and later work. The third calls for evidence about data boundaries, communications, authorship, priority, and independent audit. The three can proceed together, but one cannot substitute for another.

## First question: within what scope is the formal result correct?

Formalization turns the propositions, variables, assumptions, dependencies, and proof written in natural language into objects that a checker can process. If the paper’s claims correspond line by line to the formal proposition, the dependencies are public, the kernel accepts the proof term, and others can reproduce the check, the conclusion has a definite correctness boundary within its stated scope. Whether it reveals a new structure, reads well, or belongs in a textbook requires different evidence.

SAT gives a small but powerful comparison. For a fixed Boolean instance, a solver can provide an assignment when it claims satisfiability, or a certificate that an independent checker can verify when it claims unsatisfiability. Once the certificate passes, an engineering system can use the result within that scope to rule out a design, confirm constraints, or continue a computation. A user can rely on the certificate without understanding every path searched by the solver. The result can be useful before the certificate has been distilled into an elegant theory.

A formalized AI proof follows the same logic at a richer level: it supplies an exact proposition, a proof object, dependencies, and a kernel check. If the natural-language claim corresponds faithfully to the formal proposition, no dependency is hidden, and the check can be reproduced from the published foundations, the result has usable correctness within that scope. It may still take humans a long time to read. Structural explanation, method development, and textbook treatment may come later; their delay does not erase the formal evidence already established.

Correctness and understanding are two contributions that can develop in parallel. A formalized result should not lose all scientific value merely because it has not become a textbook within days. If a result with the same scope and formal status were produced by a human, the community would normally allow months or years for checking and digestion. Requiring an AI-origin result to provide a complete conceptual account within days, and denying recognition otherwise, places the source above the work and creates a double standard. Criticism of an unfaithful formalization, a missing dependency, an unreadable paper, or inaccurate attribution can all be justified; the criticism should identify the concrete defect.

We discuss elsewhere how a formal conclusion with a clear scope might become a callable mathematical component. Here the relevant point is simpler: a result needs a checkable boundary before anyone can discuss stable reuse.
<!-- aside: contextual -->

## Second question: how does knowledge get transmitted?

The joint statement is right to emphasize careful writing, explanation, accurate attribution, teaching, and later research. Those practices are the long-term foundation of a mathematical community. A result enters shared knowledge as it reaches the literature, the classroom, and subsequent work where others can understand and extend it. Authors remain responsible for that path after they release a result.

Knowledge transmission is an independent contribution and the process by which results enter shared knowledge. A reliably checked conclusion can be cited, reproduced, and used within a clearly stated scope while mathematicians continue the work of explaining its proof structure, improving its exposition, and exploring possible generalizations. Mathematics has a function of leaving knowledge that people can inherit, and another function of leaving components with clear boundaries that later work can reuse reliably. The two functions can strengthen each other and can mature at different speeds.

The history of the Poincaré Conjecture gives a concrete timescale. Perelman posted the first of his relevant preprints on November 11, 2002; two further installments appeared in March and July 2003. About eight months passed before the initial set of materials was in place. Verification, exposition, and consolidation by Hamilton, Kleiner, Lott, Tian, and others continued afterward. By 2006, roughly three and a half years after the first preprint, the proof had gradually become an understanding on which the community could publicly rely. The fact that it was not textbook-ready in its first days did not remove the mathematical content it had already introduced.

OpenAI released the paper and formal material on September 8. On September 14, the revision date of this article, only six days had passed. Six days is enough for readers to see a paper and code; it is too short for a community to complete every check, explanation, and extraction of structure. We can ask whether the writing is clear and whether related work is properly handled, and we can expect later papers to make the proof easier to read. An unfinished transmission process cannot serve as evidence that the conclusion has no value.

If a human author submitted the same formal result, we would treat understanding and textbook treatment as work that takes time. AI-assisted work deserves the same timescale. Evaluation can move with the evidence: first whether the proposition holds, then whether the explanation is reliable, and finally how the result enters the wider body of mathematical knowledge.
<!-- aside: poincare -->

## Third question: are mathematical value and research process the same thing?

The mathematical value of a result and the way it was produced and released are different questions. A model company can have commercial goals and still do scientifically useful work; motive does not automatically cancel value. A correct conclusion, in turn, does not grant immunity to problems involving data use, authorship, or priority.

For this event, the questions are concrete. Were unpublished Codex materials accessed or used for training? Were the researchers’ prompts and data isolated from the internal system? Were contributions and authorship represented accurately? After learning that related research existed, was a fair parallel-release arrangement still offered? Who had the power to decide when the work became public? Buckmaster’s document and OpenAI’s update give different accounts. The public record establishes that a dispute exists, but it does not independently settle every fact.

If a company used unpublished research to publish first, or placed researchers at a clear disadvantage over data boundaries or authorship, that would be a failure of research governance even if the final mathematics were correct. If logs, data provenance, timestamps, communications, and independent audit show that the systems remained isolated, researchers would still be entitled to ask how priority and authorship were handled. Mathematical evidence and process evidence answer different questions.

The value of the result and the propriety of the release should therefore be assessed separately. The first requires the paper, formal code, dependencies, and reproduction. The second requires access logs, data provenance, communications, authorship arrangements, and an audit that an independent third party can inspect. Using one set of evidence to replace the other would move the discussion away from the issue at hand.

## From result to shared knowledge: a traceable scientific process
<!-- aside: programme -->

A new machine-assisted result can move through a continuous scientific process. Each stage adds a kind of trust and leaves a record that later readers can inspect:

- Fix the proposition, scope, formal proof, dependencies, axiom status, and reproducible checking procedure.
- Turn the formal object into a paper that researchers can read smoothly, with the background, prior work, examples, and proof route in view.
- Release the paper and code as a public preprint, invite external review, and record questions, revisions, and corrections.
- Keep the paper, formal code, version timestamps, citations, and public discussion in one traceable record.
- Let surveys, classrooms, textbooks, and later research extract the structure so that the result becomes understandable as well as reliably reusable.

The stages can remain open as the work proceeds; they do not have to wait for one final moment. A formal result can first become a checkable and citable record while transmission continues. Exposition and external review can also improve after publication. Each stage has its own evidence, and public writing should say what is complete and what is still underway.

## Let discovery, checking, and transmission keep their own time

This episode separates several judgments that are often folded together: whether a conclusion is correct, whether the community has understood it, and whether the research process respected its participants and public rules. They are related, but each needs its own evidence and its own time.

We will continue to move results along the same chain: fix the proposition and formal boundary, complete a repeatable kernel check, write the proof as a paper that people can read, release a preprint for external review, and preserve revisions, explanations, and later uses in a traceable version record. That keeps the first form of the knowledge while giving it a route into shared understanding and reliable reuse.

Mathematical work can endure in two ways: as knowledge that people can understand, teach, and transmit, and as a component with a clear boundary that later work can call on reliably. Science needs both timescales, and it needs them to meet in one honest record. New technology changes the speed of discovery and checking. The work of a scientific community is to turn that speed into results that can be checked, explained, and handed on.

# ja

## ほとんど一夜で現れた答えから始まった
<!-- aside: opening -->

Navier–Stokes 方程式は、水や空気のような流体の運動を記述します。三次元非圧縮方程式の滑らかな解が滑らかさを保ち続けるかどうかは、七つのミレニアム懸賞問題の一つです。これは偏微分方程式の問題であると同時に、航空機設計、天気予報、血流の研究にも関わります。有限時間特異性とは、滑らかな初期データから始まった解が、有限時間内に速度の発散などによって正則性を失う現象です。粘性は不安定性を抑えようとしますが、非線形相互作用はエネルギーをますます小さな尺度へ集中させます。この緊張関係が問題を難しくしています。

2026 年 9 月の第一週、OpenAI はこの問題を AI の数学能力をめぐる公開競争の中へ持ち込みました。同社の説明によれば、8 月 28 日から訓練中の内部モデルが非常に強い数学能力を示しました。9 月 1 日、二つのミレニアム問題が解かれたかもしれないという報告を聞き、チームは未解決問題やその他の重要な問題でシステムを試し始めました。約 100 のエージェントが約 50 時間並行して作業し、最初の結果は外力のない Euler 方程式に関するものでした。これは粘性を無視した流体モデルであり、チームはその後 Navier–Stokes に資源を移しました。

OpenAI によれば、エージェントは 9 月 5 日、取り組みの開始から約 88 時間で Navier–Stokes の解析的な解答に到達しました。その後、Lean で形式化と検証に累計約 17 時間を使い、9 月 8 日に論文とコードを公開しました。Lean は対話型定理証明器です。形式証明は、命題、依存関係、検査規則を、信頼できるカーネルが再検査できる形で示します。OpenAI は、提示した定式化の範囲でミレニアム問題を解いたと説明し、この発表をモデルの能力と研究速度の公開記録として位置づけました。

この時間軸だけを見れば、ニュースの中心は明快です。長く未解決だった問題について、他者が検査を続けられる新しい結果が現れ、形式化資料も論文と同時に公開されました。論争が始まったのは、同じ週に別の研究の時間軸が公の記録へ入ったからです。

## 同じ週に、別の研究の時間軸が公の記録へ入った

Tristan Buckmaster と Antonin Alpöge は、以前から流体方程式を長く研究していました。Buckmaster の公開文書によれば、二人は 8 月 15 日、滑らかな外力を含む Boussinesq 方程式と Euler 方程式について進展を得ていました。また数か月分の研究上の対話、プロンプト、資料を Codex セッションに保存していました。読者にとって、それらのセッションは研究過程の作業台に近いものです。問いの立て方や試した道筋を記録する役割を担います。

9 月 3 日、大規模言語モデルが重大な未解決問題を解いたかもしれないという報告が広がりました。Buckmaster は OpenAI に連絡し、9 月 6 日の二度の通話で、過去二か月に Codex に残していた未公開研究が内部システムからアクセスされたのか、訓練に使われたのかを尋ねました。公開された文書には、その問いと通話の内容が記録されています。9 月 7 日、二人は非圧縮多孔質媒体方程式、二次元 Boussinesq 方程式、三次元非圧縮 Euler 方程式について三つの有限時間爆発結果と Lean 形式化を公開しました。これらは隣接する方程式を扱う、同じ流体特異性研究の線上の結果です。早い公開によって、二人の成果と時刻も同じ公共記録に入りました。

公開文書には、優先権と著者表示をめぐる争いも記録されています。そこには、Anthropic の職員 Levent Alpöge を共同発表の著者に含めるかどうかという問題もありました。9 月 10 日の更新で OpenAI は、Buckmaster が過去二か月に Codex に残したプロンプトが内部システムや訓練に影響することはあり得ず、相手の成果が公開される前に研究者やエージェントがそれを見ていなかったと説明しました。同社は、プロジェクトと Lean 検証を終えた後、並行公開を望んでいたこと、外力付き Euler の結果について相手の優先権を認めたことも述べました。

データ隔離、優先権、著者表示について、公開された説明は一致していません。判断には、アクセスログ、訓練データの来歴、通信、版の時刻、独立者が調べられる監査資料が必要です。争いの焦点は証明の正しさから、研究者が自分の仕事を公平な条件で保存し、説明し、発表できるかどうかへも広がっています。

## Tao の紹介と共同声明が議論の背景を広げた

9 月 7 日、Terry Tao は Alpöge–Buckmaster の仕事を刺激的な進展として紹介し、三つの有限時間爆発結果と外力のない Navier–Stokes 問題との関係を説明しました。また、最初の証明文は非常に読みにくく、著者たちが専門的な論文へ書き直していることにも触れました。問題を解くこと、証明の構造を理解すること、他者が再利用できる方法を取り出すことは、同じ時間表で進む作業ではありません。

9 月 11 日、Tao は「A Severe Misalignment of AI in Mathematics」という共同声明を公表しました。最初の署名者には 25 名のフィールズ賞受賞者が含まれていました。声明は、概念的理解と数学的洞察を数学共同体が重視する中心に置き、問題を解くことをその目標へ至る道具または代理指標として説明します。また、著名な未解決問題を AI の benchmark にすることを批判し、競争が速い発表を、丁寧な執筆、方法の抽出、先行研究の引用、共同知識への統合より前へ押し出すことを懸念しています。

声明は OpenAI の論文公開から三日後に出され、自然に同じ公開議論の中へ入りました。本文が扱うのはより広い AI と数学の実践であり、特定の論文に対する数学的裁定ではありません。それでも、中心にある因果の問いは今回の出来事に直接触れています。答えがモデル能力の公開指標として示されるとき、速度や注目が、説明、帰属、共同体が理解するために必要な時間を追い越してしまわないか。後の分析では、数学、伝承、研究過程を分けて考える必要があります。

## 同じ出来事に三つの問いがある理由

この一週間の資料は、結果、発表、倫理上の争いがほとんど同時に現れたため、混同されやすくなっています。一つの議論の中で扱うのは自然ですが、一種類の証拠ですべてを決めようとすると焦点を失います。したがって、三つの問いを分けて答える必要があります。

- 形式化された結果は、どの範囲で正しいのか。
- 正しい結果は、他者が理解し、引用し、発展させられる共同知識へどう変わるのか。
- 価値ある結果であっても、作成や公開の過程が不適切であることはあるのか。

第一の問いには、論文、形式命題、証明項、依存関係、カーネル検査、再現が必要です。第二の問いには、時間、説明、引用、教育、後続研究が必要です。第三の問いには、データ境界、通信、著者表示、優先権、独立監査についての証拠が必要です。三つは並行して進められますが、一つが他の代わりになることはありません。

## 第一の問い：形式化された結果はどの範囲で正しいのか

形式化は、自然言語の命題、変数、仮定、依存関係、証明を、検査器が扱える対象へ変換します。論文の主張が形式命題と一つずつ対応し、依存関係が公開され、カーネルが証明項を受け入れ、他者が同じ条件で検査を再現できるなら、その結論は提示された範囲で明確な正しさの境界を持ちます。新しい構造を示すか、読みやすいか、教科書に入るかは別の証拠で判断します。

SAT は小さいながら強い比較を与えます。固定されたブール問題に対し、充足可能だと主張するなら割当を、充足不可能だと主張するなら独立の検査器が確認できる証明書を提示できます。証明書が通れば、工学システムはその範囲で設計を排除し、制約を確認し、次の計算へ進めます。利用者はソルバーが試した経路をすべて理解する必要がなく、証明書も優雅な理論へ整理されるまで役に立たないわけではありません。

形式化された AI の証明も、より豊かな対象について同じ論理をたどります。正確な命題、証明対象、依存関係、カーネル検査を与え、自然言語の主張が形式命題に忠実に対応し、隠れた依存がなく、公開された基礎から検査を再現できるなら、その結果は範囲内で利用可能な正しさを持ちます。人間が読むには長い時間が必要かもしれません。構造の説明、方法の発展、教科書化は後から来る可能性がありますが、その遅れが既に成立した形式的証拠を消すことはありません。

正しさと理解は、並行して育つ二つの貢献です。形式化された結果が数日で教科書にならなかったからといって、科学的価値を失わせるべきではありません。同じ範囲と形式状態の結果を人間が発表したなら、共同体は通常、検査と消化のために数か月、時には数年を認めます。AI が関わったという出所だけを理由に、数日で完全な概念説明まで求め、それがなければ認めないなら、作品より出所を上位に置く二重基準になります。形式化の不忠実さ、依存の欠落、読みにくい論文、不正確な帰属への批判は成立しますが、具体的な欠陥に向けるべきです。

形式化された結論を、境界の明確な呼び出し可能な数学的コンポーネントへ育てる方法については、別の文章で扱っています。ここでの要点は一つです。安定した再利用を考える前に、結果には検査可能な境界が必要です。
<!-- aside: contextual -->

## 第二の問い：知識はどのように伝わるのか

共同声明が丁寧な執筆、説明、正確な帰属、教育、後続研究を重視する点には理由があります。結果が文献、教室、その後の研究へ入り、他者が理解して発展させられると、記録は共同知識へ変わっていきます。発表後も、著者はその道に責任を負います。

知識の伝承は独立した貢献であり、結果が共同知識へ入るための過程です。それを正しい結果を使うための許可証にする必要はありません。信頼できる検査を通った結論は、明確な範囲内で先に引用、再現、利用できます。その間に数学者は証明の構造を説明し、よりよい表現や一般化を探せます。数学には、人が理解し、教え、伝えられる知識として残す機能があります。同時に、境界が明確で、後続研究が信頼して再利用できるコンポーネントとして残す機能もあります。二つは互いを強め、成熟する速さも異なります。

ポアンカレ予想の歴史は、具体的な時間尺度を示します。Perelman の最初の関連プレプリントは 2002 年 11 月 11 日に公開され、続く二つの資料が 2003 年 3 月と 7 月に現れました。最初のプレプリントから初期資料がそろうまで約 8 か月です。その後も Hamilton、Kleiner、Lott、Tian らによる検証、解説、整理が続きました。2006 年には、最初のプレプリントから約 3 年半が経ち、証明は共同体が公に頼れる理解へ徐々に変わっていました。最初の数日で教科書にならなかったことは、その時点で生まれた数学的内容を消しません。

OpenAI が論文と形式化資料を公開したのは 9 月 8 日です。この記事の改訂日である 9 月 14 日まで、まだ 6 日しかありません。6 日あれば論文とコードを読む入口はできますが、すべての検証、説明、構造の抽出を終えるには短すぎます。文章の明瞭さや先行研究の扱いを問い、後続の論文に読みやすい説明を求めることはできます。途中にある伝承を、結論に価値がない証拠へ変えることはできません。

人間の著者が同じ形式化結果を提出したなら、理解と教科書化には時間がかかる後続作業だと考えるでしょう。AI が関わる成果にも同じ時間尺度を適用すべきです。命題が成立するか、説明が信頼できるか、より広い数学知識へどう入るかを、証拠の進みに合わせて評価していけばよいのです。
<!-- aside: poincare -->

## 第三の問い：数学的価値と研究過程は同じなのか

結果の数学的価値と、それがどのように作られ公開されたかは別の問いです。モデル企業が商業的な目的を持っていても、科学的に有用な仕事をすることはあります。動機だけで価値が消えるわけではありません。正しい結論も、データ利用、著者表示、優先権の問題に免責を与えるわけではありません。

今回の出来事では、問いが具体的です。未公開の Codex 資料がアクセスまたは訓練に使われたのか。研究者のプロンプトとデータは内部システムから隔離されていたのか。貢献と著者表示は正確だったのか。関連研究の存在を知った後も、公平な並行公開の選択肢が示されたのか。公開の時期を決める力を誰が持っていたのか。Buckmaster の文書と OpenAI の更新は異なる説明を示します。公開記録は争いの存在を示しますが、すべての事実を独立に確定するものではありません。

未公開研究を使って先に発表したなら、あるいはデータの境界や著者表示で研究者を明らかに不利な立場に置いたなら、最終的な数学が正しくても研究ガバナンスの失敗です。ログ、データの来歴、時刻、通信、独立監査が隔離を示した場合でも、研究者が優先権や著者表示の扱いを問う権利は残ります。数学の証拠と過程の証拠は、異なる問いに答えます。

したがって、結果に価値があるかと、公開が適切だったかは分けて評価する必要があります。前者には論文、形式コード、依存関係、再現が必要です。後者にはアクセスログ、データの来歴、通信、著者表示の取り決め、独立者が検査できる監査が必要です。一方の証拠で他方を置き換えると、議論は本来の問題から離れてしまいます。

## 結果から共同知識へ：追跡可能な科学の過程
<!-- aside: programme -->

新しい機械支援の結果は、連続した科学の過程を進むことができます。各段階が別の信頼性を加え、後の読者が調べられる記録を残します。

- 命題、適用範囲、形式証明、依存関係、公理の状態、再現可能な検査手順を固定する。
- 背景、先行研究、例、証明の道筋を示し、形式対象を研究者が無理なく読める論文へ書き直す。
- 論文とコードを公開プレプリントとして出し、外部審査を受け、質問、修正、訂正を記録する。
- 論文、形式コード、版の時刻、引用、公開議論を一つの追跡可能な記録に保つ。
- サーベイ、授業、教科書、後続研究が構造を取り出し、理解できる結果と信頼して再利用できる結果を育てる。

これらの段階は、仕事の進行に合わせてそれぞれ開いていけます。形式結果は、伝承が続いている間も、検査でき引用できる記録になれます。説明と外部審査も公開後に改善できます。段階ごとに証拠があり、公開文は完了したことと進行中のことを明確に書けばよいのです。

## 発見、検査、伝承にそれぞれの時間を与える

この出来事は、しばしば一つにまとめられる判断を分けて見せました。結論が正しいか、共同体が理解したか、研究過程が参加者と公共の規則を尊重したか。互いに関係していますが、それぞれに固有の証拠と時間があります。

私たちは今後も、命題と形式的な境界を固定し、再現可能なカーネル検査を行い、証明を人が読める論文にし、公開プレプリントと外部審査へ進め、修正、説明、後続利用を追跡可能な版の記録に残します。知識の最初の形を保存しながら、共同体の理解と信頼できる再利用へ進む道を保ちます。

数学の仕事は二つの形で長く残り得ます。人が理解し、教え、伝えられる知識として残ること。そして、境界が明確で、後続の仕事が信頼して呼び出せるコンポーネントとして残ることです。科学には二つの時間尺度が必要であり、それらを一つの誠実な記録で結びつける必要があります。新しい技術は発見と検査の速度を変えます。科学共同体の仕事は、その速度を、検査でき、説明でき、後の人へ渡せる成果へ変えることです。
