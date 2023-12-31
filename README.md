
# 古文命名实体识别任务

在灿若星河的人类文明中，中国古代典籍承载着悠久的东方文化，是世界文明的瑰宝。命名实体识别（Name Entity Recognition）通过从古籍文本中识别出人名、地名、书名、官职名和朝代等关键信息，将尘封在历史文献中的文本变为可搜索、可分析的结构化数据，在挖掘古籍中的深层知识方面展现出巨大潜力。近年来，学界已经构建了一些古籍命名实体标注数据集，为推动古籍数字化发展具有积极意义，但由于数据集体量小、命名实体标注不一、古代文献勘校困难等问题，可用于模型训练以及评测的公开数据资源较为匮乏。

此次评测由国际语言资源与评测大会LREC2024的国际古代语言处理研讨会（LT4HALA）主办，针对古代汉语的命名实体识别任务在国际上展开统一的评测，致力于综合评价当前学界已有的研究成果，期望能够探讨、发现当前研究的缺陷与不足，并能沟通众高校、研究单位共同推进古代汉语命名实体识别技术的研究进程。

# 01 评测简介

EvaHan2024是目前发布的聚焦于古代汉语命名实体识别评测任务的国际评测。语言的自动分析诸如MUC、SemEval、CoNLL和SIGHAN等在NLP领域已拥有众多较为成熟的评测，但以往大都集中于面向现代汉语的评测任务。因此，本次发布的面向古代汉语命名实体识别评测将是第三次开展的以古代汉语为研究对象的国际评测任务。本次评测主要有两个目标：

* 推动古代汉语资源的挖掘及面向古代汉语的语言技术的发展。
* 促进古代汉语有关领域学者之间的交流与合作，吸引更多学科的研究者共同探究。

我们将会为参赛者提供统一的数据集，参赛者需要完成指定的命名实体识别任务，并在规定时间内向提交至评审组。评审组将在核实数据准确性后，发布最终排名结果。

# 02 评测方法

* 数据说明

本次国际评测组织者将提供两个数据集，即训练集和测试集。训练集包含了人工标注的命名实体。测试集包含两个，仅涉及汉字。一个测试集（TestA）用于同类型古籍文本的评测，另一个测试集（TestB）用于不同类型古籍文本的评测。参赛团队不得将测试集用作训练数据。

评测为命名实体识别任务，包括人名、地名、书名、官职名、朝代等。数据集具体格式示例如下。

<table>
  <tr>
    <td>原始文本</td>
    <td>吳興太守王曇生、義興太守劉延熙、晉陵太守袁標一時響應。</td>
    <td>尚書曰：『眚災肆赦。』此謂過誤為害，罪雖大，當緩赦之。</td>
  </tr>
  <tr>
    <td>命名实体识别结果</td>
    <td>{吳興|LOC}{太守|OFI}{王曇生|PER}、{義興|LOC}{太守|OFI}{劉延熙|PER}、{晉陵|LOC}{太守|OFI}{袁標|PER}一時響應。</td>
    <td>{尚書|BOOK}曰：『眚災肆赦。』此謂過誤為害，罪雖大，當緩赦之。</td>
  </tr>
</table>

评测后，组织方会把测试数据的详细信息提供给参赛者，评测结果则会在评测结束后提供给参赛者。

# 03 重要日程

* 2023 年 12 月 22 日：发布训练数据。
* 2024 年 2 月 14 日：发布测试数据。
* 2024 年 2 月 24 日：公布评测结果。
* 2024 年 3 月 24 日：参赛队提交评测论文。
* 2024 年 3 月 31 日：论文评审截止日期。
* 2024 年 4 月 14 日：参赛者提交论文最终版。

# 04 参赛方式

参赛者仅可通过以下两种方式提交测试数据：

* 在封闭测试模式中，各团队只能使用测试数据 Text_Train 和预训练模型 XunziLLM（[https://github.com/Xunzi-LLM-of-Chinese-classics/XunziALLM](https://github.com/Xunzi-LLM-of-Chinese-classics/XunziALLM)）
* 在开放测试模式下则不限制参赛团队使用的各种资源、数据和模型。各团队可以使用其他外部数据，例如汉字的部首或拼音，并且可以采用字向量或词向量等。需要注意的是，各团队在最终报告中都必须注明他们在每个测试中所使用的全部资源、数据和模型。

# 主办团队

* 王东波（南京农业大学信息管理学院）
* 刘浏（南京农业大学信息管理学院）
* 叶文豪（南京农业大学信息管理学院）
* 张卫（南京农业大学信息管理学院）
* 沈思（南京理工大学经济管理学院）
* 张海（南京农业大学信息管理学院）
* 许乾坤（南京农业大学信息管理学院）
* 吴梦成（南京农业大学信息管理学院）
* 赵雪（南京农业大学信息管理学院）
* 李斌（南京师范大学文学院、语言大数据与计算人文研究中心）
* 常博林（南京师范大学文学院、语言大数据与计算人文研究中心）
* 卢芃秀（南京师范大学文学院、语言大数据与计算人文研究中心）
* 冯敏萱（南京师范大学文学院、语言大数据与计算人文研究中心）
* 许超（南京师范大学文学院、语言大数据与计算人文研究中心）
* 王永吉（南京师范大学文学院、语言大数据与计算人文研究中心）

# 协办单位<small>（排名不分先后）</small>

* 中国人工智能学会语言智能专委会
* 中国古籍保护协会古籍智能开发与利用专委会
* 中国民族语言学会语言资源与计算人文专委会
* 江苏省人工智能学会自然语言处理专委会
