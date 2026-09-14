---
first_published: 2026-09-12
last_revised: 2026-09-14
---

# zh

> 编辑主稿（中文）。网页三语内容由本稿整理后生成；本稿用于完整的线性阅读和论证维护。

## 这一周发生了什么
<!-- aside: opening -->


OpenAI 的公开说明称，团队在 2026 年 9 月 1 日听到两个千禧年大奖难题可能已被解决的传闻，随后启动了对尚未解决的千禧年难题和若干高影响问题的模型评估。内部系统先得到一个无外力 Euler 方程结果，团队据此把资源集中到 Navier–Stokes 问题。OpenAI 称系统在 9 月 5 日形成解析解答，随后用 17 小时完成 Lean 形式化，并于 9 月 8 日公布论文和代码。Lean 是一种交互式定理证明工具，可以把证明步骤交给一个较小、可重复运行的检查器核验。

Buckmaster 的公开陈述记录了研究者一侧的经历。他在 9 月 3 日因传闻和相关消息联系 OpenAI。9 月 6 日的两次通话中，他询问内部模型是否访问过、或曾用他们此前两个月存入 Codex 会话的研究材料进行训练。他写道，当时得到的回答覆盖了直接查阅用户数据，却没有明确回答训练问题。Alpöge 与 Buckmaster 随后改变原定节奏，于 9 月 7 日提前公开了不可压缩多孔介质方程、Boussinesq 方程和不可压缩 Euler 方程的三项有限时间爆破结果及 Lean 形式化。它们与 OpenAI 的 Navier–Stokes 结果属于不同定理。

OpenAI 在 9 月 10 日补充称，Buckmaster 此前两个月的 Codex 提示不可能以任何方式影响这套内部系统，包括通过训练；公司还称研究人员和智能体在 Alpöge 与 Buckmaster 公开工作以前没有看到其成果。Buckmaster 的文书则记录了他对通话答复、竞争性研究、发表压力和优先权安排的疑问。公开材料因此留下了两组需要依靠过程证据核对的主张。

9 月 11 日，Terry Tao 发布了由 25 位菲尔兹奖得主签署的《A Severe Misalignment of AI in Mathematics》。Tao 说，这份文字来自签署者在此前一周的讨论。联合声明把著名未解问题作为模型能力竞赛的现象放进更长的数学传统中考察。它强调讨论、简化、仔细写作、先行工作与归属、教学，以及从证明中提炼概念和新问题；在它的叙述里，解决问题是通向概念理解和洞察的工具，如果没有数学家继续发展并把 AI 构想纳入数学传统，这些想法就难以真正“活起来”。

这份声明与前几天的事件有直接的时间和主题联系，但公开文字讨论的范围更广，并不是一份针对某一份证明作出数学裁决的评审意见。它主要提出一个关于完整数学工作的要求：结果需要被共同体讨论、解释、放回先行研究，并由人类继续发展。OpenAI 的说明强调迅速发现和形式化新结果的能力；Buckmaster 的陈述把未公开研究材料、直接沟通、竞争性发表和优先权带进了讨论。三份材料呈现了同一周争议的不同侧面。

这次事件把三个时间尺度压缩到了一起。证明可以在数日内生成并形式化，人类对深证明的理解通常需要更久，而数据、合作与发表规则必须在竞争发生时就发挥作用。由此出现三个相连、但不能互相代答的问题：结论在什么意义上正确，正确的结论怎样成为共同知识，以及产生结论的过程怎样保护合作与优先权。

## 第一问：结论在什么意义上正确

数学正确性首先要求一个精确对象。需要写清假设、定义和结论，并确认论文中的主张与形式系统实际检查的定理逐项对应。如果可信内核验证了从给定假设到该定理的完整证明，所有依赖和公理状态也清楚，独立团队能够重新运行检查，那么这个结论就在它所声明的边界内成立。可信内核是证明工具中负责逐步验算的最小程序；它核验形式证明项，论文与形式对象的对应关系仍须由人检查。

这个判断回答的是“这个结论能否作为可靠前提继续使用”。它不等同于“这已经是一项完成了所有知识传承工作的数学贡献”，也不要求读者已经理解证明为什么采取这条路线。解释力、优雅程度和研究启发性会影响一个结果能走多远，却不会改变一个已经被准确核验的局部结论。

因此，数学地位需要一条可复查的证据链：公开精确命题、完整形式化、依赖版本和复现方法；由独立研究者核对论文与代码的对应关系；把检查结果、发现的问题、公理和依赖状态以及修订历史一并保存。形式化通过以后，结论的数学状态可以先得到回答；知识传承和结构解释仍然需要继续完成。

## 第二问：为什么不能把知识传承设为使用正确结果的前置条件

