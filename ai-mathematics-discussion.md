---
first_published: 2026-09-12
last_revised: 2026-09-14
---

# zh

## 先把这一周发生的事讲清楚
<!-- aside: opening -->

这场讨论始于一个很具体的数学事件。Navier–Stokes 方程描述水和空气等流体的运动。三维不可压缩方程的解能否始终保持光滑，是七个千禧年大奖难题之一；它既关系到纯数学中的偏微分方程，也关系到飞机设计、天气预报和血液流动等应用。所谓“有限时间奇异性”，是指一个从光滑状态开始的解，在有限时间内出现速度无界等失去光滑性的现象。问题的难点在于，黏性通常会抑制这种失控，而方程中的非线性又可能把能量集中到越来越小的尺度。

OpenAI 的公开说明给出了事件的第一条时间线。公司说，8 月 28 日起，内部正在训练的新模型显示出异常强的数学表现；9 月 1 日，团队听到两个千禧年问题可能已经被解决的传闻，于是把模型放到尚未解决的千禧年问题和其他高影响问题上测试。最初，近一百个智能体协同工作约五十小时，得到的是无外力 Euler 方程的结果。Euler 方程可以看作忽略黏性的流体模型。看到这条路线后，团队把资源集中到 Navier–Stokes，并让不同智能体组探索、交换和汇总中间结果。

按 OpenAI 的叙述，智能体在 9 月 5 日得到 Navier–Stokes 的解析解答，距离 9 月 1 日启动约 88 小时；之后又用 17 小时通过 Lean 完成形式化和核验，9 月 8 日公布论文与代码。Lean 是一种交互式定理证明工具。证明被写成内核能够检查的形式，内核可以在相同输入下重复运行。OpenAI 把这项工作描述为在其声明的范围内解决 Navier–Stokes 千禧年问题，同时把这项发布定位为模型能力与研究速度的公开记录，并把 Clay 数学研究所的奖金申请留在另一个程序中。

如果只看这一条时间线，这本来是一件值得庆祝的事：一个长期未解的流体问题出现了新的、可检查的结果，形式化代码也同时公开，任何人都可以继续核查、解释和改进。真正的争议来自同一周里另一条研究时间线的突然出现。

## 研究者的公开时间线为何改变了发布节奏

Tristan Buckmaster 的公开陈述提供了第二条时间线。Buckmaster 和 Antonin Alpöge 先前已经围绕流体方程工作了很长时间。Buckmaster 说，他们在 8 月 15 日取得了关于带光滑外力的 Boussinesq 方程和 Euler 方程的进展；他们还把数月的研究对话、提示和材料保存在 Codex 会话中。这里的 Codex 会话可以理解为一个保存研究过程的工作空间，而不是一个公开论文库。

9 月 3 日，关于某个大型语言模型可能解决重大开放问题的传闻开始流传，Buckmaster 因此联系 OpenAI。9 月 6 日的两次通话中，他询问内部系统是否访问过他和 Alpöge 在此前两个月放入 Codex 的未公开研究，或者是否曾把这些材料用于训练。Buckmaster 的文书记录说，关于是否直接查阅用户数据的回答，并没有清楚回答训练问题。这里的记录仍然留下一个待核实的问题：Buckmaster 公开了通话和当时的疑问，材料使用情况需要更多证据才能判断。

研究者原本希望再花几周时间，把由大型语言模型推动的证明改写成清晰、专业、能够供同行阅读的论文。9 月 7 日，他们提前公开了不可压缩多孔介质方程、二维 Boussinesq 方程和三维不可压缩 Euler 方程的三个有限时间爆破结果，以及相应的 Lean 形式化。这些是带外力或不同方程的结果，与 OpenAI 所公布的 Navier–Stokes 结论不是同一个定理，但它们共享一条流体奇异性研究路线。提前公开的直接作用，是把研究者自己的结果、贡献和时间戳放进公共记录。

Buckmaster 的陈述还记录了一个更尖锐的优先权与署名争议。他说，OpenAI 一方曾提出在联合发布安排中把 Anthropic 的员工 Levent Alpöge 从署名中排除；他还记录了 Sebastien Bubeck 提到“为什么要毁掉自己的职业生涯”之类的对话。这些内容来自一方的公开文书，本文把它们作为待核对的记录来呈现；文书本身没有完成事实裁定。它们之所以重要，是因为优先权、署名和研究者能否自由发表，都是与论文正确性并列的公平制度问题。

9 月 10 日，OpenAI 更新了自己的说明。公司称，Buckmaster 之前两个月的 Codex 提示不可能以任何方式影响内部系统，包括训练；公司也称研究人员和智能体在 Alpöge–Buckmaster 的结果公开以前没有看到这些成果。OpenAI 说，在完成项目和 Lean 核验后，团队曾希望安排并行发布，并承认对方在带外力 Euler 结果上的优先权。于是，公开记录中出现了两组互相竞争的过程叙述：一方记录担忧、通话和发表压力，另一方提供隔离、时间线和调查结论。仅凭声明本身，无法完成独立的事实裁定；但这些材料已经足以说明，数学成果的价值判断和研究过程的治理判断必须分开。

## Tao 的两次发言把同一事件推向了更大的讨论

9 月 7 日，Terry Tao 介绍 Alpöge–Buckmaster 的工作时，称其为一项令人振奋的新进展。他解释说，三项已经完成的结果距离无外力的 Navier–Stokes 问题仍有一步；在他看来，它们已经让继续推进这条路线看起来非常可行。Tao 还指出，这些论证高度使用了 AI，作者正在把最初极难阅读的文字改写成专业说明；他自己也需要通过黑板讨论和现代工具继续消化证明。对 Tao 来说，解出问题是获得数学理解的手段，理解和洞察才是更主要的目标。

