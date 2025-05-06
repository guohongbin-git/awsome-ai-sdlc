# **大型语言模型辅助软件开发需求分析过程的进展**

**1\. 引言**

需求分析（RA）在软件开发生命周期（SDLC）中扮演着至关重要的角色，它直接关系到项目的成功与否，并能有效降低项目失败的风险 1。不良的需求是导致项目失败的主要原因之一 2。然而，传统的需求分析过程往往耗时费力，容易出错，并且高度依赖人工的解读和分析 4。大型语言模型（LLM）作为一种变革性技术，展现出彻底改变包括需求分析在内的软件工程多个方面的巨大潜力 6。近年来，研究人员对LLM的兴趣日益增长，其快速发展也深刻影响着自然语言处理（NLP）及跨学科应用领域 13。LLM相关的研究出版物数量在近几年呈现指数级增长 13。需求分析的有效性是软件项目成功的关键，而LLM技术的飞速发展为此领域带来了显著的创新和改进机会。

本报告旨在全面概述当前使用LLM辅助完成软件开发需求分析过程的进展。报告将涵盖LLM在需求工程中不断演变的角色、其在需求获取、分析、规约和建模中的应用、优化技术、面临的挑战、混合方法、相关工具、案例研究、对需求质量的影响、最新研究趋势以及未来的发展方向。

**2\. 大型语言模型在需求工程中不断演变的角色**

LLM预先训练的对自然语言的理解能力使其能够有效地适应特定的需求工程任务 15。LLM有潜力通过自动化诸如需求获取和规约等历来耗时且容易出错的任务，从根本上改进需求工程过程 7。LLM凭借其自然语言处理能力，已成为需求工程中积极的合作伙伴，为需求获取、规约生成、质量保证以及需求的许多其他方面提供自动化支持 7。LLM为需求工程带来了生成式和分析式两种能力 7。这表明，LLM正在从被动的工具转变为需求工程过程中积极的协作者，从而实现更高水平的自动化，并有可能增强人类的专业知识。

在需求工程中，LLM可以分为以下几类：

* **生成式预训练Transformer (GPT):** 包括ChatGPT和GPT-3等模型，已在需求工程中得到广泛应用。这些模型有助于生成需求文档、系统代码和测试用例，从而促进重复性任务的自动化并加速文档编制工作流程 7。例如，ChatGPT已被用于生成需求规约的初始草稿甚至代码片段，这些草稿随后由人类工程师进行完善 7。GPT模型还支持渐进式提示技术，以迭代方式提高生成输出的相关性和特异性 7。  
* **代码聚焦的语言模型 (如Codex):** 专门为编程相关任务而设计。在需求工程中，Codex常用于将自然语言需求直接翻译成可执行代码，从而弥合了高级需求和具体技术实现之间的差距 7。Codex在测试用例生成中也发挥着关键作用，通过基于初始需求输入自动创建测试脚本来帮助验证需求 7。  
* **双向编码器表示 (BERT) 及其变体:** 这些模型具有上下文感知能力，在分析文本需求方面具有显著优势 7。它们通过执行需求分类、冲突检测和关键词提取等任务来支持需求工程 7。  
* **基于Transformer的模型 (如T5, Llama 2):** 将Transformer架构扩展到释义和总结需求等任务，这对于将技术语言转化为更易于不同利益相关者理解的术语至关重要 7。这些模型还能够总结大量的需求文档 7。  
* **多模态模型:** 可以处理文本和视觉数据，特别适用于涉及图表或可视化辅助的需求工程任务，例如用户界面草图和工作流程图 12。通过将视觉资产与基于文本的需求相结合，实现全面的理解和文档编制 12。

LLM的不同架构提供了专门的功能，这些功能可以用于需求工程过程中的不同任务，因此需要根据活动的具体需求采取战略性的模型选择方法。LLM正有效地集成到需求工程的不同阶段，包括需求获取、建模和验证，从而提高准确性和效率 7。

**3\. LLM在需求获取和分析中的应用**