这里是本文最明确的判断。SAT 提供了一个解释程度更低、但已经被广泛接受的参照。对于一个具体的布尔可满足性问题，求解器可能给出一份极其庞大的证书，通常没有人会逐行理解它的数学意义。要判定这个实例不可满足时，独立检查器确认这份证书以后，人们就会接受这一结论，并把它用于协议验证、调度或有限组合研究。它可能没有简洁的概念证明，也没有揭示可以推广的结构；可检查性仍然赋予这个具体结论明确的使用价值。

经过形式化的 AI 证明至少具备同样的基本条件，而且通常还提供了按定义、引理和推导步骤组织的完整形式结构。它可能很长，证明路线也可能尚未被人类真正理解。只要论文命题、形式定理和全部依赖准确对应，可信内核通过，独立团队能够重现检查，后续研究就可以在所声明的范围内引用它、调用它或以它为前提继续证明。

这条逻辑不能因为证明来自 AI 就被改写。若我们接受经过独立检查的 SAT 证书可以支持受限使用，就应当按照同一数学标准处理经过形式化和内核检查的 AI 证明。只因为结果的生成者是 AI，就要求它在几天内先完成概念解释、教材化和共同体传承，再承认它具有科学或工程价值，这就是对来源额外加上的门槛，也构成 double standard。人类写出的深证明如果在公开数日后仍然难以消化，我们通常会说它需要更多审读和说明，而不会仅因尚未进入教材就否认其正确性或潜在用途。

庞加莱猜想的现代证明提供了一个熟悉的时间尺度参照。初次公开与形成适合广泛阅读的完整说明之间，隔了相当长的共同体审读和重写过程。OpenAI 的材料在 9 月 8 日公开，到本文写作的 9 月 14 日只有六天。公开记录尚未显示成熟的人类解释，只能说明截至该日期，公共材料还没有完成这种转化。若人类作者可以获得更长的理解时间，AI 产生的证明也应接受同样的时间尺度。

承认一个经过核验的结果可以被使用，并不等于宣称它已经完成了知识传承，也不等于把特殊情形推广成一般理论。它只表示：在明确的定义、假设和验证范围内，这个结论已经具有可引用、可调用的价值。数学贡献的成熟度可以被诚实标注，正确性却不应因来源而被重新定价。

## 第三问：正确结论怎样成为共同知识
<!-- aside: contextual -->


联合声明强调的知识传承仍然是数学的核心工作。一个定理进入共同知识，需要有人解释它解决了什么，把它放回先行文献，说明关键机制和适用范围，澄清哪些步骤能够复用，并留下其他研究者可以继续使用的语言。教学、直觉、抽象、归属和新问题使一个结果跨越研究小组和世代。

本文把这项工作与正确性放在两条可以并行推进的轴上，也因此保留了它应有的地位。经过核验的结果可以先以准确标明边界和成熟度的形式公开、引用和使用；人类可读的重写、结构解释、历史定位、外部审评和教学材料随后继续完善。知识传承让结果更容易被理解、推广和创造性地使用，但它不应成为正确结果获得数学地位或受限使用价值的事前许可。

时间在这里尤其重要。深证明从首次公开到共同体形成稳定解释，本来就可能需要数月或数年。六天内还没有成熟的公共说明，不能被读成结果没有留下知识，也不能被读成证明已经被人类充分理解。我们能做的判断应当与公开证据的时间范围相称。

更完整的知识转化路径会保留多个阶段：可检查的初始结果，人类可读的论文，形式证明与复现记录，公开预印本，外部审评及其带来的修订，之后形成的综述、教材和新的研究方向。机器可以缩短发现和形式化的时间；理解、选择、归属和传播仍由人类共同体完成。这些阶段共同构成知识传承，可以并行推进、前后衔接，不必排成一条单行队列。

## 第四问：结果有价值，与产生过程是否恰当，是两次判断

数学结论的真伪无法回答研究过程是否公平。模型公司可以通过解决困难问题展示能力并获得商业声誉；只要产生了可验证的新知识，这项活动也可能为科学提供真实贡献。需要另外追问的是取得贡献的过程付出了什么代价：未公开的人类研究是否得到同意和隔离，贡献是否被准确记录，掌握模型、日志和发表渠道的一方是否利用了信息和资源上的优势。

这次事件使问题具体化。OpenAI 公开承认项目由未解问题可能取得突破的传闻触发；Buckmaster 此前使用 Codex 处理未公开研究，并在 OpenAI 项目公布前与公司进行了直接沟通。OpenAI 后来明确主张，这些 Codex 提示不可能影响内部系统，研究团队在相关成果公开前也没有看到其工作。Buckmaster 的陈述记录了他为何认为通话答复和发表安排仍留下疑问。公开数学材料可以回答证明的形式核验问题；这些过程主张需要访问日志、训练和评估数据的来历、时间戳、通信记录以及可由独立第三方执行的调查来回答。