9 月 11 日，Tao 发布《A Severe Misalignment of AI in Mathematics》，初始签署者包括 25 位菲尔兹奖得主。他说明，这份文字来自签署者此前一周的讨论；因为他们认为情况紧迫，所以没有等待一个更长的协商过程。声明强调，数学结果需要被讨论、简化、写成可读的论文，放回先行工作和归属的历史中，并通过教学和后续研究进入共同体。它担心的是，当 AI 以越来越快的速度产出“真或假”的答案时，解决题目这一工具可能与数学共同体真正想要的理解、提问和传承脱节。

这两次发言之间有清楚的时间和主题联系，但它们不是同一件事。Tao 9 月 7 日的文章是对 Alpöge–Buckmaster 结果和数学机制的介绍；9 月 11 日的联合声明则把问题扩展到 AI 公司、数学共同体和其他知识行业。声明没有替 OpenAI 这份具体证明作出独立的数学裁决。它提出的是更一般的担忧：一个结果何时只是被算出来，何时真正变成了共同体可以理解、传授和继续使用的知识。

## 为什么要把这场事件拆成三个问题

把时间线讲完后，问题才会清楚。这里至少有三种不同的判断，它们需要三种不同的证据。

第一，结论在它明确声明的范围内是否正确，能否被可靠地复现和使用。这是数学判断，核心材料是命题、假设、形式证明、依赖关系、内核检查和独立复现。

第二，一个正确结果怎样成为共同知识。这里要考察论文是否可读，证明中的结构是否被说明，先行工作的贡献是否被定位，其他人是否能学习、复用和继续发展。这是知识传承的判断。

第三，结果是怎样产生和公布的。未公开材料有没有被访问或用于训练，贡献和署名是否准确，优先权如何处理，发布是否给研究者留下公平的选择空间。这是研究过程与治理的判断。

三者会相互影响，却不能互相代答。形式化通过不能自动解决署名争议；一份漂亮的教材回答的是知识传承问题，命题核验需要另一组证据；研究过程的争议也属于另一层判断，不能改写一个已经被可靠检查的结论。把它们压成“这项成果完整”或“这项成果不完整”的总评，反而会掩盖真正需要回答的问题。

## 第一问：形式化的结论在什么意义上正确

“形式化”把命题、变量、假设、依赖和证明写成一个可信内核能够检查的对象。它改变的是证明的可检查表达，不是论文的排版。如果论文所说的结论与形式对象逐项对应，依赖和公理状态被公开，内核能够重新检查，并且独立的人或团队能够复现，那么这个结论至少在声明的范围内获得了一个明确的正确性边界。它是否包含新的数学结构，是否值得写进教材，是另外的判断。

SAT 提供了一个有用的参照。一个 Boolean 可满足性问题的求解器，可能只留下一个很大的搜索结果或一个由独立检查器验证的证书。使用者不必先理解求解器经历的每一步，才可以采用“这个实例不可满足”这一结论。它可以先进入协议验证、排程或有限组合计算，结构解释则在之后继续发展。SAT 证书可以在进入数学教材以前发挥作用；它经过检查的结论已经有了工程用途。

形式化的 AI 证明遵循同一条逻辑链。若 AI 给出的是一份复杂得多的证明，而这份证明已经被 Lean 这样的内核逐项检查，那么它至少不应因为人类还没有迅速提炼出结构，就被当作一个尚未存在的结果。它可能暂时难读，可能还没有形成漂亮的概念解释，甚至可能需要后续发现其中只是旧方法的组合；这些都影响它的成熟度和可传授性，却不自动否定形式化结论在边界内的可用性。与此同时，形式化也不是魔法：人仍需核对自然语言命题与形式对象是否一致，边界条件是否被正确表达，代码是否真的对应论文声称的结果。

这也是我们反对双重标准的地方。假如一位人类研究者在 9 月 8 日公开了同样范围、同样形式化状态的结果，我们不会仅仅因为到 9 月 14 日还没有教材式解说，就否认它的正确性或一切有限使用价值。把“来自 AI”作为几天内必须完成结构解释和知识传承的额外条件，会让来源替代数学质量成为评判指标。数学工作应当依据命题、证明、适用边界和证据来评价；来源与研究伦理有关，却不应单独改变正确性标准。

这段判断并不替 OpenAI 的论文完成数学审查。它只给出一个公平的原则：先问结论是否被正确表达和检查，再问人类如何理解它、怎样把它变成共同知识。不能因为第二个问题需要几年，就假定第一个问题在今天没有答案；也不能因为第一个问题有答案，就假定第二个问题已经完成。

## 第二问：正确结果如何成为共同知识

联合声明强调知识传承，有充分理由。数学不是把答案放进仓库就结束了。一个结果需要说明它解决了什么，和哪些先行工作相连，哪些步骤是关键，哪些条件限制了它的使用，后来者可以怎样学习和推广。清晰的论文、公开的讨论、同行审评、教学材料、综述和教材，都是把一个局部结果接到共同知识上的不同环节。

但这些环节不必排成一条“先传承、后使用”的单行道。一个已经经过形式化核验的局部结论，可以先以清楚的信任边界被引用、复现或用于后续计算；人类再用更长的时间理解它的结构，修正表述，提取方法，并判断它能否进入教材。作为人类知识留下来，是数学成果的一项功能；作为可以被可靠调用的组件留下来，是另一项功能。两者都重要，完成时间也不必相同。

