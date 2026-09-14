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

9 月 7 日，Terry Tao 介绍 Alpöge–Buckmaster 的工作时，称其为一项令人振奋的新进展。他解释说，三项已经完成的结果距离无外力的 Navier–Stokes 问题仍有一步；在他看来，它们已经让继续推进这条路线看起来非常可行。Tao 还指出，这些论证高度使用了 AI，作者正在把最初极难阅读的文字改写成专业说明；他自己也需要通过黑板讨论和现代工具继续消化证明。对 Tao 来说，解出问题是获得数学理解的手段，理解和洞见才是更主要的目标。

9 月 11 日，Tao 发布《A Severe Misalignment of AI in Mathematics》，初始签署者包括 25 位菲尔兹奖得主。他说明，这份文字来自签署者此前一周的讨论；因为他们认为情况紧迫，所以没有等待一个更长的协商过程。原文提出了一套明确的价值排序：解题只是通往数学共同体“首要目标”的工具和代理，那个目标是概念理解与洞见。声明批评 AI 公司把著名公开问题作为模型 benchmark 的竞赛，担心快速宣布“真或假”的答案会挤压认真写作、提炼新方法、引用先行工作，以及由数学家把结果纳入共同知识的时间。

这两次发言在时间和主题上紧密相连，却承担不同作用。9 月 7 日的文章介绍 Alpöge–Buckmaster 的结果和数学机制；9 月 11 日的声明把讨论扩展到研究激励。声明没有点名 OpenAI、Navier–Stokes、Alpöge 或 Buckmaster，也没有正式裁定 OpenAI 的论文；但它并不脱离这次事件。OpenAI 刚刚把一个著名开放问题作为模型能力展示，而声明直接反对 AI 公司用这类问题作为 benchmark。读者把两者放在同一场讨论中，是合理的。

声明的论证还包含一条清楚的因果判断：benchmark 竞赛推动快速宣布结果，快速宣布又挤压认真写作、方法提炼、先行工作引用和知识整合。这指出了一种真实的制度风险，也让声明在当前语境中具有明确的批评方向。从制度风险走到对一项具体成果的判断，需要实际证据。benchmark 动机说明机构为何投入资源，并提出一个过程假设：发布节奏是否压缩了写作、归属和解释。答案来自论文与形式化、引用记录，以及作者面对批评时的修订和后续说明。商业展示可以与数学贡献同时存在，研究过程的质量需要在另一条证据线上判断。

声明与当前事件有实质关系，对具体成果的判断仍需回到作品。声明列出的写作、归属、解释和传承工作都是真实的学术贡献；它把概念理解置于首位、把解题视为工具和代理，则提出了一套我们并不接受的普遍排序。

## 为什么要把这场事件拆成三个问题

把时间线讲完后，问题才会清楚。这里至少有三种不同的判断，它们需要三种不同的证据。

第一，结论在它明确声明的范围内是否正确，能否被可靠地复现和使用。这是数学判断，核心材料是命题、假设、形式证明、依赖关系、内核检查和独立复现。

第二，一个正确结果怎样成为共同知识。这里要考察论文是否可读，证明中的结构是否被说明，先行工作的贡献是否被定位，其他人是否能学习、复用和继续发展。这是知识传承的判断。

第三，结果是怎样产生和公布的。未公开材料有没有被访问或用于训练，贡献和署名是否准确，优先权如何处理，发布是否给研究者留下公平的选择空间。这是研究过程与治理的判断。

三者会相互影响，却不能互相代答。形式化通过不能自动解决署名争议；一份漂亮的教材回答的是知识传承问题，命题核验需要另一组证据；研究过程的争议也属于另一层判断，不能改写一个已经被可靠检查的结论。把它们压成“这项成果完整”或“这项成果不完整”的总评，反而会掩盖真正需要回答的问题。

## 第一问：形式化的结论在什么意义上正确

“形式化”把命题、变量、假设、依赖和证明写成一个可信内核能够检查的对象。如果论文中的自然语言主张与形式对象逐项对应，依赖和公理状态被公开，内核能够重新检查，并且独立的人或团队能够复现，那么这个结论就在声明的范围内获得了明确的正确性边界。它是否揭示新的结构、是否容易阅读、是否适合进入教材，需要另外的证据。

