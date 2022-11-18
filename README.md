## “互联网+”金融科技创新竞赛 – 商业银行操作风险自动化管理

**赛事时间：** 2022年11月 – 2023年2月

**赛事背景：** 为顺应以移动互联网为代表的IT技术持续向各领域渗透这一趋势，推动金融科技创新的不断发展，由南京大学工程管理学院和软件学院主办并组织的第一届《互联网+金融科技创新竞赛》正式开赛。本次大赛将为两个学院的各位同学、金融科技研究人员、及包含AI在内移动互联网技术爱好者提供一个良好的交流平台。



### 1. 大赛机构

#### 1.1 主办单位

南京大学工程管理学院

#### 1.2 组织与承办单位

南京大学软件学院



### 2. 参赛办法

#### 2.1 参赛对象

本次竞赛定位为院系内部比赛，面向南京大学软件学院三、四年级本科生与工程管理学院计算机与金融实验班全年级本科生。欢迎各位同学组织队伍申报参赛。

#### 2.2 参赛组织形式

选手可自行组队报名，每支队伍需包含3-5名队员，允许跨年级、跨院系组队。队伍内不允许出现非参赛对象中的其他学校、院系、企业或单位人员。

#### 2.3 报名方式

2022年12月1日前，参赛队伍可通过如下腾讯文档链接 https://docs.qq.com/form/page/DRHplT090U2lxbU5E 进行报名，并将队伍信息发送至如下邮箱 seHelper@outlook.com 完成报名审核。



#### 2.4 参赛选题

##### 2.4.1 竞赛背景

当前国内外金融环境复杂多变，相关法规政策多有调整，涉及的诉讼与处罚频发（即所谓“外规”），这使得商业银行的内部操作流程与规范（即所谓“内规”）需要及时依据“外规”变化进行调整以规避风险（即所谓“外规内化”）。而实践中这一流程往往还依赖于人工完成，费时费力。因此，本赛题从给定时间内新发布的“外规”（包含诉讼判决书与处罚决定书）出发，尝试利用文本处理、信息检索、数据挖掘等技术实现对某商业银行需依据“外规”而进行调整的“内规”的进行自动化分析与管理。



##### 2.4.2 赛题描述

本次赛题选择已确定需按照“外规”进行调整的“内规”作为校对数据，以给定的每一项“外规”作为查询，逐一检索所有给出的“内规”，并按其自动计算出的关联性形成候选列表并从高到低排序。参赛队设计实现的自动化方法应针对给定的某一项“外规”，将需要相应调整的所有“内规”尽可能地排在候选列表的前列，从而使得用户能够尽快从候选列表中逐一确定所有需要调整的“内规”，极大地提升“外规内化”工作的效率，最终更好地应对外部复杂多变的金融环境。具体的“内规”、“外规”输入以及输出的候选列表示例如下：

**被检索文档：**

相关“内规”库，如《案防工作实施办法》、《客户风险预警系统实施细则（试行）》等

**检索输入（新出现的“外规”）：**

```json
{
    "input_fileName":"《中国银保监会有关部门负责人就《银行保险机构信息科技外包风险监管办法》答记者问》",
    "input_text":" 一、制定《办法》的背景和意义是什么？ 答：近几年，银行保险机构积极开展数字化转型，在加大科技创新力度、更好地满足金融消费者需求的同时，对信息科技外包服务的依赖度不断加大。与此同时，部分银行保险机构对信息科技外包风险管控不力，因而导致的业务中断、敏感信息泄露等事件时有发生。此外，部分领域外包服务提供商高度集中，形成了行业集中度风险。为此，按照风险为本的导向，以弥补短板、强化监管为目标，拟通过制定《办法》，从信息科技外包治理、准入、监控评价、风险管理等方面对银行保险机构信息科技外包提出要求。《办法》的制定出台，将促进银行保险机构建立并完善信息科技外包治理架构，加强信息科技外包风险管理体系建设，提升信息科技外包风险管控能力，促进银行保险机构稳健开展数字化转型工作。"
}
```

**检索输出（可能受到影响的“内规”条款）：**

```json
[       
    {
        "similiarity":0.4537525233380211,
        "rule_fileName":"《案防工作实施办法》.docx",
        "rule_text":"第十七条 加强授信风险全流程管理。授信与风险审查岗位分工合理、职责明确，岗位之间相互配合、相互制约，做到审贷分离、业务经办与会计账务处理分离。\n不断完善统一授信管理制度。健全客户信用风险识别与监测体系，不断完善授信决策与审批机制，采取有效措施防止对单一客户、关联企业客户和集团客户授信风险的高度集中，防止违反信贷原则发放关系人贷款和人情贷款，防止信贷资金违规使用。\n",
        "relevance":1
    },
    {
        "similiarity":0.16718170069616375,
        "rule_fileName":"《资本管理办法》.doc",
        "rule_text":"第三十一条 资本规划的主要发展目标：\n（一）稳健的资本充足率水平。本行资本充足率目标的确定，应确保满足内部业务发展需求和外部监管要求。\n（二）不断优化的资本结构。在资本管理过程中，积极优化并保持稳定的资本结构，提高抵御风险能力。\n（三）不断提升的资本运营效率。本行在业务发展过程中，应充分、高效利用资本杠杆功能，加快业务转型发展，提高资本配置效率。\n",
        "relevance":0
    },       
    {
        "similiarity":0.1661873838587476,
        "rule_fileName":"《客户风险预警系统实施细则（试行）》.doc",
        "rule_text":"第一条 为有效推广应用客户风险预警管理系统（以下简称“预警系统”），促进信用风险管理转型，提升信用风险管控质量，制定本细则。\n",
        "relevance":1
    },       
    {
        "similiarity":0.13677256782007713,
        "rule_fileName":"《在建工程抵押贷款管理办法及操作规程》.docx",
        "rule_text":"第三十一条 抵押合同签订后，经办行须要求抵押人到有关保险机构按照下列条件办理抵押在建工程的保险手续：\n（一）办理抵押在建工程足额保险；\n（二）保险期限不得短于合同履行期限；\n（三）保险金额不得小于合同贷款本息；\n（四）保险合同及保险单中应当注明，本行为保险赔偿金的第一受益人；\n（五）保险单中不得有任何限制本行权益的条款；\n（六）抵押在建工程保险费用全部由抵押人承担，保险单证原件应交由经办行保管。\n",
        "relevance":0
    }
]
```