一个结果可以在数学上正确且具有科学价值，同时其研究过程仍然需要治理审查。反过来，一个过程即使完全合规，也不能替错误证明提供数学信用。承认科学贡献不等于替过程背书，追问过程也不等于抹去结果的价值。把两次判断分开，才能同时保护知识和研究者。

竞争本身并不罕见，公开展示模型能力也可能推动工具发展。问题出现在竞争改变了研究者的选择空间：如果研究者担心未公开想法进入训练、评估或相邻项目，他们可能停止分享早期工作；如果企业掌握普通用户无法核实的访问记录、训练边界和内部时间线，优先权争议就很难靠公开声明解决。

可行的治理需要在争议发生以前建立。研究用途的模型应清楚区分产品改进、训练、内部评估和竞争性研究，并提供可以核查的隔离模式；重要访问和模型版本应留下审计记录；接触未公开研究后启动相邻项目，应有利益冲突登记、内部隔离和发表审查；优先权争议应保全时间戳、通信和访问日志，并允许独立第三方在保密条件下核查。制度应避免在事实未明时替任何一方预先定罪，同时让事实能够被可靠地查明。

## 三类判断怎样共同落地

同一份成果可以同时拥有三种状态，而它们不应互相覆盖：

- **数学状态**：命题、形式定理、依赖和公理状态、可信内核检查以及独立复现，说明结论在什么范围内成立。
- **知识状态**：可读论证、结构解释、先行工作、归属、教学和后续问题，说明结果在共同体中成熟到了什么程度。
- **过程状态**：数据用途、访问记录、同意、竞争规则和优先权程序，说明研究过程能否获得信任。

这套分层让每个问题都由自己的证据回答，也避免给成果贴一个总分。形式化核验可以先完成，知识传承可以同时推进，过程审查也可以独立进行。一个状态的暂时空缺，不应被偷换成另外两个状态的否定。

## 这场讨论真正要求我们做什么

这场事件不要求科学在机器能力和人类知识之间二选一。它要求我们把判断做得更精确：对已通过可信检查的结果，给出与证据相称的数学地位和受限使用范围；对尚未完成的解释，继续投入人类的理解、归属、教学和结构提炼；对涉及未公开研究和竞争性发表的过程，建立可审计、可复核的治理规则。

由此得到的立场很明确。数学作品应当根据它实际提供的命题、证明、边界、复现证据和解释质量来评价。AI 参与研究不会自动降低一个结果的价值，也不应让它获得免于人类阅读和知识传承的豁免。正确性、知识传承和研究伦理都重要，但它们属于不同的判断链。把其中任何一条强行设成另外一条的前置条件，都会让讨论失去应有的精度。

新技术带来的速度变化需要新的制度回应，也需要耐心的共同体工作。最可靠的路径，是让可以核验的结果及时进入科学使用，同时让人类继续把它解释、传承、改进，并确保产生它的过程尊重合作、归属和优先权。



# en

> Editorial master. The website’s three-language content is generated from this file; the file is maintained for complete linear reading and argument review.

## What happened over the course of a week
<!-- aside: opening -->

OpenAI’s public account says that on September 1, 2026, it heard rumors that two Millennium Prize Problems might have been solved and began evaluating its models on the remaining Millennium problems and several other high-impact questions. An internal system first produced a result for the unforced Euler equations, which led the team to concentrate resources on Navier–Stokes. OpenAI says the system formed an analytic solution on September 5, completed a Lean formalization in 17 hours, and released the paper and code on September 8. Lean is an interactive theorem prover that lets a comparatively small, repeatable checker verify formal proof steps.

Buckmaster’s public statement records the researchers’ experience. He contacted OpenAI on September 3 after hearing rumors and related reports. In two calls on September 6, he asked whether the internal model had accessed, or been trained on, research materials that he and Alpöge had placed in Codex sessions during the previous two months. He writes that the answers addressed direct inspection of user data without clearly resolving the training question. Alpöge and Buckmaster then changed their planned schedule and released, on September 7, three finite-time blow-up results for the incompressible porous media, Boussinesq, and incompressible Euler equations, together with Lean formalizations. These are different theorems from OpenAI’s Navier–Stokes result.

On September 10, OpenAI added that Buckmaster’s Codex prompts from the previous two months could not have influenced the internal system in any way, including through training. It also says its researchers and agents had not seen the Alpöge–Buckmaster work before that work became public. Buckmaster’s document records why he continued to question the answers given during the calls, the handling of competing research, publication pressure, and priority arrangements. The public record therefore contains two sets of process claims that require process evidence to assess.