LLM在需求获取方面展现出强大的辅助能力。它们能够帮助识别遗漏的信息，并针对需求的可行性和清晰度提供反馈 7。LLM还可以将用户故事转化为结构化需求，并通过分析利益相关者的输入来促进交互式获取 7。借助人工智能驱动的对话系统，LLM能够提出相关问题并引导利益相关者提供更详细的信息，从而改进反馈和想法的收集过程 17。此外，人工智能工具可以更快、更全面地生成调查问卷或访谈问题列表 17。LLM可以作为协作式头脑风暴伙伴，通过分析复杂的文本和执行市场分析来激发创新性见解并挖掘市场情报 17。它们还可以将来自各种来源的关键点总结成格式清晰的报告 17。对于产品的迭代开发，人工智能可以根据历史使用情况和事件分析提出额外的想法 17。人工智能工具还可以通过快速构建粗略的原型来加速需求获取的最终阶段 17。LLM能够基于自然语言提示生成需求规约的初始草稿 7。这表明，LLM正在增强传统的需求获取技术，通过提供自动化的信息提取、想法生成和初步文档编制能力，有可能减少对人工的依赖并加速需求收集的初始阶段。

在需求分析方面，LLM也显示出巨大的潜力。它们可以用于需求分类、冲突检测和关键词提取 7。LLM还有助于识别和纠正定义不充分的需求 1，并利用LLM和提示模式检测遗漏的需求并最小化需求集合 1。研究表明，LLM在需求获取方面的能力与人类专家相比毫不逊色 18，LLM生成的需求被评估为与参与者的初始想法更加一致，并且可能更完整 18。LLM可以分析最终用户的反馈、对需求进行分类并识别依赖关系 19。它们还可能用于自动化的质量保证、风险识别、冲突协商以及需求变更的影响分析 19。LLM还可以作为一种替代来源，用于注释机器学习实验的数据集 19。将LLM的性能与其他人工智能技术（如SVM和LSTM）在需求分类方面进行比较的研究也已开展 19。此外，LLM还可以分析非功能性需求，以解决非技术利益相关者之间存在的冲突 19。这表明，LLM在自动化和增强需求分析的各个方面（包括分类、冲突检测和质量评估）方面展现出显著的潜力，通常优于或补充了传统的AI方法。

一项研究比较了LLM与人类专家在需求获取方面的表现，发现LLM生成需求的速度（720倍）和成本（仅为人类专家成本的0.06%）都具有显著优势 18。参与者认为LLM生成的需求更加符合他们的想法，但他们倾向于认为更符合想法的解决方案是由人类专家创建的 18。LLM生成的文档也显示出更完整的趋势 18。虽然LLM在需求获取的速度和成本方面提供了显著的优势，但对齐性的感知以及人类理解的细微差别仍然突显了人类专家在此过程中不可替代的作用。

**表 1：LLM 与人类专家在需求获取方面的性能比较**

| 指标 | LLM 生成 | 人类专家生成 |
| :---- | :---- | :---- |
| 对齐性评分 | \+1.12 | 基线 |
| 完整性（更完整） | \+10.2% | 基线 |
| 速度 | 720x | 1x |
| 成本 | 0.06% | 100% |

*数据来源：18*

**4\. LLM在需求规约和建模中的应用**

LLM在生成需求文档方面表现出色。它们有助于生成需求文档、系统代码和测试用例 7。ChatGPT已被用于生成需求规约的初始草稿 7。研究表明，LLM在生成软件需求规约（SRS）方面可以达到初级软件工程师的输出质量 9，并能提供完整且一致的SRS文档草稿，从而显著缩短初级工程师的开发时间 9。LLM还能够识别和纠正给定需求文档中的问题，其中GPT-4在提供建设性反馈方面表现出强大的能力 9。此外，LLM可以在极短的时间内生成结构良好的需求文档 20。这表明，LLM能够显著加速软件需求文档的创建过程，通过生成初始草稿甚至识别潜在问题，将人类专家解放出来，专注于更复杂和细致的方面。

除了文本需求，LLM还有助于创建系统模型。它们可以辅助生成UML图 7，将高级需求转化为正式规约 7，支持规约的生成和验证 7，并通过模型规约提供需求的可视化 7。自然语言处理工具可以促进从文本需求创建概念模型，例如UML图和特征模型 21。这表明，LLM不仅限于文本需求，还可以促进可视化模型和正式规约的创建，从而提高记录需求的清晰度和精确度。