SAT 给出了最简洁的参照。先固定一个具体的可满足性实例和一套可信的检查规则。求解器若声称实例可满足，可以交出一个赋值供检查；若声称不可满足，可以交出一份能够由独立检查器验证的证书。检查通过以后，下游工作就能在这个明确边界内采用该结论，用它排除一种设计、确认一种约束，或者继续下一步计算。使用者无需先理解求解器搜索过的每一条路径，证书也无需先被提炼成一套优雅理论，结论才开始有用。

形式化的 AI 证明把同一逻辑放进更丰富的对象中。这里固定的是精确命题、证明项、依赖关系和检查内核。只要自然语言命题与形式命题忠实对应，依赖没有隐藏缺口，内核也确实接受证明项，这个定理便可以在所公布的边界内被后续证明调用。这份能够重复检查的证明对象，比模型给出的一句“答案为真”包含更多可审计结构。人类尚未提取出最好的概念结构，会限制解释、教学和推广；已经通过检查的对象依然在公布的边界内构成一项结果。

在这里，我们与联合声明提出的普遍排序有明确分歧。经过可靠检验的新结论本身就是一种数学贡献，并非只是一种等待未来理解来赋予价值的代理。解释证明的结构、形成新概念、推广方法并把知识传给后来者，是另一种数学贡献。有些工作最重要的是结构，有些问题的确切答案本身就具有很高价值，更多时候两者共同构成成果。它们的相对贡献只能逐项判断，不能预先规定概念理解永远居于首位，也不能因为 AI 参与了解答或解释中的某一部分而改变排序。

双重标准的风险并不只来自后来对声明的误读。声明本身把 benchmark 动机与匆忙发布、知识传承不足联系起来，这是一项值得检验的经验判断。完整的判断包含两个步骤。商业 benchmark 提出一个过程假设，询问这种激励是否压缩了写作、归属和解释；论文、形式化、引用、版本记录和后续行为提供判断是否失责的证据。数学标准本身不随动机提高或降低。人类研究者也可能受优先权、奖金或声望驱动而提前发布，成果仍然要回到作品上评价。AI 公司以模型能力为动机时，同一原则继续适用。

如果同样范围、同样形式状态的早期结果由人类发布，通常会获得数月乃至数年的核查和消化时间；如果仅因来源是 AI，就在几天内被要求同时交出教科书式解释，否则不承认其贡献，来源便取代了作品本身。对形式化不忠实、依赖有缺口、论文难读、归属不准确的批评都可以成立，但应当指出具体缺陷，并对人类和 AI 参与的成果使用同一标准。

这仍然没有替 OpenAI 的论文完成数学审查。它给出的是审查顺序：先检查命题、证明对象、依赖和形式化是否对应，再评价结构洞见、可读性、先行工作和长期传承。前一组问题获得答案，不代表后一组工作已经完成；后一组工作需要时间，也不能抹去前一组已经建立的内容。

## 第二问：正确结果如何成为共同知识

联合声明列出的可读写作、讨论、简化、准确归属、教学和后续研究，是数学长期发展的必要工作。这些工作把一个局部结果接入已有文献，使其他人能够理解它的范围、发现其中的方法，并据此继续研究。作者公开一个结果以后，仍然需要为这些环节承担责任。

这些环节构成一种独立的贡献，不是数学价值的唯一来源，也不是使用正确结果之前必须通过的单向门槛。作为人类能够理解、教学和继续发展的知识留下来，是数学成果的一项功能；作为边界清楚、能够被后续证明和计算可靠调用的组件留下来，是另一项功能。两种功能可以互相加强，完成时间也可以不同。哪一种在具体成果中贡献更大，要看问题、定理和用途。