On September 11, Terry Tao published “A Severe Misalignment of AI in Mathematics,” signed by 25 Fields medalists. Tao says the text grew from discussions among the signatories during the preceding week. The declaration places the use of famous open problems as model benchmarks within a longer mathematical tradition. It calls for talks, simplifications, careful writeups, prior work and attribution, teaching, and the extraction of concepts and new questions from proofs. In its account, solving a problem is a tool for reaching conceptual understanding and insight; without mathematicians who continue to develop AI-conceived ideas and integrate them into mathematical tradition, those ideas may never become fully alive.

The declaration has a direct chronological and thematic connection to the events of the preceding days, but its public text has a broader scope. It is not a mathematical verdict on one particular proof. It sets out what is needed for an AI result to mature into complete mathematical work: discussion, explanation, placement among earlier research, and continued human development. OpenAI emphasizes rapid discovery and formalization; Buckmaster’s account brings unpublished materials, direct communication, competitive publication, and priority into view. The three documents present different sides of the same week’s episode.

The episode compresses three timescales. A proof can be generated and formalized within days; human understanding of a deep proof usually takes longer; rules for data, collaboration, and publication must already work while the competition is taking place. The same event therefore raises three connected questions that cannot answer one another: in what sense is the result correct, how does a correct result become shared knowledge, and how should the process that produced it protect collaboration and priority?

## First question: in what sense is the result correct

Mathematical correctness begins with a precise object. The assumptions, definitions, and conclusion must be stated, and the claim in the paper must correspond exactly to the theorem checked by the formal system. If a trusted kernel verifies a complete derivation from the stated assumptions, the status of all dependencies and axioms is clear, and an independent team can rerun the check, then the result holds within its declared boundary. The trusted kernel is the small part of a proof system that checks a formal proof term; people must still check that the paper and the formal object say the same thing.

This judgment answers whether the conclusion can serve as a reliable premise for later work. It is not the same as saying that every task of knowledge transmission has been completed, and it does not require readers already to understand why the proof took this route. Explanatory power, elegance, and research fertility affect how far a result can travel, while leaving an accurately verified local conclusion intact.

Mathematical status therefore needs a reviewable evidence chain: the exact statement, complete formalization, dependency versions, and reproduction instructions should be public; independent researchers should compare the paper with the code; verification results, discovered defects, the status of axioms and dependencies, and revision history should remain available. Once formalization passes, the mathematical status of the conclusion can be answered. Knowledge transmission and structural explanation still require further work.

## Second question: why knowledge transmission cannot be a precondition for using a correct result

This is the clearest judgment in this discussion. SAT offers a reference with even less explanation. For a particular Boolean satisfiability instance, a solver may produce an enormous certificate whose mathematical meaning no person understands line by line. When the goal is to establish that the instance is unsatisfiable, an independent checker can validate the certificate; people can then use that conclusion in protocol verification, scheduling, or finite combinatorics. The certificate may offer no compact conceptual proof and reveal no general structure. Its checkability still gives the particular conclusion a definite use value.

A formalized AI proof meets at least the same basic condition and usually supplies more: a complete formal structure organized through definitions, lemmas, and derivation steps. It may be long, and people may not yet understand why its route works. When the paper statement, formal theorem, and all dependencies correspond exactly, a trusted kernel accepts the proof, and an independent team can reproduce the check, later work can cite it, invoke it, or use it as a premise within its declared scope.

This logic cannot be rewritten because the proof came from AI. If we accept that an independently checked SAT certificate can support bounded use, we should apply the same mathematical standard to a formalized, kernel-checked AI proof. Requiring an AI result to complete conceptual explanation, textbook treatment, and community transmission within days before recognizing scientific or engineering value adds a source-based hurdle. It is a double standard. When a human writes a deep proof that remains difficult to absorb a few days after publication, we normally say that it needs more scrutiny and exposition. We do not deny its correctness or possible use simply because it has not yet entered a textbook.

The modern proof of the Poincaré conjecture offers a familiar time-scale reference. A substantial period of community scrutiny and rewriting separated its initial public appearance from accounts suitable for broad reading. OpenAI released its materials on September 8; only six days had passed by the date of this post, September 14. The public record had not yet shown a mature human explanation; that establishes only that this transformation had not appeared in public materials by that date. If a human author is allowed a longer period of understanding, an AI-originated proof should be judged on the same timescale.

Recognizing that a checked result can be used does not say that it has completed knowledge transmission, or that a special case has become a general theory. It says that under its stated definitions, assumptions, and verification scope, the conclusion has value as something that can be cited or invoked. The maturity of a mathematical contribution can be stated honestly; its correctness should not be repriced because of its source.

## Third question: how a correct result becomes shared knowledge
<!-- aside: contextual -->