LLM在生成正式规约方面也发挥着作用。它们可以将自然语言规约翻译成正式代码或领域特定语言（DSL）7，检查语法和语义的正确性 7，并协助调试和修复规约 7。SpecGen项目专注于利用大型语言模型自动生成正式的程序规约 22。这表明，LLM可以在自然语言需求和正式规约或代码之间架起桥梁，从而有可能实现更严格的验证过程。

**表 2：LLM 在需求工程阶段的应用示例**

| 需求工程阶段 | LLM 应用示例 |
| :---- | :---- |
| 需求获取 | 识别遗漏信息，提供可行性和清晰度反馈，分析利益相关者输入，生成访谈问题和调查问卷，进行头脑风暴 |
| 需求规约 | 生成需求文档初稿，创建软件需求规约（SRS），识别和纠正需求问题 |
| 需求建模 | 生成UML图，将高级需求转化为正式规约，提供需求可视化 |
| 需求形式化 | 将自然语言规约翻译成正式代码或DSL，检查语法和语义正确性，协助调试和修复规约 |

*数据来源：7*

**5\. LLM在需求工程中的优化技术**

微调技术对于使LLM的输出与需求工程的要求对齐至关重要。诸如低秩自适应（LoRA）和提示调优等参数高效方法已被证明非常有效 7，能够以更高的相关性和准确性处理复杂的规约 7。对于更复杂的任务，则采用全量微调 7。使用特定于领域的數據对LLM进行微调可以提高其性能 7。这表明，使用LoRA和提示调优等技术对LLM进行微调，可以使其适应需求工程的特定细微差别和标准，从而在不需要大量重新训练的情况下提高生成输出的质量和相关性。

提示工程技术也至关重要。少样本和迭代提示是为LLM构建结构化输入的重要技术，可以产生符合需求工程标准的响应 7。诸如少样本提示、迭代提示和上下文提示等技术对于引导LLM的响应并提高需求工程任务的输出质量至关重要 7。提示工程是产生能够从LLM中获得最准确和相关输出的输入艺术 24。这表明，提示的设计和使用方式显著影响着LLM在需求工程中的有效性，而少样本和迭代提示等技术对于实现期望的结果至关重要。

**6\. LLM在需求分析中面临的挑战和局限性**

尽管LLM取得了显著的进步，但在需求分析领域仍然面临着一些挑战和局限性。LLM可能难以理解特定领域的语言细微之处 7，并且存在产生看似合理但不真实信息的“幻觉”现象 6。它们也可能难以理解各种需求工程环境中的复杂依赖关系 7。此外，LLM生成输出的质量和完整性也存在问题 7，并且在处理结构化输入方面存在技术和程序上的限制，导致输出中出现不一致和错误 7。在与需求相关的代码和测试任务中，也存在特定的困难 7，并且为复杂的RE任务构建有效的提示可能具有挑战性 7。LLM还可能延续甚至放大训练数据中存在的偏见 6。使用敏感数据作为LLM的提示也存在安全和隐私方面的风险，包括潜在的数据泄露 6。LLM有时可能无法完成对人类来说简单的任务，使其行为具有不可预测性 27。LLM的输出通常需要人类专家的审查和验证 10。这表明，尽管LLM取得了进展，但在需求分析方面仍然面临着重大的挑战，尤其是在处理现实世界软件项目的复杂性方面，因此需要仔细考虑它们的局限性以及制定缓解策略的必要性。

**7\. 混合方法与人机协作**

为了提高LLM生成输出的可靠性和准确性，将LLM与传统需求工程工具相结合的混合方法正在兴起 7。同时，强调人工评估和整合LLM输出的人机协作系统也变得越来越重要 7。一种建议的模型是将LLM作为“初稿代理”，生成初始草稿，然后由人类专家进行验证和完善 18。研究人员呼吁将重点从炒作转向利用社区的分析技能和对技术复杂性的理解，并以人为本的角度研究如何为LLM进行需求工程 10。LLM由于处理了大量的文本，可以发现人类可能忽略的联系并提供独特的视角 10。用户需要时间来适应人工智能的辅助，并理解LLM响应的非确定性 3。尽管LLM可以提供帮助，但人类在制定需求方面的参与是不可替代的，其输出必须经过人类利益相关者的仔细审查和验证 23。这表明，LLM在需求分析中最有效的集成可能涉及一种协作方法，即LLM处理可自动化且可能繁琐的任务，而人类专家则提供关键的领域知识、批判性思维和验证，以确保需求的质量和准确性。