其中“similarity”指通过自动化方法计算出的相似度或关联度（一般在0到1之间），“relevance”是指数据集内已标注的该条“内规”是否与给定的“外规”相关，且后续需要调整。



##### 2.4.3 检索模型构建思路

主办方提供如下解题思路供参赛选手参考，选手可按照如下思路开发检索模型并优化，也可选择其它各类数据挖掘或人工智能方法，思路不限。

**解题思路（仅供参考）：**

- 通过中文文本处理将“外规”和“内规”条款转化为基于关键词的文本向量。

- 利用各类检索模型计算文本向量的相似度并排序

- 可能的优化空间：检索模型计算前的文本增强，以及检索模型计算后的排序优化等

 

##### 2.4.4 训练集数据介绍

主办方将提供初始小批量数据集帮助项目启动，并在后期提供规模约一万句的数据集作为最终的训练与验证集。参赛队在构建方法时可以使用已有的公开数据集或其它开放数据。

**训练集以及后续消息通知将在[此github项目](https://github.com/seHelper2/FinTechNJU2022)下发布**

**现有公开数据集参考：**

司法领域中文检索数据集（王佳麒等人2020年发表的《检务文书检索数据集的构建》）

https://pan.baidu.com/s/1FOXffPnrFOSQd4-1y9zuzg

 

#### 2.5 作品要求

参赛队的参赛内容应是参赛队员独立设计并开发完成的作品，严禁抄袭、剽窃等行为。一旦发现包括抄袭、剽窃在内的竞赛不端行为，大赛组织方将取消参赛队伍的参赛资格，并通报参赛队员所在院系。

 

### 3. 竞赛时间安排

2022.11.16 发布大赛通知，开始报名

2022.11.28 发布示例样本、检索模型基线与小批量伪数据

2022.12.01 报名截止

2022.12.26 公布最终版本数据集与实验结果提交地址

2023.01.16 提交最终实验结果与分析系统

2023.01.18 公布最终进入公开讲演的队伍名单

2023.02  进入公开讲演的队伍于假期撰写报告，开学后公开讲演并颁奖

 

### 4. 竞赛赛制

#### 4.1 整体流程

参赛队需在2022年12月1日前完成报名，并在数据发布后从指定网站获取竞赛启动所需的示例样本、检索模型基线与小批量伪数据，之后即可开始数据处理与自动化方法构建及验证。2022年12月26日将公布最终竞赛所使用的数据集，并允许参赛队在指定网址每周提交或更新一次（仅限一次）实验结果。2023年1月16日为最终的实验结果更新与提交系统更新截止日，参赛队需将自己的最终版系统以项目的形式提交至自己选定的代码提交平台（例：GitHub或Gitee），并将项目网址发送至指定邮箱，该项目内不能有超过2023年1月16日的任何文件更新。

#### 4.2 评测规则

赛事组委会将对参赛队伍提交的自动化检测结果与主办方公布的标准结果进行一致性评估，参赛队伍自身亦可根据公布的数据集随时评估自己系统的分析结果。由于本次“外规内化”自动检测的本质是以“外规”作为查询，“内规”作为被检索对象的排序问题，因此评估指标将采用领域内最常用的多查询检索指标Average Precision（AP）和Mean Average Precision（MAP），并计算二者的调和平均（类似于F-Measure计算）作为最终的单一评估指标。提交截止日后赛事组委会将按照上述评估指标对每支队伍在截止日前最后更新的实验结果进行计算，并按评估指标从高到低排序，最终选取排名前12的队伍进入公开讲演名单。入选的队伍需在后续时间内撰写技术总结报告与讲演ppt，开学后组委会将组织公开讲演并最终确定获奖队伍名单，评奖所依据的最终竞赛分数 = 0.8*排名得分 + 0.2*报告与讲演评分。

#### 4.3 参赛规则

允许使用开源代码、工具以及其它公开数据集，以及参赛队伍自己以往开发且尚未公开的代码和数据集。评奖最终决定权归赛事组委会所有，若拒绝或未在规定时间内提供相应代码、文档，或未参加公开讲演的，组委会将取消该参赛队评奖资格。

 

### 5. 奖项设置

本次赛事最终选出一等奖1队，二等奖2队，三等奖3队，对应如下奖励：

- 一等奖参赛队奖金5000元人民币/队

- 二等奖参赛队奖金3000元人民币/队

- 三等奖参赛队奖金1000元人民币/队

 

### 6. 竞赛管理

本次竞赛仅限南京大学软件学院与工程管理学院特定年级与专业同学参加，赛事组委会拥有对本次赛事的最终解释权。