The knowledge transmission emphasized by the declaration remains core mathematical work. For a theorem to become shared knowledge, someone must explain what it solves, place it among earlier research, describe its mechanism and scope, clarify which steps can be reused, and leave a language in which other researchers can continue. Teaching, intuition, abstraction, attribution, and new questions allow a result to cross research groups and generations.

This discussion places that work on an axis that can advance alongside correctness, preserving its status while adding a second question. A checked result can first be released, cited, and used with its boundary and maturity stated accurately. Human-readable rewriting, structural interpretation, historical placement, external review, and teaching materials can then continue to develop. Knowledge transmission makes a result easier to understand, generalize, and use creatively; it should not become prior permission for a correct result to acquire mathematical status or bounded use value.

Time matters especially here. A deep proof can take months or years to move from first publication to a stable community explanation. Six days without a mature public account cannot be read as proof that the result has left no knowledge, and it cannot be read as proof that the proof has already been fully understood. Our judgment should match the time range covered by the public evidence.

A fuller path of knowledge conversion preserves several stages: a checkable initial result, a human-readable paper, a formal proof and reproduction record, a public preprint, external review and the revisions it brings, and later surveys, teaching materials, and new research directions. Machines may shorten discovery and formalization; understanding, selection, attribution, and transmission remain work for the human community. These stages together form knowledge transmission, but they do not need to be a single queue in which the next stage is forbidden until the previous one is complete.

## Fourth question: scientific value and process appropriateness are separate judgments

The truth of a mathematical conclusion cannot decide whether the research process was fair. A model company may demonstrate capability by solving a difficult problem and gain commercial standing from doing so. When the work creates verifiable new knowledge, it can also make a real contribution to science. The further question concerns the cost: whether unpublished human research received consent and isolation, whether contributions were recorded accurately, and whether the party controlling the model, logs, and publication channels used its informational and resource advantages responsibly.

This episode makes the issue concrete. OpenAI acknowledges that its project was triggered by rumors of progress on open problems. Buckmaster had used Codex for unpublished research and communicated directly with the company before its project was announced. OpenAI later stated clearly that those Codex prompts could not have influenced the internal system and that its research team had not seen the relevant work before publication. Buckmaster’s statement explains why he believed the answers and publication arrangements still left questions. Public mathematical materials can address what the formal proof checks; these process claims require access logs, training and evaluation data provenance, timestamps, communications, and an investigation that an independent third party can conduct.

A result may be mathematically correct and scientifically valuable while the process around it still requires governance review. Conversely, a compliant process cannot lend mathematical credit to a false proof. Recognizing a scientific contribution does not endorse the process, and investigating the process does not erase the value of the result. Keeping the judgments separate protects both knowledge and researchers.

Competition is common, and public demonstrations of model capability can advance tools. The problem begins when competition changes researchers’ choices. If researchers fear that unpublished ideas will enter training, evaluation, or adjacent projects, they may stop sharing early work. If a company holds access records, training boundaries, and internal timelines that ordinary users cannot verify, a priority dispute cannot be resolved by public statements alone.

Useful governance must exist before a dispute. Research-facing models should distinguish product improvement, training, internal evaluation, and competing research, and provide an isolation mode that can be checked. Important access and model versions should leave audit records. Starting an adjacent project after contact with unpublished research should trigger conflict registration, internal separation, and publication review. A priority dispute should preserve timestamps, communications, and access logs for confidential independent examination. The point is not to convict either side in advance; it is to make the facts reliably discoverable.

## How the three judgments work together

The same output can carry three statuses at once, and none should overwrite the others:

- **Mathematical status:** the statement, formal theorem, dependency and axiom status, trusted-kernel check, and independent reproduction show where the conclusion holds.
- **Knowledge status:** readable argument, structural explanation, prior work, attribution, teaching, and later questions show how far the result has matured in the community.
- **Process status:** data use, access records, consent, competition rules, and priority procedures show whether the research process can be trusted.

Each question is answered by its own evidence, so the result does not receive a single score. Formal checking can finish first, knowledge transmission can advance at the same time, and process review can proceed independently. A temporary gap in one status should not be exchanged for a denial of the other two.

## What this discussion actually requires

This episode does not require science to choose between machine capability and human knowledge. It requires more precise judgments: give a result that has passed trusted checking the mathematical status and bounded use warranted by its evidence; continue the human work of explanation, attribution, teaching, and structural interpretation; and establish auditable governance rules for processes involving unpublished research and competitive publication.

The position is clear. Mathematical work should be evaluated by the statement, proof, boundary, reproduction evidence, and quality of explanation it actually provides. AI participation should not automatically lower a result’s value, and it should not exempt a result from human reading and knowledge transmission. Correctness, knowledge transmission, and research ethics all matter, but they belong to different chains of judgment. Making one chain a mandatory precondition for another sacrifices precision.