**8\. 集成LLM的需求管理工具和平台**

越来越多的专业工具和成熟平台正在集成LLM功能，以简化和增强需求管理的各个方面。这些工具提供从自动生成到质量分析以及与现有工作流程集成的一系列功能 30。

* **人工智能驱动的需求管理工具：** Copilot4DevOps、aqua、Notion、Tara AI、IBM Engineering Requirements Management和WriteMyPrd等工具正在集成人工智能功能，用于各种需求工程任务 30。  
* **具体功能包括：**  
  * **需求生成：** 从语音提示、媒体文件或自然语言描述生成需求 30。  
  * **重复项删除：** 识别并删除重复的需求 30。  
  * **测试用例生成：** 从需求自动创建测试用例 30。  
  * **需求审查：** 基于INCOSE等指南进行人工智能驱动的错误纠正和质量保证审查 30。  
  * **洞察和分析：** 基于团队工作流程提供洞察并提出改进建议 30。  
  * **总结和组织：** 总结产品会议并组织需求 30。  
  * **与开发平台集成：** 与Azure DevOps和Jira等工具无缝集成 20。  
* **ScopeMaster：** 自2017年以来一直应用人工智能的商业自动化软件需求分析工具 34。其功能包括积压分析、自动化规模估算、改进用户故事和自动生成功能测试 34。  
* **Altium 365 的需求和系统门户：** 提供人工智能辅助自动化功能，用于将需求分解为电气规范、生成和改进需求、查找不一致性以及进行质量评估 36。  
* **Jama Connect Advisor™：** 使用自然语言处理技术指导系统工程师根据INCOSE和EARS标准创建有效的需求规范 37。  
* **ClickUp：** 项目管理工具，具有人工智能驱动的功能，用于起草需求文档、总结利益相关者的输入和生成行动项 31。

**表 3：人工智能驱动的需求管理工具概览**

| 工具名称 | 主要人工智能特性 | 亮点 |
| :---- | :---- | :---- |
| Copilot4DevOps | 生成式人工智能需求管理 | 自动从原始数据提取高质量需求，生成用例和用户故事，进行影响和风险评估 |
| aqua | 全功能人工智能需求和测试用例管理 | 从语音笔记和媒体文件创建需求，自动生成测试用例，删除重复项 |
| Notion | 人工智能需求处理 | 简化需求创建，总结产品会议，突出行动项 |
| Jama Connect Advisor™ | 基于自然语言处理的需求规范指导 | 根据INCOSE和EARS标准指导创建有效的需求规范 |
| Altium 365 | 人工智能辅助需求自动化 | 快速将需求分解为电气规范，生成和改进需求，查找不一致性，进行质量评估 |

*数据来源：30*

**9\. 案例研究与实际应用**

在需求分析和相关任务中使用LLM的案例研究表明，其在节省时间、降低成本、提高质量和效率方面具有多样化的应用和切实的益处。例如，针对大学学生俱乐部管理门户网站生成SRS的案例研究表明，LLM可以生成与初级工程师相当的完整且一致的草稿 9。First Line Software开发的AI分解（AiD）工具利用OpenAI API将需求分解为用户故事和验收标准，从而节省了时间和成本 39。在复杂领域中使用AI进行需求分析的案例研究（使用HaivenTM）显示了提高质量、速度和团队效率的潜力，并强调了上下文的重要性 3。一家领先的IT咨询公司实施了一个AI聊天机器人进行初步的客户访谈，从而减少了人工工作量并加快了项目启动日期 40。ArgonDigital的AI可以分析文档、代码或用户界面以提取详细的需求，即使在文档不完整的情况下也是如此 8。gpt-engineer是一个开源项目，LLM可以分析高级需求并构建软件，包括创建多人蛇游戏的案例研究 23。医学招生中LLM辅助的社会经济背景分析用例展示了LLM从文本中提取和分析特定类型信息的能力 41。金融服务公司使用定制的LLM来显著缩短网络安全法规与策略和控制的映射时间 42。为理赔员实施生成式AI知识库可以加快处理速度并提升客户体验 42。使用LLM确定常见的客户投诉和有价值的功能，从而实现数据驱动的产品开发和营销决策 42。半导体公司利用LLM摄取知识库文章并提供定制化的响应，从而提高客户服务效率 42。GitHub Copilot提供的实时代码建议可以提高开发人员的生产力 42。训练小型LLM检测命令行中的混淆可以改进网络安全 42。使用在公司数据上训练的LLM可以扩展客户服务能力并提高客户满意度 42。