庞加莱猜想的历史说明，深证明需要时间；证明在早期同样可以拥有价值。Perelman 的第一篇相关预印本发布于 2002 年 11 月 11 日，随后两篇材料分别在 2003 年 3 月和 7 月出现；从第一篇预印本到材料基本齐备约八个月。之后，Hamilton、Kleiner、Lott、Tian 等人的解说、核查和整理持续推进。到 2006 年，围绕这项百年问题的证明已经经过约三年半的讨论和说明，才逐步形成了共同体可以依靠的公开理解。这里没有一个简单的“某一天人类突然完成理解”的开关，只有从证明、核查、解释到教学的连续过程。

OpenAI 在 9 月 8 日公开材料，到本文 9 月 14 日修订时只有六天。六天内没有成熟的公共解说，只能说明阅读和转化刚刚开始。人类深证明通常获得数月甚至数年的核查时间，却对 AI 结果提出几天内必须完成概念传承的额外条件，这不是对数学内容本身的对称评价。

更合适的路径，是把不同阶段同时保存下来：初始的形式化结果，面向人的可读论文，公开预印本和外部审评，随着审评产生的修订和更正，以及最终进入综述、教材和后续研究的结构解释。机器可以缩短发现和形式化；理解、归属、选择和传授仍由人类共同体完成。传承承担的是延长正确结果生命的工作，而非充当承认正确性的前置许可。

## 第三问：结果有价值，与产生过程是否恰当

一个结果的数学价值与研究过程的伦理问题属于两组证据。模型公司即使带有商业目标，也可能真的做出了科学上有用的工作；动机不会自动抹去结论的价值。数学正确性之外，仍要单独审视产生和发布过程是否恰当。

这次事件中的过程问题很具体：未公开的 Codex 材料是否被访问或用于训练，研究者的提示和数据是否与内部系统隔离，贡献和署名是否准确，OpenAI 是否在知道相关研究存在后仍有公平的并行发布安排，谁拥有决定公开时间的权力。Buckmaster 的文书与 OpenAI 的更新给出了不同的叙述。当前公开材料能够确定这些争议存在，却还不足以独立裁定哪一方的每一个主张为真。

如果一家公司为了抢先发布而使用了未公开研究，或者让研究者在数据边界和署名上处于明显弱势，那是研究治理的失败，即使最终的数学结论仍然正确。反过来，如果日志、训练数据来历、时间戳、通信记录和独立审计显示模型确实保持了隔离，也不能因此要求研究者放弃对优先权和署名的正常关切。数学价值和过程适当性必须分别取证。

这也是为什么“OpenAI 的结果有没有价值”和“OpenAI 在这次发布中是否做得恰当”不能合并成一句话。前一个问题需要论文、形式代码、依赖和复现；后一个问题需要访问日志、数据来历、通信记录、署名安排和可供独立第三方核验的审计。任何一项证据都不应替代另一项证据。

## 三个问题怎样进入同一条科学流程

一个新的机器辅助结果，可以沿着一条连续但分阶段的科学流程前进：

- 先固定命题、适用范围、形式证明、依赖关系、公理状态和可复现的检查方式。
- 再把形式对象解释成普通研究者能够阅读的论文，说明它和先行工作、相关方程以及已有方法的关系。
- 公开预印本，接受外部审评，记录谁提出了什么问题，并据此修订证明和文字。
- 把论文、形式代码、公开记录和更正保持在同一条可追溯记录上。
- 最后让结果进入综述、课堂、教材和后续研究，使它既能被理解，也能被可靠复用。

这条流程不是把三个问题排成一道门。数学正确性、知识成熟度和研究过程的可信度可以在不同时间达到不同状态。重要的是每一个状态都要有自己的证据，公开时也要把尚未完成的部分说清楚。

## 我们接下来会怎样处理这类结果

面对这类事件，最有用的回应，是先把证据链保留下来，再形成总评。我们会先把结论的范围、形式化状态和可复现条件写清楚，再把证明转成人类能够认真阅读的论文，提交公开预印本和外部审评。审评产生的修订、错误和补充会保留在版本记录中；涉及合作、数据和优先权的部分，则通过可以由独立第三方核查的记录来处理。

科学知识需要被传承，也需要在传承完成以前保持可检查、可引用和可复用。新的技术会改变发现、验证和传播的速度，科学共同体要做的工作，是让这些速度进入一条能够尊重事实、尊重研究者、也能把结果交给后来者的道路。

# en

## First, what happened during that week
<!-- aside: opening -->

This discussion began with a specific mathematical event. The Navier–Stokes equations describe the motion of fluids such as water and air. Whether smooth solutions of the three-dimensional incompressible equations can remain smooth is one of the seven Millennium Prize Problems. The question belongs to pure mathematics, but it also touches aircraft design, weather forecasting, and the study of blood flow. A finite-time singularity means that a solution which starts smoothly develops an unbounded speed or another loss of regularity in finite time. Viscosity tends to smooth motion, while the nonlinear terms can concentrate energy at smaller and smaller scales.

OpenAI’s public account gives the first timeline. The company says that an internal model being trained since August 28 had shown an unusual level of mathematical performance. On September 1, the team heard rumors that two Millennium problems might have been solved, and began testing the model on the remaining Millennium problems and several other high-impact questions. Nearly one hundred agents worked together for roughly fifty hours and first produced a result for the unforced Euler equations. Euler can be viewed as a fluid model without viscosity. After seeing that route, the team shifted its resources to Navier–Stokes and had different groups explore, exchange, and consolidate intermediate results.