Changes in technological speed need institutional responses and patient community work. The reliable path is to let checkable results enter scientific use in a timely way, while people continue to explain, transmit, and improve them, and while the process that produced them respects collaboration, attribution, and priority.

# ja

> 編集用原稿。ウェブサイトの三言語本文はこのファイルから整えます。この原稿は全体を通読し、論旨を維持するために使います。

## この一週間に何が起きたのか
<!-- aside: opening -->

OpenAI の公開説明によれば、チームは2026年9月1日、二つのミレニアム懸賞問題が解決された可能性があるという噂を聞き、未解決のミレニアム問題と複数の重要問題についてモデル評価を始めました。内部システムがまず外力のない Euler 方程式に関する結果を得たため、チームは Navier–Stokes 問題に資源を集中しました。OpenAI は、システムが9月5日に解析的な解答を形成し、その後17時間で Lean による形式化を終え、9月8日に論文とコードを公開したと述べています。Lean は、形式的な証明手順を比較的小さく反復可能な検査器で確認できる対話型定理証明系です。

Buckmaster の公開文書は研究者側の経験を記録しています。彼は噂と関連情報を受けて9月3日に OpenAI へ連絡しました。9月6日の二度の通話では、内部モデルが、彼らがそれ以前の二か月間に Codex セッションへ入力した未公開研究を閲覧したか、あるいは訓練に利用したかを質問しました。彼によれば、その時点の回答はユーザーデータの直接閲覧には触れましたが、訓練については明確に解消しませんでした。Alpöge と Buckmaster は予定を変更し、9月7日に非圧縮性多孔質媒体方程式、Boussinesq 方程式、非圧縮性 Euler 方程式について三つの有限時間爆発結果と Lean 形式化を前倒しで公開しました。これらは OpenAI の Navier–Stokes 結果とは異なる定理です。

OpenAI は9月10日、Buckmaster が過去二か月に入力した Codex プロンプトが、訓練を含め、内部システムへ影響することはあり得なかったと追記しました。また、Alpöge と Buckmaster の研究が公開される前に、研究者とエージェントがその内容を見ていなかったとも述べています。Buckmaster の文書は、通話での回答、競合研究、公開への圧力、優先権の調整について疑問が残った理由を記しています。公開記録には、過程の証拠によって検討すべき二組の主張が残りました。

9月11日、Terry Tao は25名のフィールズ賞受賞者が署名した「A Severe Misalignment of AI in Mathematics」を公開しました。Tao によれば、この文章は署名者が前週に行った議論から生まれました。共同声明は、著名な未解決問題をモデル能力の競争に用いる現象を数学の長い伝統の中で捉えています。議論、簡略化、丁寧な書き下ろし、先行研究と帰属、教育、証明から概念や新しい問いを抽出する仕事を重視します。その説明では、問題を解くことは概念的理解と洞察へ至るための手段です。数学者が AI による着想を発展させ、数学の伝統へ組み込まなければ、それらの着想は十分に「生きたもの」にならないかもしれない、と述べています。

この共同声明は、直前の出来事と時間的にも主題上も直接つながっていますが、公開文の射程はより広いものです。特定の証明について数学的な裁定を下す審査文ではありません。AI による結果が完全な数学的仕事へ成熟するために必要な、議論、説明、先行研究の中での位置づけ、人間による継続的な発展を示しています。OpenAI は新結果の迅速な発見と形式化を強調し、Buckmaster の記録は未公開資料、直接の連絡、競合する公開、優先権を議論に持ち込みました。三つの文書は同じ週の出来事の異なる側面を示しています。

今回の出来事は三つの時間軸を圧縮しました。証明は数日で生成され形式化され得ます。深い証明を人間が理解するには通常さらに時間がかかります。データ、協力、公開の規則は競争が進んでいる最中から機能しなければなりません。同じ出来事から、結論はどの意味で正しいのか、正しい結論はどう共同知になるのか、結論を生んだ過程は協力と優先権をどう守るべきか、という三つの問いが続いて現れます。

## 第一の問い：結論はどの意味で正しいのか

数学的正しさは精密な対象から始まります。仮定、定義、結論を明示し、論文の主張と形式体系が実際に検査した定理が一項ずつ対応していることを確かめます。信頼できる kernel が明示された仮定から定理までの完全な導出を検査し、すべての依存関係と公理の状態が明確で、独立したチームが検査を再実行できるなら、結論は宣言された境界の中で成立します。kernel は各形式証明項を検査する証明系の小さな中核です。論文と形式対象の対応は人が確認する必要があります。

この判断は、その結論を後続研究の信頼できる前提として使えるかを答えます。知識継承に関するすべての作業が完了したという意味ではありません。読者がなぜその証明経路を取ったのかを理解している必要もありません。説明力、優美さ、研究上の広がりは結果がどこまで進めるかに影響しますが、正確に検証された局所的結論はそのまま残ります。