**10\. LLM对软件需求质量的影响**

LLM有潜力提高需求规约的精确度并减少歧义 7。人工智能驱动的工具可以帮助创建清晰、全面且可测试的需求 44。人工智能工具可以分析需求以检测不一致性并建议改进方法 20。LLM可以帮助检测书面需求的质量并根据各种写作标准（例如良好沟通的6C原则）对其进行分析 2。使用人工智能进行需求分析可能会更好地实现用户故事的“完成定义”3，并且在测试期间发现的遗漏需求也会更少 3。LLM在生成SRS文档方面的输出质量可以与初级软件工程师的水平相当 9。然而，LLM可能产生幻觉，导致软件开发中出现不清晰或不正确的指令 6。LLM输出的质量高度依赖于训练数据的质量和偏差 6。评估LLM输出的质量至关重要，因为并不总存在唯一的正确答案，而且人类可能无法识别超人的输出 10。虽然LLM可以加快工作速度，但如果管理不当，也可能导致项目早期出现更多错误 10。这表明，LLM有潜力通过提高清晰度、完整性和一致性来显著提高软件需求的质量，但它们对训练数据的依赖以及产生幻觉的风险需要仔细验证和人工监督，以确保准确性并防止潜在的错误。

**11\. 最新研究趋势与未来方向**

当前的研究正在积极解决LLM在需求分析中的局限性，并探索其集成的新途径，重点是改进评估、调整、提示和促进有效的人机协作。未来研究需要继续开发更有效的指标来评估LLM在RE任务中的性能 7，进一步改进使用特定于不同软件开发领域的数据对LLM进行调整 7，探索和完善提示工程方法以更好地指导LLM完成RE任务 7，并进一步研究将LLM与传统RE工具和方法相结合的混合方法 7。此外，还需要解决与LLM在RE过程中可靠性和一致性相关的挑战 7，开发人机任务委派框架 45，并在类似现实世界的环境中验证LLM 45。研究还需要解决组织采用LLM的障碍 45，并将重点转向如何有效地利用LLM的能力进行需求工程 10，探索LLM在敏捷方法中需求优先级排序的应用 46，开发针对特定RE任务定制的LLM 23，并解决LLM中的伦理问题，确保负责任地使用人工智能 24。

**12\. 结论**

目前，利用LLM进行需求分析已取得显著进展，其在需求获取、分析、规约和建模等关键环节展现出巨大的潜力。LLM有望通过自动化任务、提高精度和增强效率来彻底改变需求工程过程，从而缩短开发周期并提升软件质量。然而，我们也必须认识到LLM并非完美无缺，它们在处理领域特定语言、理解复杂依赖关系以及避免产生“幻觉”等方面仍然面临挑战。因此，未来软件开发需求分析的有效实施将依赖于混合方法，即结合LLM的自动化能力与人类专家的领域知识和批判性思维。持续的研究对于完善评估指标、优化模型调优、改进提示工程以及解决伦理考量至关重要。通过积极应对挑战并促进人机协作，我们可以充分释放LLM在软件开发领域的潜力，迈向更高效、更高质量的软件交付未来。

#### **引用的著作**