According to OpenAI, the agents reached their Navier–Stokes resolution on September 5, about 88 hours after the effort began. Lean formalization and verification took another 17 hours, and the paper and code were released on September 8. Lean is an interactive theorem prover: a proof is represented in a form that a comparatively small kernel can check and recheck. OpenAI described the result as resolving the Navier–Stokes Millennium Prize problem within the stated formulation. It framed the release as a public record of model capability and research speed, leaving any Clay Prize claim to a separate process.

Seen on its own, that timeline would be a reason to celebrate. A long-standing fluid problem had received a new, checkable result, and the formal code was released at the same time. Others could inspect it, explain it, and improve it. The controversy began because another research timeline entered the public record during the same week.

## Why the researchers changed their publication timetable

Tristan Buckmaster’s public statement supplies the second timeline. Buckmaster and Antonin Alpöge had already been working on fluid equations for some time. Buckmaster wrote that they made substantial progress on August 15 on finite-time blowup for the Boussinesq and Euler equations with smooth forcing. They had also kept months of research conversations, prompts, and materials in Codex sessions. In this context, a Codex session is a workspace that preserves part of a research process; it is not a public paper archive.

On September 3, rumors circulated that a large language model might have solved a major open problem, and Buckmaster contacted OpenAI. During two calls on September 6, he asked whether an internal system had accessed unpublished work that he and Alpöge had placed in Codex during the preceding two months, or whether those materials had been used for training. Buckmaster’s document says that an answer about direct access to user data did not clearly answer the training question. The record leaves a material question open: Buckmaster published his account of the calls and his concerns, while the use of the material requires further evidence.

The researchers had planned to spend several more weeks turning the large-language-model-assisted arguments into clear, professional papers. On September 7 they released three finite-time blowup results, for the incompressible porous-medium equation, the two-dimensional Boussinesq equation, and the three-dimensional incompressible Euler equation, together with Lean formalizations. These are different theorems from OpenAI’s Navier–Stokes result, although they belong to a connected programme on fluid singularities. The immediate purpose of the early release was to place the researchers’ own work, contributions, and timestamps in the public record.

Buckmaster’s statement also records a sharper dispute about priority and authorship. He says that an OpenAI representative proposed excluding Levent Alpöge, an Anthropic employee, from the authorship of a joint release, and he records a remark along the lines of “Why would you ruin your career?” These details come from one side’s public document, so this article presents them as records requiring verification; the document itself does not adjudicate them. They matter because priority, authorship, and a researcher’s freedom to publish are institutional questions of fairness alongside mathematical correctness.

On September 10, OpenAI updated its account. The company said that Buckmaster’s Codex prompts from the preceding two months could not have influenced its internal system in any way, including through training, and that its researchers and agents had not seen the Alpöge–Buckmaster work before it was made public. OpenAI said that, after completing the project and Lean verification, it had sought a concurrent release and recognition of the other team’s priority on the forced Euler result. The public record therefore contains two competing accounts of the process: one records concerns about calls, access, and publication pressure; the other presents an isolation and investigation account. The statements alone cannot settle every fact. They do show why mathematical value and research governance must be judged separately.

## Tao’s two interventions widened the discussion

On September 7, Terry Tao described the Alpöge–Buckmaster work as exciting. He explained that the three results still fell short of the unforced Navier–Stokes problem; in his view, they made further progress along that route look highly feasible. He also noted that the arguments were heavily AI-assisted and that the authors were rewriting extremely difficult initial drafts into professional explanations. Tao himself said that he needed more time, discussion, and modern tools to digest the proof. For him, solving a problem is a means toward mathematical understanding; understanding and insight are the deeper goals.

On September 11, Tao published “A Severe Misalignment of AI in Mathematics,” initially signed by 25 Fields medalists. He wrote that the text grew out of discussions among the signatories during the previous week, and that they released it quickly because they considered the situation urgent. The declaration emphasizes discussion, simplification, readable writing, priority and attribution, teaching, and the movement of ideas into the mathematical community. Its concern is that when AI produces true-or-false answers at increasing speed, problem solving can become detached from the understanding, questioning, and transmission that the community wants mathematics to cultivate.

The two interventions have a clear temporal and thematic connection, but they are not the same intervention. Tao’s September 7 post introduced the Alpöge–Buckmaster results and their mathematical mechanism. The September 11 declaration widened the subject to AI companies, the mathematical community, and other knowledge professions. It did not independently adjudicate the mathematics of OpenAI’s paper. It raised a broader question: when is a result merely computed, and when has it become knowledge that a community can understand, teach, and develop?

## Why the event contains three different questions

Once the timeline is clear, the structure of the discussion becomes visible. At least three judgments are involved, and each requires different evidence.

The first is whether a conclusion is correct within the scope it states, and whether it can be reliably reproduced and used. This is a mathematical judgment. Its materials are the proposition, hypotheses, formal proof, dependencies, kernel check, and independent reproduction.

The second is how a correct result becomes shared knowledge. This asks whether the paper can be read, whether the proof’s structure has been explained, whether prior work and credit have been located, and whether others can learn, reuse, and extend the result. This is a knowledge-transmission judgment.

The third is how the result was produced and released. Were unpublished materials accessed or used for training? Were contributions and authorship recorded accurately? Were priority and publication choices handled fairly? This is a research-process and governance judgment.

The three questions interact, but they cannot answer one another. A formal proof answers a mathematical question, while an authorship dispute requires institutional evidence. A beautiful exposition answers a knowledge-transmission question, while proposition verification requires its own evidence. A process problem belongs to a third layer and leaves a reliably checked conclusion mathematically intact. Reducing everything to one verdict about whether a result is “complete” hides the evidence each question actually requires.

## First question: in what sense is a formalized conclusion correct?