庞加莱猜想的历史说明，深证明需要自己的时间尺度。Perelman 的第一篇相关预印本发布于 2002 年 11 月 11 日，随后两篇材料分别在 2003 年 3 月和 7 月出现；从第一篇预印本到初始材料基本齐备约八个月。之后，Hamilton、Kleiner、Lott、Tian 等人的解说、核查和整理继续推进。到 2006 年，距离第一篇预印本约三年半，这项证明才逐步形成共同体可以公开依靠的理解。它在最初数日没有完成教材化，并不意味着当时没有数学贡献；证明、核查、解释和教学本来就是不同速度的工作。

OpenAI 在 9 月 8 日公开论文和形式化材料，到本文 9 月 14 日修订时只有六天。它把结果作为模型能力展示，确实落在声明批评的 benchmark 激励之内；由此产生的过程问题也很具体：发布节奏是否压缩了写作，文字是否可读，先行工作是否得到妥善处理。benchmark 动机没有直接回答这些问题。仅凭商业动机，或者六天内尚未出现成熟的公共解说，不能认定这项成果已经忽视知识传承。论文、代码、引用、公开记录和后续修订才是相应的证据。若人类提出同样的结果会获得较长的理解时间，AI 参与的结果也应得到同样的时间尺度。

更合适的路径，是让不同贡献并行推进并留下记录：保存初始形式结果，写成人类可读的论文，公开预印本并接受外部审评，根据批评修订和更正，再由综述、课堂、教材和后续研究逐步提取结构。机器可以缩短发现和形式化的时间；人类共同体继续承担解释、归属、选择和传授。每一层都增加成果的价值，没有一层需要否定另一层才能说明自身的重要性。

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

On September 11, Tao published “A Severe Misalignment of AI in Mathematics,” initially signed by 25 Fields medalists. He wrote that the text grew out of discussions among the signatories during the previous week and was released quickly because they considered the situation urgent. The declaration states a clear hierarchy of value: solving problems is a tool and proxy for the mathematical community’s primary goal, which it identifies as conceptual understanding and insight. It criticizes the competition among AI companies to use famous open problems as model benchmarks, warning that rapid true-or-false announcements can crowd out careful writing, the isolation of new methods, citations to prior work, and the work by which mathematicians integrate a result into shared knowledge.

The two interventions are close in time and subject, but they serve different purposes. The September 7 post introduced the Alpöge–Buckmaster results and their mathematical mechanism. The September 11 declaration widened the discussion to research incentives. It did not name OpenAI, Navier–Stokes, Alpöge, or Buckmaster, and it did not formally adjudicate OpenAI’s paper. It was nevertheless connected to the event. OpenAI had just presented a famous open problem as a demonstration of model capability, while the declaration directly opposed the use of such problems as AI benchmarks. Readers can reasonably place both in the same discussion.

The declaration also contains a clear causal claim: benchmark competition drives rapid announcements, and rapid announcements crowd out careful writing, the isolation of methods, citations to prior work, and integration into shared knowledge. This identifies a real institutional risk and gives the declaration a definite critical direction in the present context. A judgment about a particular result requires evidence beyond that institutional risk. The benchmark motive explains why an organization invested resources and raises a process hypothesis: did the release schedule compress writing, attribution, and explanation? The answer comes from the paper and formalization, the citation record, and the authors’ response through criticism, revision, and later exposition. Commercial demonstration can coexist with mathematical contribution, while process quality is assessed on a separate line of evidence.

The declaration has a substantive relation to the event, while judgment of the particular result must return to the work itself. Its demands for writing, attribution, explanation, and transmission identify real scholarly contributions. Its placement of conceptual understanding first, with problem solving as a tool and proxy, advances a general hierarchy that we do not accept.

## Why the event contains three different questions

Once the timeline is clear, the structure of the discussion becomes visible. At least three judgments are involved, and each requires different evidence.

The first is whether a conclusion is correct within the scope it states, and whether it can be reliably reproduced and used. This is a mathematical judgment. Its materials are the proposition, hypotheses, formal proof, dependencies, kernel check, and independent reproduction.

The second is how a correct result becomes shared knowledge. This asks whether the paper can be read, whether the proof’s structure has been explained, whether prior work and credit have been located, and whether others can learn, reuse, and extend the result. This is a knowledge-transmission judgment.