1. Using Large Language Models in Software Requirements Analysis \- IDEAS/RePEc, 访问时间为 五月 6, 2025， [https://ideas.repec.org/a/ajp/edwast/v9y2025i3p856-863id5357.html](https://ideas.repec.org/a/ajp/edwast/v9y2025i3p856-863id5357.html)  
2. AI in Requirements Management: The Ultimate Guide to Mastering It ..., 访问时间为 五月 6, 2025， [https://www.modernrequirements.com/blogs/ai-in-requirements-management-everything-you-need-to-know/](https://www.modernrequirements.com/blogs/ai-in-requirements-management-everything-you-need-to-know/)  
3. Using AI for requirements analysis: A case study | Thoughtworks United States, 访问时间为 五月 6, 2025， [https://www.thoughtworks.com/en-us/insights/blog/generative-ai/using-ai-requirements-analysis-case-study](https://www.thoughtworks.com/en-us/insights/blog/generative-ai/using-ai-requirements-analysis-case-study)  
4. A Systematic Literature Review on Using Natural Language Processing in Software Requirements Engineering \- MDPI, 访问时间为 五月 6, 2025， [https://www.mdpi.com/2079-9292/13/11/2055](https://www.mdpi.com/2079-9292/13/11/2055)  
5. \[2408.10886\] Leveraging LLMs for the Quality Assurance of Software Requirements \- arXiv, 访问时间为 五月 6, 2025， [https://arxiv.org/abs/2408.10886](https://arxiv.org/abs/2408.10886)  
6. Revolutionizing Software Development With Large Language Models \- Forbes, 访问时间为 五月 6, 2025， [https://www.forbes.com/councils/forbestechcouncil/2024/03/20/revolutionizing-software-development-with-large-language-models/](https://www.forbes.com/councils/forbestechcouncil/2024/03/20/revolutionizing-software-development-with-large-language-models/)  
7. Research directions for using LLM in software requirement engineering: a systematic review, 访问时间为 五月 6, 2025， [https://www.frontiersin.org/journals/computer-science/articles/10.3389/fcomp.2025.1519437/full](https://www.frontiersin.org/journals/computer-science/articles/10.3389/fcomp.2025.1519437/full)  
8. How We Use AI to Write Requirements \- ArgonDigital | Making Technology a Strategic Advantage, 访问时间为 五月 6, 2025， [https://argondigital.com/blog/general/how-we-use-ai-to-write-requirements/](https://argondigital.com/blog/general/how-we-use-ai-to-write-requirements/)  
9. Using LLMs in Software Requirements Specifications: An Empirical Evaluation \- arXiv, 访问时间为 五月 6, 2025， [https://arxiv.org/html/2404.17842v1](https://arxiv.org/html/2404.17842v1)  
10. Requirements Engineering and Large Language Models: Insights ..., 访问时间为 五月 6, 2025， [https://www.computer.org/csdl/magazine/so/2024/02/10452860/1UUuUj45692](https://www.computer.org/csdl/magazine/so/2024/02/10452860/1UUuUj45692)  
11. Unifying the Perspectives of NLP and Software Engineering: A Survey on Language Models for Code \- OpenReview, 访问时间为 五月 6, 2025， [https://openreview.net/pdf?id=hkNnGqZnpa](https://openreview.net/pdf?id=hkNnGqZnpa)  
12. Research directions for using LLM in software requirement engineering: a systematic review, 访问时间为 五月 6, 2025， [https://www.frontiersin.org/articles/10.3389/fcomp.2025.1519437](https://www.frontiersin.org/articles/10.3389/fcomp.2025.1519437)  
13. Analyzing 16,193 LLM Papers for Fun and Profits \- arXiv, 访问时间为 五月 6, 2025， [https://arxiv.org/html/2504.08619v3](https://arxiv.org/html/2504.08619v3)  
14. Analyzing 16,193 LLM Papers for Fun and Profits \- arXiv, 访问时间为 五月 6, 2025， [https://www.arxiv.org/pdf/2504.08619](https://www.arxiv.org/pdf/2504.08619)  
15. arxiv.org, 访问时间为 五月 6, 2025， [https://arxiv.org/abs/2402.13823\#:\~:text=Large%20Language%20Models%20(LLMs)%20are,them%20to%20specific%20RE%20tasks.](https://arxiv.org/abs/2402.13823#:~:text=Large%20Language%20Models%20\(LLMs\)%20are,them%20to%20specific%20RE%20tasks.)  
16. arxiv.org, 访问时间为 五月 6, 2025， [https://arxiv.org/abs/2402.13823](https://arxiv.org/abs/2402.13823)  
17. Role of AI in requirements engineering \- Xray Blog, 访问时间为 五月 6, 2025， [https://www.getxray.app/blog/ai-in-requirements-engineering](https://www.getxray.app/blog/ai-in-requirements-engineering)  
18. arxiv.org, 访问时间为 五月 6, 2025， [https://arxiv.org/abs/2501.19297](https://arxiv.org/abs/2501.19297)  
19. (PDF) Large Language Model for Requirements Engineering: A ..., 访问时间为 五月 6, 2025， [https://www.researchgate.net/publication/386905816\_Large\_Language\_Model\_for\_Requirements\_Engineering\_A\_Systematic\_Literature\_Review](https://www.researchgate.net/publication/386905816_Large_Language_Model_for_Requirements_Engineering_A_Systematic_Literature_Review)  
20. How AI is Transforming Requirements Gathering and Documentation \- Copilot4DevOps, 访问时间为 五月 6, 2025， [https://copilot4devops.com/ai-in-requirements-gathering-and-documentation/](https://copilot4devops.com/ai-in-requirements-gathering-and-documentation/)  
21. Natural Language Processing for Requirements Engineering, 访问时间为 五月 6, 2025， [https://www.modernanalyst.com/Resources/Articles/tabid/115/ID/6268/Natural-Language-Processing-for-Requirements-Engineering.aspx](https://www.modernanalyst.com/Resources/Articles/tabid/115/ID/6268/Natural-Language-Processing-for-Requirements-Engineering.aspx)  
22. FudanSELab/Agent4SE-Paper-List: Repository for the ... \- GitHub, 访问时间为 五月 6, 2025， [https://github.com/FudanSELab/Agent4SE-Paper-List](https://github.com/FudanSELab/Agent4SE-Paper-List)  
23. Requirements are All You Need: From Requirements to Code with LLMs \- arXiv, 访问时间为 五月 6, 2025， [https://arxiv.org/html/2406.10101v1](https://arxiv.org/html/2406.10101v1)  
24. Product Lifecycle Management in Software Development using Large Language Models, 访问时间为 五月 6, 2025， [https://www.calsoftinc.com/blogs/product-lifecycle-management-in-software-development-using-large-language-models.html](https://www.calsoftinc.com/blogs/product-lifecycle-management-in-software-development-using-large-language-models.html)  
25. NLPCC 2024 Tutorials, 访问时间为 五月 6, 2025， [http://tcci.ccf.org.cn/conference/2024/tutorials.php](http://tcci.ccf.org.cn/conference/2024/tutorials.php)  
26. LLM Observability Tools: 2025 Comparison \- lakeFS, 访问时间为 五月 6, 2025， [https://lakefs.io/blog/llm-observability-tools/](https://lakefs.io/blog/llm-observability-tools/)  
27. LLMs are fundamentally incapable of doing software engineering. : r/ChatGPTCoding \- Reddit, 访问时间为 五月 6, 2025， [https://www.reddit.com/r/ChatGPTCoding/comments/1ip7yhf/llms\_are\_fundamentally\_incapable\_of\_doing/](https://www.reddit.com/r/ChatGPTCoding/comments/1ip7yhf/llms_are_fundamentally_incapable_of_doing/)  
28. Leveraging Requirements Elicitation through Software Requirement Patterns and LLMs (REFSQ 2025 \- Research Track), 访问时间为 五月 6, 2025， [https://2025.refsq.org/details/refsq-2025-research-papers/27/Leveraging-Requirements-Elicitation-through-Software-Requirement-Patterns-and-LLMs](https://2025.refsq.org/details/refsq-2025-research-papers/27/Leveraging-Requirements-Elicitation-through-Software-Requirement-Patterns-and-LLMs)  
29. Requirements are All You Need: From Requirements to Code with LLMs \- ResearchGate, 访问时间为 五月 6, 2025， [https://www.researchgate.net/publication/381470946\_Requirements\_are\_All\_You\_Need\_From\_Requirements\_to\_Code\_with\_LLMs](https://www.researchgate.net/publication/381470946_Requirements_are_All_You_Need_From_Requirements_to_Code_with_LLMs)  
30. 5 Best AI Tools for Requirements Management \- aqua cloud, 访问时间为 五月 6, 2025， [https://aqua-cloud.io/ai-tools-for-requirements-management/](https://aqua-cloud.io/ai-tools-for-requirements-management/)  
31. Top 10 AI Tools for Requirements Gathering Success in 2025, 访问时间为 五月 6, 2025， [https://clickup.com/blog/ai-tools-for-requirements-gathering/](https://clickup.com/blog/ai-tools-for-requirements-gathering/)  
32. 5 Best AI-powered Requirements Management Tools for Business Analysts, 访问时间为 五月 6, 2025， [https://copilot4devops.com/5-ai-tools-for-requirements-management/](https://copilot4devops.com/5-ai-tools-for-requirements-management/)  
33. Jira Requirements Management 101: Strategies and Tools \- Deviniti, 访问时间为 五月 6, 2025， [https://deviniti.com/blog/application-lifecycle-management/manage-requirements-in-jira/](https://deviniti.com/blog/application-lifecycle-management/manage-requirements-in-jira/)  
34. ScopeMaster \- AI Software Requirements Analysis, QA and Sizing, 访问时间为 五月 6, 2025， [https://www.scopemaster.com/](https://www.scopemaster.com/)  
35. Requirements Elicitation \- Boosted with AI \- ScopeMaster, 访问时间为 五月 6, 2025， [https://www.scopemaster.com/blog/requirements-elicitation-boosted/](https://www.scopemaster.com/blog/requirements-elicitation-boosted/)  
36. Requirements & Systems Portal | Altium 365, 访问时间为 五月 6, 2025， [https://www.altium365.com/capabilities/requirements-systems-portal](https://www.altium365.com/capabilities/requirements-systems-portal)  
37. Leveraging Artificial Intelligence in Requirements Management \- Jama Software, 访问时间为 五月 6, 2025， [https://www.jamasoftware.com/blog/leveraging-artificial-intelligence-in-requirements-management/](https://www.jamasoftware.com/blog/leveraging-artificial-intelligence-in-requirements-management/)  
38. How to Plan for Large Language Model (LLM) Adoption Within Your Engineering Organization \- Jama Software, 访问时间为 五月 6, 2025， [https://www.jamasoftware.com/blog/blog-how-to-plan-for-large-language-model-llm-adoption-within-your-engineering-organization/](https://www.jamasoftware.com/blog/blog-how-to-plan-for-large-language-model-llm-adoption-within-your-engineering-organization/)  
39. AI Tool Saving Time on Requirements Analysis and Documentation, 访问时间为 五月 6, 2025， [https://firstlinesoftware.com/case-study/ai-tool-saves-time-on-requirements-analysis-and-documentation/](https://firstlinesoftware.com/case-study/ai-tool-saves-time-on-requirements-analysis-and-documentation/)  
40. How AI is automating requirement gathering in 2024 \- IoT Tech News, 访问时间为 五月 6, 2025， [https://iottechnews.com/news/how-ai-is-automating-requirement-gathering-in-2024/](https://iottechnews.com/news/how-ai-is-automating-requirement-gathering-in-2024/)  
41. Use Case 3: LLM-Assisted Socioeconomic Context Analysis | AAMC, 访问时间为 五月 6, 2025， [https://www.aamc.org/about-us/mission-areas/medical-education/responsible-ai-medical-school-and-residency-selection/use-case-3-llm-assisted-socioeconomic-context-analysis](https://www.aamc.org/about-us/mission-areas/medical-education/responsible-ai-medical-school-and-residency-selection/use-case-3-llm-assisted-socioeconomic-context-analysis)  
42. Successful Real-World Use Cases For LLMs (And Lessons They Teach) \- Forbes, 访问时间为 五月 6, 2025， [https://www.forbes.com/councils/forbestechcouncil/2024/03/07/successful-real-world-use-cases-for-llms-and-lessons-they-teach/](https://www.forbes.com/councils/forbestechcouncil/2024/03/07/successful-real-world-use-cases-for-llms-and-lessons-they-teach/)  
43. Research Directions for Using LLM in Software Requirement Engineering: A Systematic Review \- Frontiers, 访问时间为 五月 6, 2025， [https://www.frontiersin.org/journals/computer-science/articles/10.3389/fcomp.2025.1519437/abstract](https://www.frontiersin.org/journals/computer-science/articles/10.3389/fcomp.2025.1519437/abstract)  
44. AI Tools to Support Requirements Engineering & Test Case Developments, 访问时间为 五月 6, 2025， [https://specinnovations.com/blog/ai-tools-to-support-requirements-engineering-and-test-case-developments](https://specinnovations.com/blog/ai-tools-to-support-requirements-engineering-and-test-case-developments)  
45. Enhancing Requirements Engineering Practices Using Large Language Models \- Gupea, 访问时间为 五月 6, 2025， [https://gupea.ub.gu.se/handle/2077/83054](https://gupea.ub.gu.se/handle/2077/83054)  
46. Prioritizing Software Requirements Using Large Language Models \- arXiv, 访问时间为 五月 6, 2025， [https://arxiv.org/html/2405.01564v1](https://arxiv.org/html/2405.01564v1)