Formalization is not a prettier typesetting of a paper. It expresses the proposition, variables, hypotheses, dependencies, and proof as an object checked by a trusted kernel. If the natural-language claim corresponds to the formal object, if dependencies and axioms are disclosed, if the kernel can recheck the proof, and if an independent person or team can reproduce the check, the conclusion has a definite correctness boundary within its stated scope. Whether it contains a new mathematical structure or deserves a textbook treatment is a separate judgment.

SAT offers a useful reference point. A Boolean satisfiability solver may leave only a large search result or a certificate checked by an independent checker. Users do not have to understand every step of the search before they can use the conclusion that a particular instance is unsatisfiable. The result can enter protocol verification, scheduling, or finite combinatorial computation first; structural explanations can develop later. A SAT certificate can be useful before it becomes a mathematical textbook. Its checked conclusion already has an engineering use.

A formalized AI proof follows the same basic logic. If an AI produces a much more complicated proof and a Lean kernel checks it line by line, the result should not be treated as nonexistent merely because people have not quickly extracted its structure. It may be difficult to read, it may lack a polished conceptual explanation, and later work may show that it combines familiar methods. Those facts affect maturity and teachability. They do not automatically erase the limited usability of a checked conclusion within its boundary. Formalization is not magic: people must still check that the natural-language proposition matches the formal object, that boundary conditions were expressed correctly, and that the code proves what the paper claims.

This is where we see a double standard. If a human researcher released the same proposition with the same formal status on September 8, we would not deny its correctness or every limited use merely because no textbook-style explanation existed by September 14. Requiring an AI-originated result to acquire conceptual explanation and knowledge transmission within a few days, solely because of its origin, makes provenance a substitute for mathematical evaluation. The work should be judged by its proposition, proof, scope, and evidence. Origin matters for research ethics; it should not by itself change the standard for correctness.

This point is not an independent mathematical verdict on OpenAI’s paper. It is a fairness principle. Ask first whether the conclusion has been correctly stated and checked; then ask how people will understand it and turn it into shared knowledge. The second question may take years without making the first question empty. The first may have an answer without making the second complete.

## Second question: how does a correct result become shared knowledge?

The declaration is right to emphasize transmission. Mathematics does not end when an answer is placed in a repository. A result needs to say what it solves, how it connects to earlier work, which steps carry the argument, what limits its use, and how later readers can learn and extend it. Clear papers, public discussion, external review, teaching materials, surveys, and textbooks are different links in that chain.

Those links do not have to form a one-way gate in which transmission must be finished before use is permitted. A formally checked local conclusion can be cited, reproduced, or used in a bounded calculation while people spend more time understanding its structure, correcting its language, extracting methods, and deciding whether it belongs in a textbook. Leaving a result in human knowledge is one function of mathematics. Leaving it as a reliably callable component is another. Both functions matter, and they do not have to finish at the same time.

The history of the Poincaré conjecture shows why deep proofs have their own timescale. Perelman’s first related preprint appeared on November 11, 2002. Two further papers followed in March and July 2003, so the initial set of materials took about eight months to assemble. Expositions, checking, and reorganizing continued through the work of Hamilton, Kleiner, Lott, Tian, and others. By 2006, roughly three and a half years after the first preprint, the proof had accumulated the explanations and checks that allowed the community to rely on it publicly. There was no single switch from “not knowledge” to “knowledge”; there was a long chain from proof, to checking, to exposition, to teaching.

OpenAI’s material appeared on September 8. By this article’s revision on September 14, only six days had passed. The absence of a mature public exposition after six days means that the work of reading and translating had just begun. Human proofs of great depth are given months or years for checking, yet an AI result is sometimes asked to complete conceptual transmission within days. That is not a symmetric evaluation of the mathematics.

A better path preserves the stages together: the initial formal result, a paper people can read, a public preprint and external review, revisions and corrections, and eventually structural explanations in surveys, classrooms, and later research. Machines can shorten discovery and formalization. Understanding, attribution, selection, and teaching still require a human community. Transmission is not prior permission for correctness; it is the work that gives a correct result a longer life.

## Third question: can a valuable result still come from an inappropriate process?

The mathematical value of a result cannot answer the ethical questions about how it was produced. A model company may have commercial motives and still produce genuinely useful science; motive does not automatically erase value. Mathematical correctness leaves a separate question about whether the process of producing and releasing the result was appropriate.

The process questions here are concrete. Were unpublished Codex materials accessed or used for training? Were the researchers’ prompts and data isolated from the internal system? Were contributions and authorship recorded accurately? After learning that related research existed, did OpenAI still offer a fair concurrent-release arrangement? Who had the power to decide when the result would be public? Buckmaster’s document and OpenAI’s update provide different accounts. The public record establishes that the dispute exists, but does not independently settle every claim.

If a company used unpublished research to gain priority, or left researchers in a clearly weaker position over data boundaries and authorship, that would be a failure of research governance even if the final mathematical result were correct. If logs, training-data provenance, timestamps, communications, and independent audits show that the systems were properly isolated, researchers would still be entitled to ask ordinary questions about priority and credit. Mathematical value and procedural appropriateness require different evidence.

That is why “does the OpenAI result have value?” and “was the release handled appropriately?” cannot be answered in one sentence. The first calls for the paper, formal code, dependencies, and reproduction. The second calls for access logs, data provenance, communications, authorship arrangements, and an audit that an independent party can inspect. Neither set of evidence can replace the other.

## How the three questions enter one scientific process

A new machine-assisted result can move through a continuous process with distinct stages:

- Fix the proposition, scope, formal proof, dependencies, axiom status, and reproducible checking procedure.
- Explain the formal object in a paper that researchers can read, including its relation to prior work, the relevant equations, and existing methods.
- Release a public preprint, invite external review, record the questions raised, and revise both proof and exposition.
- Keep the paper, formal code, public record, and corrections together.
- Let the result enter surveys, classrooms, textbooks, and later research so that it becomes understandable as well as reliably reusable.

This process is not a single gate that forces the three questions into one order. Mathematical correctness, knowledge maturity, and procedural trust can reach different states at different times. Each state needs its own evidence, and public writing should say clearly what is complete and what remains open.

## What we will do with results of this kind

The most useful response to an event like this is to separate the evidence before forming a total verdict. We will state the scope, formal status, and reproducibility conditions of a result; turn the proof into a paper people can read; submit it as a public preprint and to external review; and preserve revisions, errors, and additions in the version record. Questions about collaboration, data, and priority will be handled through records that an independent party can examine.

Scientific knowledge needs transmission, and it also needs to remain checkable, citable, and reusable before transmission is complete. New technology changes the speed of discovery, verification, and publication. The work of a scientific community is to place that speed on a path that respects facts and researchers while handing durable results to the people who come next.

# ja

## まず、その一週間に起きたこと
<!-- aside: opening -->

この議論は、具体的な数学上の出来事から始まりました。Navier–Stokes 方程式は、水や空気のような流体の運動を記述します。三次元非圧縮方程式の滑らかな解が滑らかさを保ち続けるかどうかは、七つのミレニアム懸賞問題の一つです。これは純粋数学の問題ですが、航空機設計、天気予報、血流の研究にも関わります。有限時間特異性とは、滑らかに始まった解が有限時間内に速度の発散などを起こし、滑らかさを失う現象です。粘性は運動を滑らかにする一方、非線形項はエネルギーをますます小さな尺度へ集中させる可能性があります。

OpenAI の公開説明が第一の時間軸を示します。同社によれば、8月28日から訓練中だった内部モデルが非常に高い数学能力を示し、9月1日に二つのミレニアム問題が解かれたかもしれないという噂を聞いたため、未解決のミレニアム問題と他の重要問題でモデルを試し始めました。約100のエージェントが約50時間協調し、最初に外力のない Euler 方程式の結果を得ました。Euler 方程式は、粘性を無視した流体モデルと考えることができます。その経路を見た後、チームは Navier–Stokes に資源を移し、複数のグループに中間結果を探索・交換・統合させました。

OpenAI の説明では、エージェントは9月5日に Navier–Stokes の解答に到達し、取り組みの開始から約88時間でした。その後、Lean による形式化と検証に17時間をかけ、9月8日に論文とコードを公開しました。Lean は対話型定理証明器です。証明は比較的小さなカーネルが検査・再検査できる形で表されます。OpenAI は、提示した定式化の範囲で Navier–Stokes のミレニアム問題を解決したと説明し、Clay 数学研究所の賞を請求するのではなく、モデルの能力と研究速度の記録を公開するのだと述べました。

この時間軸だけを見れば、祝うべき出来事です。長く未解決だった流体問題に検査可能な結果が現れ、形式コードも同時に公開されました。誰もがそれを調べ、説明し、改善できます。論争が始まったのは、同じ週に別の研究の時間軸が公の記録へ入ったからです。

## 研究者が公開の予定を変えた理由

Tristan Buckmaster の公開文書が第二の時間軸を示します。Buckmaster と Antonin Alpöge は、すでに流体方程式を長く研究していました。Buckmaster は、8月15日に滑らかな外力をもつ Boussinesq 方程式と Euler 方程式の有限時間爆発について大きく前進したと記しています。二人は数か月の研究会話、プロンプト、資料を Codex のセッションに保存していました。ここでいう Codex セッションは研究過程の一部を保存する作業空間であり、公開論文の保管庫ではありません。

9月3日、大型言語モデルが大きな未解決問題を解いたかもしれないという噂が広がり、Buckmaster は OpenAI に連絡しました。9月6日の二度の通話で、二人がその前の二か月に Codex へ置いた未公開研究が内部システムにアクセスされたか、訓練に使われたかを尋ねました。Buckmaster の文書によれば、ユーザーデータを直接見たかどうかへの回答は、訓練について明確ではありませんでした。ここでは記録の範囲を守る必要があります。これは Buckmaster による通話と懸念の公開説明であり、それだけで OpenAI が資料を使ったことを証明するものではありません。

研究者は、本来ならさらに数週間かけて、大型言語モデルの支援を受けた議論を明快で専門的な論文に直す予定でした。9月7日、二人は非圧縮多孔質媒体方程式、二次元 Boussinesq 方程式、三次元非圧縮 Euler 方程式について、三つの有限時間爆発の結果と Lean 形式化を公開しました。これは OpenAI の Navier–Stokes の結果とは別の定理ですが、流体の特異性を研究する一つのつながった計画に属します。早期公開の直接の目的は、自分たちの成果、貢献、タイムスタンプを公の記録に置くことでした。

Buckmaster の文書には、優先権と著者表示をめぐるさらに鋭い争いも記録されています。彼によれば、OpenAI 側から、Anthropic の社員である Levent Alpöge を共同発表の著者から外す案が出され、「なぜ自分のキャリアを壊すのか」という趣旨の発言もあったとされます。これらは一方の公開文書に基づく内容です。この記事では、検証を要する記録として扱います。優先権、著者表示、研究者が自由に発表できることは、数学的正しさと並ぶ公平な研究制度の問題です。