The third is how the result was produced and released. Were unpublished materials accessed or used for training? Were contributions and authorship recorded accurately? Were priority and publication choices handled fairly? This is a research-process and governance judgment.

The three questions interact, but they cannot answer one another. A formal proof answers a mathematical question, while an authorship dispute requires institutional evidence. A beautiful exposition answers a knowledge-transmission question, while proposition verification requires its own evidence. A process problem belongs to a third layer and leaves a reliably checked conclusion mathematically intact. Reducing everything to one verdict about whether a result is “complete” hides the evidence each question actually requires.

## First question: in what sense is a formalized conclusion correct?

Formalization expresses a proposition, variables, hypotheses, dependencies, and proof as an object checked by a trusted kernel. If the natural-language claim corresponds term by term to the formal object, the dependencies and axioms are disclosed, the kernel can recheck the proof, and an independent person or team can reproduce it, the conclusion has a definite correctness boundary within its stated scope. Whether it reveals a new structure, reads well, or belongs in a textbook requires different evidence.

SAT gives the cleanest reference point. Begin with a fixed satisfiability instance and trusted checking rules. A solver that claims satisfiability can provide an assignment; one that claims unsatisfiability can provide a certificate for an independent checker. Once the check succeeds, downstream work can rely on that bounded conclusion to reject a design, confirm a constraint, or continue a computation. The checked conclusion can enter downstream work while the solver’s search remains conceptually opaque and while an elegant theory has yet to be extracted from the certificate.

A formalized AI proof places the same logic in a richer object. Here the fixed items are the precise proposition, proof term, dependencies, and checking kernel. If the natural-language theorem faithfully matches the formal proposition, the dependency boundary contains no hidden gap, and the kernel accepts the proof term, later proofs can invoke the theorem within that published boundary. This is more than a model saying that an answer is true; it is a proof object that can be checked again. The absence of a mature human account limits explanation, teaching, and generalization. It does not turn an accepted proof object into a result that does not yet exist.

Here we differ explicitly from the declaration’s general hierarchy. A reliably checked new conclusion is itself a mathematical contribution. Its established content has value from the outset, and later understanding adds another form of value. Explaining the proof’s structure, forming new concepts, extending the method, and transmitting it to later researchers constitute another kind of mathematical contribution. In some work the structure is the main achievement; in other problems the exact answer carries substantial value by itself; often both matter. Their relative weight must be judged case by case. Conceptual understanding cannot be ranked first in advance, and AI participation in either the solution or its explanation cannot determine that ranking.

The risk of a double standard does not arise only from later misreadings of the declaration. The declaration itself connects benchmark motives with rushed publication and weak transmission, an empirical claim worth testing. A complete judgment has two steps. A commercial benchmark raises a process hypothesis about whether the incentive compressed writing, attribution, and explanation. The paper, formalization, citations, version record, and later conduct provide the evidence for deciding whether responsibility was neglected. The mathematical standard does not rise or fall with the motive. Human researchers may also release early under pressure from priority, prizes, or prestige, and their work still returns to evaluation on its merits. The same principle applies when an AI company is motivated by model capability.

If an early result with the same scope and formal status would receive months or years of checking and digestion when released by a human, an AI-originated result should not be denied recognition merely because it has not supplied a textbook account within days. Criticism of an unfaithful formalization, a dependency gap, unreadable writing, or inaccurate attribution may all be justified. It should identify the actual defect and use the same standard for human and AI-assisted work.

This argument does not complete a mathematical review of OpenAI’s paper. It establishes an order of review: first check the proposition, proof object, dependencies, and fidelity of the formalization; then evaluate structural insight, readability, prior work, and long-term transmission. An answer to the first group does not complete the second. The time required by the second cannot erase what the first has established.

## Second question: how does a correct result become shared knowledge?

The declaration names several tasks that are necessary to the long development of mathematics: readable writing, discussion, simplification, accurate attribution, teaching, and later research. They connect a local result to the literature, allow others to understand its scope and methods, and make further research possible. Authors remain responsible for this work after a result is released.