したがって数学的地位には再検討可能な証拠の連鎖が必要です。精密な命題、完全な形式化、依存関係の版、再現方法を公開し、独立研究者が論文とコードの対応を確認し、検査結果、発見された問題、公理と依存関係の状態、改訂履歴を保存します。形式化を通過すれば、結論の数学的状態には先に答えられます。知識継承と構造的説明にはなお作業が必要です。

## 第二の問い：なぜ知識継承を正しい結果の利用条件にしてはならないのか

ここはこの議論で最も明確な判断です。SAT は、さらに説明の少ない参照点を与えます。特定のブール充足可能性問題について、求解器は人が一行ずつ数学的意味を理解しないほど巨大な証明書を出すことがあります。そのインスタンスが充足不能であることを確かめるとき、独立した検査器が証明書を確認すれば、その結論を受け入れ、プロトコル検証、スケジューリング、有限組合せ研究に利用できます。簡潔な概念的証明を与えず、一般化可能な構造を示さない場合でも、検査可能性はその具体的結論に明確な利用価値を与えます。

形式化された AI 証明は少なくとも同じ基本条件を満たし、通常はさらに、定義、補題、推論手順で構成された完全な形式構造も提示します。長大で、その経路がなぜ働くかを人間がまだ理解していないこともあります。論文の命題、形式定理、すべての依存結果が正確に対応し、信頼できる kernel が証明を受理し、独立したチームが検査を再現できれば、後続研究は宣言された範囲で引用し、呼び出し、前提として利用できます。

この論理は、証明が AI から来たという理由で書き換えられるべきではありません。独立に検査された SAT 証明書が範囲を限定した利用を支えられると認めるなら、形式化され kernel を通った AI 証明にも同じ数学的基準を適用すべきです。AI による結果について、科学的または工学的価値を認める前に、数日以内に概念的説明、教科書化、共同体への継承まで終えるよう求めるなら、出所に基づく追加の障壁になります。これは double standard です。人間が書いた深い証明が公開数日後も理解しにくいとき、私たちは通常、さらに検討と説明が必要だと言います。教科書に入っていないことだけを理由に、その正しさや用途の可能性を否定しません。

現代のポアンカレ予想の証明は、時間尺度を考えるためのよく知られた参照例です。最初の公開から、広く読める説明が形成されるまでには、相当な共同体の検討と書き直しがありました。OpenAI が資料を公開したのは9月8日で、この文章の日付である9月14日まで六日しか経っていません。公開記録には成熟した人間向け説明がまだ示されていません。これは、その日までに公共資料でこの転換が現れていないことだけを示します。人間の著者により長い理解の時間を認めるなら、AI に由来する証明も同じ時間尺度で判断すべきです。

検査済みの結果を利用できると認めることは、知識継承を完了したと宣言することでも、特殊な場合を一般理論へ拡張することでもありません。明示された定義、仮定、検証範囲の下で、引用や呼び出しが可能な価値を持つという意味です。数学的貢献の成熟度は正直に示せます。正しさを出所によって再評価すべきではありません。

## 第三の問い：正しい結論はどう共同知になるのか
<!-- aside: contextual -->

共同声明が重視する知識継承は、数学の核心的な仕事です。定理が共同知になるには、何を解いたかを説明し、先行研究の中に位置づけ、機構と適用範囲を示し、再利用できる手順を明確にし、他の研究者が続けられる言葉を残す必要があります。教育、直観、抽象化、帰属、新しい問いによって、結果は研究グループや世代を越えます。

ここでの補足は、この仕事を正しさと並行して進められる第二の軸として位置づけます。検査済みの結果は境界と成熟度を正確に示した上で、先に公開、引用、利用できます。人間が読める書き直し、構造的解釈、歴史的位置づけ、外部審査、教材はその後も発展します。知識継承は結果の理解、一般化、創造的利用を容易にしますが、正しい結果が数学的地位や範囲を限定した利用価値を得るための事前許可にすべきではありません。

ここでは時間が特に重要です。深い証明が初めて公開されてから、共同体の安定した説明になるまでには、数か月または数年かかることがあります。成熟した公開説明が六日間現れなかったことは、結果が知識を残していないことの証明ではありません。証明がすでに十分理解されたことの証明でもありません。判断は公開証拠が覆う時間範囲に合わせる必要があります。

より完全な知識転換は複数の段階を残します。検査可能な初期結果、人間が読める論文、形式証明と再現記録、公開プレプリント、外部審査による改善、そして後に生まれる総説、教材、新しい研究方向です。機械は発見と形式化を短縮できます。理解、選択、帰属、伝達は数学共同体が引き続き担います。これらは知識継承を構成しますが、前の段階が終わるまで次の段階を禁止する一列の順番である必要はありません。