9月10日、OpenAI は説明を更新しました。同社は、Buckmaster の過去二か月の Codex プロンプトが訓練を含むいかなる形でも内部システムに影響し得ず、研究者とエージェントも Alpöge–Buckmaster の成果が公開されるまで見ていなかったと述べました。また、プロジェクトと Lean 検証が完了した後、強制外力を含む Euler の結果について相手の優先権を認め、同時公開を提案したと説明しました。公の記録には、通話、アクセス、発表圧力への懸念を記す説明と、隔離と調査の結果を示す説明があります。声明だけではすべての事実を確定できません。しかし、数学的価値と研究ガバナンスを分けて判断しなければならない理由は明確です。

## Tao の二つの発言が議論を広げた

9月7日、Terry Tao は Alpöge–Buckmaster の仕事を 非常に刺激的な新展開と紹介しました。三つの結果は外力のない Navier–Stokes へ向かう途中の成果です。Tao は、この経路をさらに進めることが現実的になったと説明しました。また、議論は AI の支援を強く受けており、著者たちは非常に読みにくい最初の草稿を専門的な説明へ書き直していると述べました。Tao 自身も、黒板での議論や現代のツールを使って、さらに時間をかけて理解する必要があるとしています。Tao にとって、問題を解くことは数学的理解へ進む手段であり、理解と洞察がより深い目標です。

9月11日、Tao は “A Severe Misalignment of AI in Mathematics” を公表し、最初の署名者は25人のフィールズ賞受賞者でした。署名者の前週の議論から生まれ、状況が緊急だと考えたため、長い協議を待たずに公開したと説明しています。声明は、議論、簡約、読みやすい執筆、先行研究と帰属、教育、そしてアイデアを数学共同体へ送り込むことを重視します。AI が真偽の答えを急速に生産するとき、問題を解く道具が、共同体が数学に求めてきた理解、問い、伝承から切り離される危険を指摘しています。

二つの発言には時間的・主題的なつながりがありますが、同じ発言ではありません。9月7日の記事は Alpöge–Buckmaster の結果と数学的機構を紹介し、9月11日の声明は AI 企業、数学共同体、他の知識分野へ論点を広げました。声明は OpenAI の論文の数学を独立に裁定したものではありません。結果が単に計算された段階から、共同体が理解し、教え、発展させられる知識になるまでの距離を問いかけています。

## なぜこの出来事を三つの問いに分けるのか

時間軸をたどると、議論の構造が見えてきます。少なくとも三つの判断があり、それぞれ異なる証拠を必要とします。

第一は、結論が明示した範囲で正しいか、信頼して再現・使用できるかです。命題、仮定、形式証明、依存関係、カーネル検査、独立再現が中心になります。

第二は、正しい結果がどのように共有知になるかです。論文を読めるか、証明の構造が説明されているか、先行研究と貢献が位置づけられているか、他者が学び、再利用し、拡張できるかを問います。

第三は、結果がどのように生まれ、公開されたかです。未公開資料がアクセスまたは訓練に使われたか、貢献と著者表示が正確か、優先権と公開の選択が公平だったかを調べます。

三つは関係しますが、互いの代わりにはなりません。形式証明は著者表示の争いを解決せず、きれいな解説は命題の検証を置き換えません。過程の問題も、検査済みの結論を数学的誤りにはしません。「完全な成果か」という一つの評点に押し込めると、それぞれの証拠が見えなくなります。

## 第一の問い：形式化された結論はどの意味で正しいのか

形式化は論文の組版を整えることではありません。命題、変数、仮定、依存関係、証明を、信頼できるカーネルが検査できる対象として表します。自然言語の主張と形式対象が対応し、依存関係と公理が開示され、カーネルが再検査でき、独立した人やチームが再現できるなら、その結論は明示された範囲で明確な正しさの境界を持ちます。新しい数学的構造を含むか、教科書に載るべきかは別の判断です。

SAT は有用な参照になります。Boolean 充足可能性のソルバーは、大きな探索結果や、独立チェッカーが検証する証明書だけを残すことがあります。利用者は探索の全過程を理解しなくても、特定のインスタンスが充足不能だという結論を使えます。その結果は、プロトコル検証、スケジューリング、有限組合せ計算に先に入ることができ、構造の説明は後から発展します。SAT の証明書は数学の教科書ではありませんが、検査済みの結論はすでに工学的な用途を持ちます。

形式化された AI の証明も基本的には同じ論理に従います。AI がはるかに複雑な証明を出し、Lean のカーネルが一行ずつ検査したなら、人間がすぐに構造を抽出できないという理由だけで、結果を存在しないものとして扱うべきではありません。読みにくさ、概念説明の不足、後から見れば既存手法の組合せにすぎない可能性は、成熟度と教えやすさに影響します。しかし、境界内で検査された結論の限定的な利用価値を自動的に消しません。形式化も万能ではなく、自然言語の命題と形式対象の一致、境界条件の表現、コードと論文の対応を人が確認する必要があります。

ここで私たちが二重基準を問題にします。もし同じ命題と同じ形式化の状態を持つ結果を人間の研究者が9月8日に公開していたなら、9月14日までに教科書的な説明がないことだけで、正しさや限定的な利用価値を否定することはないでしょう。AI から出たという理由だけで、数日以内に概念説明と知識継承まで終えるよう求めるなら、出所が数学的評価の代わりになっています。評価は命題、証明、範囲、証拠に向けるべきです。出所は研究倫理に関係しますが、それだけで正しさの基準を変えるべきではありません。

これは OpenAI の論文についての独立した数学判定ではありません。公平な評価の原則です。まず結論が正しく述べられ、検査されているかを問う。そのうえで、人間がそれを理解し、共有知へ変える方法を問う。第二の仕事に数年かかっても、第一の問いが空になるわけではありません。第一に答えがあっても、第二が完了したことにはなりません。