These tasks form an independent contribution. Mathematical value also arises from an established conclusion, and a bounded correct result can be used while explanation and transmission continue. Preserving a result as knowledge that people can understand, teach, and develop is one function of mathematics. Preserving it as a bounded component that later proofs and computations can reliably invoke is another. The two functions can reinforce each other and mature at different times. Their relative contribution depends on the problem, theorem, and use.

The history of the Poincaré conjecture shows why deep proofs have their own timescale. Perelman’s first related preprint appeared on November 11, 2002. Two further papers followed in March and July 2003, so the initial materials took about eight months to assemble. Exposition, checking, and reorganization continued through work by Hamilton, Kleiner, Lott, Tian, and others. By 2006, roughly three and a half years after the first preprint, the proof had gradually acquired an account on which the community could publicly rely. Its failure to become textbook mathematics in its first days did not mean that it had made no mathematical contribution. Proof, checking, explanation, and teaching proceed at different speeds.

OpenAI released its paper and formal materials on September 8. Only six days had passed by this article’s revision on September 14. Its presentation of the result as a demonstration of model capability does fall within the benchmark incentive criticized by the declaration. The resulting process questions are concrete: did the release schedule compress the writing, is the paper readable, and was prior work handled properly? The benchmark motive does not answer them. Evidence of neglected transmission must come from the paper, code, citations, public record, and later revisions; commercial motive and a six-day interval describe the context of that inquiry. The paper, code, citations, public record, and later revisions provide the relevant evidence. If an equivalent human result would receive a longer period for understanding, an AI-assisted result should receive the same timescale.

A sounder path lets the contributions proceed in parallel and preserves their record: retain the initial formal result, write a paper that people can read, publish a preprint and invite external review, revise and correct it in response, and allow surveys, classrooms, textbooks, and later research to extract structure over time. Machines can shorten discovery and formalization. The human community continues the work of explanation, attribution, selection, and teaching. Each layer adds value without having to deny the value of another.

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

9月7日、Terry Tao は Alpöge–Buckmaster の仕事を刺激的な新展開として紹介しました。三つの結果は外力のない Navier–Stokes 問題にはまだ届いていませんが、この経路をさらに進めることが現実的になったと説明しています。また、議論は AI の支援を強く受けており、著者たちは非常に読みにくい最初の草稿を専門的な説明へ書き直していると述べました。Tao 自身も、議論や現代のツールを使いながら、さらに時間をかけて証明を理解する必要があるとしています。Tao にとって、問題を解くことは数学的理解へ進む手段であり、理解と洞察がより深い目標です。

9月11日、Tao は “A Severe Misalignment of AI in Mathematics” を公表し、最初の署名者は25人のフィールズ賞受賞者でした。署名者による前週の議論から生まれ、状況が緊急だと考えたため早く公開したと説明しています。声明は、価値について明確な順序を示しています。問題を解くことは数学共同体の「第一の目標」に向かう道具であり代理で、その目標は概念的理解と洞察だとします。また、著名な未解決問題をモデルの benchmark にする AI 企業間の競争を批判し、真偽の答えを急いで発表することが、丁寧な執筆、新しい方法の抽出、先行研究の引用、数学者が結果を共有知へ組み込む時間を圧迫すると警告しています。

二つの発言は時間と主題の面で近くにありますが、役割は異なります。9月7日の記事は Alpöge–Buckmaster の結果と数学的機構を紹介し、9月11日の声明は研究上の動機へ議論を広げました。声明は OpenAI、Navier–Stokes、Alpöge、Buckmaster の名を挙げず、OpenAI の論文を正式に裁定してもいません。それでも、この出来事と切り離されてはいません。OpenAI は著名な未解決問題をモデル能力の実演として示し、声明はそのような問題を AI の benchmark に使うことを直接批判しています。両者を同じ議論の中で読むのは自然です。

声明には明確な因果判断もあります。benchmark の競争が発表を速め、その速さが丁寧な執筆、方法の抽出、先行研究の引用、共有知への統合を圧迫するという判断です。これは現実にあり得る制度的リスクを示し、現在の文脈で声明に明確な批判方向を与えています。ただし、リスクから事実判断へ進むには検査が必要です。問題をモデルの benchmark に使うことは、組織が資源を投入した理由を説明します。それだけで論文の説明が不足していたことや、研究者が伝承を軽視したことは証明できません。商業的な実演と数学的貢献は両立します。伝承が十分だったかは、論文と形式化を読み、引用と帰属を調べ、批判、改訂、後の解説への対応を見ることで判断すべきです。