## 第四の問い：成果の価値と、過程が適切だったかは別の判断である

数学的結論の真偽から、研究過程が公正だったかを決めることはできません。モデル企業は難問を解くことで能力を示し、商業的評価を得ることがあります。検証可能な新知識を生めば、その活動は科学への本当の貢献にもなります。さらに問うべきなのは、その貢献の費用です。未公開の人間の研究に同意と隔離が与えられたか、貢献が正確に記録されたか、モデル、ログ、公開経路を管理する側が情報と資源の優位を責任を持って扱ったかが問題になります。

今回の出来事は問題を具体化しました。OpenAI は、未解決問題の進展に関する噂がプロジェクトの契機だったと認めています。Buckmaster は未公開研究に Codex を使い、プロジェクト公表前に会社と直接連絡していました。OpenAI は後に、それらの Codex プロンプトが内部システムへ影響することはあり得ず、研究チームも公開前に該当研究を見ていなかったと明確に述べました。Buckmaster の文書は、回答と公開調整に疑問が残った理由を説明しています。公開された数学資料は形式証明が何を検査したかを示せます。これらの過程主張には、アクセスログ、訓練・評価データの来歴、タイムスタンプ、通信記録、独立した第三者が実施できる調査が必要です。

結果が数学的に正しく科学的価値を持ちながら、その周囲の過程にガバナンス上の問題が残ることはあり得ます。反対に、完全に適切な協力過程であっても、誤った証明に数学的信用を与えることはできません。科学的貢献を認めることは過程を承認することではなく、過程を調査することは結果の価値を消すことでもありません。判断を分けることで、知識と研究者の双方を守れます。

競争は珍しくなく、モデル能力の公開実演が道具の発展を促すこともあります。問題は、競争が研究者の選択肢を変えるときに始まります。未公開の考えが訓練、評価、隣接プロジェクトに入ることを恐れれば、研究者は初期研究を共有しなくなるかもしれません。企業が一般利用者の確認できないアクセス記録、訓練境界、内部時系列を持つなら、優先権争いは公開声明だけでは解決できません。

有効なガバナンスは紛争より前に必要です。研究用途のモデルには、製品改善、訓練、内部評価、競合研究を区別する明確な規則と、検証可能な隔離モードを設けます。重要なアクセスとモデル版には監査記録を残します。未公開研究との接触後に隣接プロジェクトを始める企業には、利益相反の登録、内部隔離、公開審査を適用します。優先権争いではタイムスタンプ、通信、アクセスログを保全し、独立した第三者が守秘義務の下で検査できるようにします。制度の目的は、どちらか一方を事前に有罪とすることではありません。事実を信頼できる形で明らかにすることです。

## 三つの判断をどう一緒に機能させるか

同じ成果は三つの状態を同時に持つことができ、それらが互いを上書きすることはありません。

- **数学的状態**：命題、形式定理、依存関係と公理の状態、信頼できる kernel の検査、独立再現が、結論の成立範囲を示します。
- **知識の状態**：読める論証、構造的説明、先行研究、帰属、教育、後続の問いが、共同体の中で成果がどこまで成熟したかを示します。
- **過程の状態**：データ利用、アクセス記録、同意、競争規則、優先権手続が、研究過程を信頼できるかを示します。

これは成果に一つの点数を付ける仕組みではありません。各問いには、それぞれの証拠で答えます。形式検証が先に終わっても、知識継承は同時に進められ、過程の審査も独立して進められます。一つの状態に一時的な空白があることを、他の二つの否定に置き換えるべきではありません。

## この議論が実際に求めること

今回の出来事は、科学に機械能力と人間知識のどちらかを選ばせるものではありません。求めているのは、より精密な判断です。信頼できる検査を通った結果には、その証拠が支える数学的地位と範囲を限定した利用価値を与えること。説明、帰属、教育、構造的解釈という人間の仕事を続けること。未公開研究と競合する公開に関わる過程には、監査可能なガバナンス規則を設けることです。

立場は明確です。数学的成果は、実際に示された命題、証明、境界、再現の証拠、説明の質によって評価されるべきです。AI が関与したことだけで価値を自動的に下げるべきではありません。同時に、人間による読解と知識継承から免除されるべきでもありません。正しさ、知識継承、研究倫理はいずれも重要ですが、別々の判断の連鎖に属します。一つの連鎖を別の連鎖の必須条件にすると、議論の精度が失われます。

技術の速度が変われば制度の対応が必要になり、共同体の忍耐強い仕事も必要になります。信頼できる道は、検査可能な結果を適切な時期に科学的利用へ入れながら、人々がそれを説明し、伝え、改善し続け、同時にそれを生んだ過程が協力、帰属、優先権を尊重することです。