## 第二の問い：正しい結果はどのように共有知になるのか

声明が知識の伝承を重視するのには理由があります。答えをリポジトリに置けば数学が終わるわけではありません。何を解いたのか、どの先行研究とつながるのか、どの手順が核心なのか、利用の限界は何か、後の読者がどう学び拡張できるのかを示す必要があります。明快な論文、公開討論、外部審査、教育資料、サーベイ、教科書は、その鎖の異なる部分です。

これらは「先に伝承を終えなければ使えない」という一方向の門である必要はありません。形式化された局所的な結論は、境界を明示したうえで引用、再現、計算に使えます。その間に人間は構造を理解し、表現を直し、方法を抽出し、教科書に入るか判断できます。結果を人間の知識として残すことは数学の一つの機能です。信頼できる呼び出し可能な部品として残すことは別の機能です。両方が重要で、完了時期は同じでなくてよいのです。

ポアンカレ予想の歴史は、深い証明に固有の時間尺度があることを示します。Perelman の最初の関連プレプリントは2002年11月11日に公開され、その後の二本が2003年3月と7月に現れました。最初のプレプリントから初期資料がそろうまで約8か月です。その後も Hamilton、Kleiner、Lott、Tian らによる解説、検証、整理が続きました。2006年には、最初のプレプリントから約3年半を経て、百年越しの問題の証明が共同体から公に頼れる形へ近づきました。証明が一日で教科書的な知識へ変わることはなく、証明、検証、解説、教育の長い鎖が形成されました。

OpenAI の資料が公開されたのは9月8日です。この記事の改訂日である9月14日まで、わずか6日しかありません。6日後に成熟した公開解説がないことは、読解と転換が始まったばかりだという意味です。人間の深い証明には数か月や数年の検証時間を与えながら、AI の結果だけに数日で概念継承を終えるよう求めるのは、数学の対称的な評価ではありません。

段階を一緒に保存する道筋が、ここでは有用です。初期の形式結果、人間が読める論文、公開プレプリントと外部審査、改訂と訂正、そしてサーベイ、授業、後続研究での構造説明です。機械は発見と形式化を短縮できます。理解、帰属、選択、教育には人間共同体の仕事が残ります。伝承は正しさを認めた後も続く仕事であり、正しい結果に長い生命を与えます。

## 第三の問い：価値ある結果でも、過程は不適切になり得るのか

結果の数学的価値は、それがどのように作られたかという倫理問題に答えません。モデル企業が商業的な目的を持っていても、科学的に有用な仕事をすることはあります。動機だけで価値が消えるわけではありません。反対に、数学的に正しい結果であっても、作成と公開の過程が適切だったとは限りません。

この事件の問いは具体的です。未公開の Codex 資料がアクセスまたは訓練に使われたのか。研究者のプロンプトとデータは内部システムから隔離されていたのか。貢献と著者表示は正確だったのか。関連研究の存在を知った後も、OpenAI は公平な同時公開の選択肢を示したのか。公開時期を決める力を誰が持っていたのか。Buckmaster の文書と OpenAI の更新は異なる説明を示します。公開記録は争いの存在を示しますが、すべての主張を独立に確定するものではありません。

会社が優先権を得るために未公開研究を使ったなら、あるいはデータの境界と著者表示で研究者を明らかに弱い立場へ置いたなら、最終的な数学が正しくても研究ガバナンスの失敗です。ログ、訓練データの来歴、タイムスタンプ、通信、独立監査が適切な隔離を示したとしても、研究者が優先権と貢献について通常の質問をする権利は残ります。数学的価値と過程の適切さには別の証拠が必要です。

だから「OpenAI の結果に価値があるか」と「今回の公開は適切だったか」は一文で答えられません。前者には論文、形式コード、依存関係、再現が必要です。後者にはアクセスログ、データの来歴、通信、著者表示の取り決め、独立者が検査できる監査が必要です。一方の証拠が他方を置き換えることはできません。

## 三つの問いを一つの科学的過程に置く

新しい機械支援の結果は、別々の段階を持つ一つの過程を進むことができます。

- 命題、範囲、形式証明、依存関係、公理の状態、再現可能な検査手順を固定する。
- 形式対象を、先行研究、関係する方程式、既存手法との関係まで含めて、研究者が読める論文に説明する。
- 公開プレプリントとして出し、外部審査を受け、提起された問いを記録し、証明と説明を改訂する。
- 論文、形式コード、公開記録、訂正を一つの追跡可能な鎖に保つ。
- サーベイ、授業、教科書、後続研究へつなぎ、理解できる結果と信頼して再利用できる結果を同時に育てる。

これは三つの問いを一つの順番に押し込める門ではありません。数学的正しさ、知識の成熟、過程への信頼は、異なる時点で異なる状態に到達します。各状態に固有の証拠を用意し、公開文では完了したことと残っていることを明確に書く必要があります。

## 私たちはこのような結果をどう扱うか

このような出来事への最も有用な応答は、証拠を分ける前に全体評価を下すことではありません。結果の範囲、形式化の状態、再現条件を記し、人間が読める論文に直し、公開プレプリントと外部審査へ進めます。審査による改訂、誤り、追加を版の記録に残します。協力、データ、優先権の問題は、独立者が調べられる記録を通じて扱います。

科学知識には伝承が必要です。同時に、伝承が終わる前から検査でき、引用でき、再利用できる状態も必要です。新しい技術は発見、検証、公開の速度を変えます。科学共同体の仕事は、その速度を、事実と研究者を尊重しながら、次の人へ耐久性のある結果を渡す道へ置くことです。