声明は現在の出来事と実質的に関係していますが、具体的な成果の判断は作品そのものに戻る必要があります。執筆、帰属、説明、伝承は実質的な学術貢献です。一方、概念的理解を第一に置き、問題を解くことを道具と代理として位置づける一般的な順序を、私たちは受け入れません。

## なぜこの出来事を三つの問いに分けるのか

時間軸をたどると、議論の構造が見えてきます。少なくとも三つの判断があり、それぞれ異なる証拠を必要とします。

第一は、結論が明示した範囲で正しいか、信頼して再現・使用できるかです。命題、仮定、形式証明、依存関係、カーネル検査、独立再現が中心になります。

第二は、正しい結果がどのように共有知になるかです。論文を読めるか、証明の構造が説明されているか、先行研究と貢献が位置づけられているか、他者が学び、再利用し、拡張できるかを問います。

第三は、結果がどのように生まれ、公開されたかです。未公開資料がアクセスまたは訓練に使われたか、貢献と著者表示が正確か、優先権と公開の選択が公平だったかを調べます。

三つは関係しますが、互いの代わりにはなりません。形式証明は著者表示の争いを解決せず、きれいな解説は命題の検証を置き換えません。過程の問題も、検査済みの結論を数学的誤りにはしません。「完全な成果か」という一つの評点に押し込めると、それぞれの証拠が見えなくなります。

## 第一の問い：形式化された結論はどの意味で正しいのか

形式化は、命題、変数、仮定、依存関係、証明を、信頼できるカーネルが検査できる対象として表します。自然言語の主張と形式対象が一つずつ対応し、依存関係と公理が公開され、カーネルが再検査でき、独立した人やチームが再現できるなら、その結論は明示された範囲で明確な正しさの境界を持ちます。新しい構造を示すか、読みやすいか、教科書に入るかは、別の証拠を必要とします。

SAT は最も簡潔な参照になります。まず、具体的な充足可能性のインスタンスと、信頼する検査規則を固定します。ソルバーが充足可能だと主張するなら代入を示せます。充足不能だと主張するなら、独立チェッカーが検査できる証明書を示せます。検査に通れば、後の作業はその境界内で結論を使い、設計を除外し、制約を確認し、次の計算へ進めます。利用者はソルバーが探索した枝をすべて理解する必要がなく、証明書が先に美しい理論へ変わる必要もありません。

形式化された AI の証明は、同じ論理をさらに豊かな対象に置きます。ここで固定されるのは、正確な命題、証明項、依存関係、検査カーネルです。自然言語の定理が形式命題と忠実に一致し、依存関係に隠れた穴がなく、カーネルが証明項を受理するなら、後続の証明は公表された境界内でその定理を利用できます。この繰り返し検査できる証明対象は、モデルによる一言の「真」という回答より多くの監査可能な構造を含みます。人間による成熟した説明がないことは、解説、教育、一般化を制限します。受理された証明対象は、公表された境界内ですでに一つの結果を構成します。

ここで私たちは、声明が示す一般的な順序と明確に異なる見方を取ります。信頼できる検査を通った新しい結論は、それ自体が数学的貢献です。将来の理解によって初めて価値を得る代理にすぎないとは考えません。証明の構造を説明し、新しい概念を作り、方法を拡張し、後の研究者へ伝えることは、もう一つの数学的貢献です。構造が主な成果になる仕事も、正確な答えそのものが大きな価値を持つ問題もあり、多くの場合は両方が重要です。相対的な重みは個別に判断する必要があります。概念的理解を常に第一に置くことも、解答や説明の一部に AI が参加したことで順序を変えることもできません。

二重基準の危険は、声明の後の誤読だけから生まれるわけではありません。声明自体が benchmark の動機と、急いだ公開や弱い知識伝承を結びつけています。これは検証すべき経験的な判断ですが、作品を調べずに結論にはできません。より完全な推論は、商業的 benchmark が検証すべき過程上の仮説、つまり動機が執筆、帰属、説明を圧縮したかという問いを生み、論文、形式化、引用、版の記録、その後の対応が責任を果たしたかを判断する証拠を与える、というものです。数学的基準そのものは動機によって上下しません。人間の研究者も優先権、賞金、名声の圧力で早く公開することがありますが、動機だけで結果は消えません。モデル能力の実演という動機も、検査済みの結論の数学的価値を単独で下げることはできません。

同じ範囲と形式化状態の初期結果を人間が公表すれば数か月、場合によっては数年の検査と理解の時間が与えられるなら、AI 由来の結果だけに数日以内の教科書的説明を要求し、それがなければ貢献を認めないのは対称な評価ではありません。形式化の不一致、依存関係の穴、読みにくい論文、不正確な帰属への批判は成立し得ます。批判は具体的な欠陥を示し、人間と AI 支援の成果に同じ基準を使うべきです。

この議論は OpenAI の論文の数学的審査を完了するものではありません。まず命題、証明対象、依存関係、形式化の忠実性を調べ、その後で構造的洞察、可読性、先行研究、長期的な伝承を評価するという順序を示します。前の問いに答えがあっても後の仕事は完了しません。後の仕事に時間がかかっても、前の検査が確立した内容は消えません。

## 第二の問い：正しい結果はどのように共有知になるのか

読みやすい執筆、議論、簡約、正確な帰属、教育、後続研究という声明が挙げた仕事は、数学の長期的な発展に必要です。局所的な結果を既存文献へつなぎ、他の人が範囲と方法を理解し、次の研究へ進めるようにします。結果を公開した後も、著者はこれらの仕事に責任を持ちます。

これらの仕事は独立した貢献です。数学的価値の唯一の源でも、正しい結果を使う前に必ず通る一方向の門でもありません。人が理解し、教え、発展させられる知識として結果を残すことは、数学の一つの機能です。後続の証明と計算が信頼して呼び出せる、境界の明確な部品として残すことは別の機能です。二つは互いを強め、異なる時期に成熟できます。具体的な貢献の大きさは、問題、定理、用途によって決まります。

ポアンカレ予想の歴史は、深い証明に固有の時間尺度があることを示します。Perelman の最初の関連プレプリントは2002年11月11日に公開され、その後の二本が2003年3月と7月に現れました。初期資料がそろうまで約8か月です。その後も Hamilton、Kleiner、Lott、Tian らによる解説、検証、整理が続きました。2006年には、最初のプレプリントから約3年半を経て、共同体が公に頼れる理解が徐々に形成されました。最初の数日で教科書的な数学にならなかったことは、当時の数学的貢献がなかったことを意味しません。証明、検査、説明、教育は異なる速度で進みます。

OpenAI が論文と形式資料を公開したのは9月8日です。この記事の改訂日である9月14日まで、わずか6日しかありません。モデル能力の実演として結果を示したことは、声明が批判する benchmark の動機に確かに含まれます。そこから生じる過程上の問いは具体的です。公開日程が執筆を圧縮したのか、文章は読めるのか、先行研究を適切に扱ったのか。benchmark の動機だけでは答えは出ません。商業的な動機や、6日以内に成熟した公開解説がないことだけでは、知識伝承が軽視されたとは確定できません。論文、コード、引用、公開記録、その後の改訂が判断の証拠になります。同じ結果を人間が発表した場合に長い理解期間を認めるなら、AI 支援の結果にも同じ時間尺度を認めるべきです。

より適切な道は、異なる貢献を並行して進め、その記録を残すことです。最初の形式結果を保存し、人が読める論文を書き、プレプリントを公開して外部審査を受け、批判に応じて修正し、サーベイ、授業、教科書、後続研究が時間をかけて構造を抽出します。機械は発見と形式化を短縮できます。人間共同体は説明、帰属、選択、教育を続けます。各層は、別の層の価値を否定することなく成果に価値を加えます。

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
