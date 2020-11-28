# Seminar Template
LaTeX-Template for seminar papers

# TODO
- 重新製圖

# 1. Introduction

The rest of the paper is structured as follows: Data Quality Fundamentals, Related Works, Evaluation and Conclusion.

For the first section, the fundamental of data quality are introduced, which include
an overview of data quality and their attributes and classification of data quality assessment methods.   
In second section, literature review of five data quality assessment are presented and important concept from different paper are explained in brief. 
In the third part, evaluation on these five methods is performed in terms of steps, process, strategies, techniques, cost and performance.
In the end of paper, a conclusion is made based on evaluation result in the context of CI/CD application in software engineering. 
The proposed method, future work and challenges are discussed in brief.

# 2. Data Quality Fundamentals

The section introduces the basic data quality issues common to all methodologies, which represent the perspectives used in this article for comparative analysis such as:
(1) the methodological phases and steps, 
(2) the strategies and techniques, 
(3) the data quality dimensions, 
(4) the types of data

- 2.1. Common Phases and Steps

In the most general case, the sequence of activities of a data quality methodology is composed of three phases:
(1) State reconstruction, which is aimed at collecting contextual information on orga- nizational processes and services, data collections and related management proce- dures, quality issues and corresponding costs; this phase can be skipped if contextual information is available from previous analyses.
(2) Assessment/measurement, which measures the quality of data collections along rel- evant quality dimensions; the term measurement is used to address the issue of measuring the value of a set of data quality dimensions. The term assessment is used when such measurements are compared to reference values, in order to enable a diagnosis of quality. The term assessment is adopted in this article, consistent with the majority of methodologies, which stress the importance of the causes of poor data quality.
(3) Improvement concerns the selection of the steps, strategies, and techniques for reaching new data quality targets.
**_（把phases跟steps製圖）_**
The steps of the assessment phase are:
—data analysis, which examines data schemas and performs interviews to reach a
complete understanding of data and related architectural and management rules;
—DQ requirements analysis, which surveys the opinion of data users and administra- tors to identify quality issues and set new quality targets;
—identification of critical areas, which selects the most relevant databases and data flows to be assessed quantitatively;
—process modeling, which provides a model of the processes producing or updating data;
—measurement of quality, which selects the quality dimensions affected by the quality issues identified in the DQ requirements analysis step and defines corresponding metrics; measurement can be objective when it is based on quantitative metrics, or subjective, when it is based on qualitative evaluations by data administrators and users.


Note that in all the steps of the assessment phase, a relevant role is played by meta- data that store complementary information on data for a variety of purposes, including data quality. Metadata often provide the information necessary to understand data and/or evaluate them.

- 2.2. Strategies and Techniques
- 2.3. Dimensions
- 2.4. Costs
- 2.5. Types of Data
- 2.6. Types of Information Systems


## 2.2 Strategies and Techniques

### 2.2.2 Strategies

### 2.2.1 Techniques

## Data Type

The ultimate goal of a DQ methodology is the analysis of data that, in general, describe real world objects in a format that can be stored, retrieved, and processed by a software procedure, and communicated through a network. 
In the field of data quality, most authors either implicitly or explicitly distinguish three types of data:

- Structured data, is aggregations or generalizations of items described by elementary attributes defined within a domain. 
Domains represent the range of values that can be assigned to attributes and usually correspond to elementary data types of programming languages, such as numeric values or text strings. 
Relational tables and statistical data represent the most common type of structured data.

- Unstructured data, is a generic sequence of symbols, typically coded in natural language. 
Typical examples of unstructured data are a questionnaire containing free text answering open questions or the body of an e-mail.

- Semistructured data, is data that have a structure which has some degree of flex- ibility. Semistructured data are also referred to as schemaless or self-describing. 
 XML is the markup language commonly used to represent semistructured data. 
 Some common charac- teristics are: 
 (1) data can contain fields not known at design time; for instance, an XML file does not have an associated XML schema file; 
 (2) the same kind of data may be represented in multiple ways; for example, a date might be represented by one field or by multiple fields, even within a single data set; and 
 (3) among the fields known at design time, many fields will not have values.
 
 
 Data quality techniques become increasingly complex as data lose structure. For ex- ample, let us consider a registry describing personal information such as Name, Surname, Region, and StateOfBirth. Figure 2 shows the representation of Mr. Patrick Metzisi, born in the Masai Mara region in Kenya, by using a structured (Figure 2(a)), unstruc- tured (Figure 2(b)), and semistructured (Figure 2(c)) type of data. The same quality dimension will have different metrics according to the type of data. For instance, syn- tactic accuracy is measured as described in Section 2.3 in the case of structured data. With semistructured data, the distance function should consider a global distance re- lated to the shape of the XML tree in addition to the local distance of fields.
 The large majority of research contributions in the data quality literature focuses on structured and semistructured data. For this reason, although we acknowledge the relevance of unstructured data, this article focuses on structured and semistructured data.
 
 ![avatar](figures/DataType.png) 
 Different representations of the same real-world object.

## Data Quality Dimensions
Framework
 ![avatar](figures/TwoLayerStandard.png) 
 ![avatar](figures/HierarchicalFrameWork.png) 
 ![avatar](figures/TwoLayerStandard.png)

- Accessibility
- Timeliness
- Authorization
- Credibility
- Definition/Documentation
- MetaData
- Accuracy
- Consistency
- Integrity
- Completeness
- Auditability
- Fitness
- Readability
- Structure

## Data Quality Problems
 ![avatar](figures/2DataQualityProblem.png)
 As the paper is aiming at classifying DQ assessment methods in the context of relational databases, this
 research focuses on the data perspective problems for both context dependent and independent categories and uses the classification of DQ problems identified in [5] (see Table 1). Hence, we provide a brief definition for each DQ problem in the context of our research in the following. In the context independent category, spelling errors, missing data, and incorrect values are self-explanatory DQ problems. Duplicate data problems occur when rows are duplicated or when schemas contain redundancies (that is, specify duplicate attributes in multiple databases). Data format problems occur when two or more semantically equivalent data values have different representations (this includes inconsistent and text formatting DQ problems). Syntax violation problems occur when a pre-specified format has been assigned to an attribute and a data value for this attribute does not adhere to this format (this includes the incomplete data format DQ problem in Table 1). Problems with violations of integrity constraints arise when data values do not adhere to pre-specified database integrity constraints; we also therefore include unique value violations, rather than have these as a separate problem, because unique value violations are one type of database integrity constraint. Note that, despite its position in Table 1, we treat outdated data to be a user perspective problem because whether data is out of date depends on the purpose it is used for.
 For the context dependent category, the problem of violation of domain constraints is when an attribute value must be in a pre-specified context-dependent domain of values. Violation of organizational business rules is when any set of values do not adhere to a pre-specified rules assigned by the organization. Violation of company and governmental regulations is when any set of values do not adhere to a pre- specified rules assigned imposed on the organization by legislating bodies. Similarly, violation of constraints provided by the database administrator is when any set of values do not adhere to a pre- specified rules assigned by the database administrator.
 
 ## Techniques
 
 - Column analysis: Number of (unique) values and the number of instances per value as percentage from the total number of instances in that column
 - Cross-domain analysis
 - Data validation
 - Domain analysis
 - Lexical analysis
 - Matching algorithms: identify duplicates
 - Primary key and foreign key analysis (PK/FK analysis) : are good candidates for a PK/FK
 - Schema matching: two attributes are semantically equivalent
 - Semantic profiling
 
# Literature Review

In this section, 3~5 data quality assessment methods are introduced in brief:

## Total Data Quality Management(TDQM)
 ![avatar](figures/PhasesTDQM.png)
 
- General description: The TDQM methodology was the first general methodology published in the data quality literature [Wang 1998]. 
 TDQM is the outcome of academic research, but has been extensively used as a guide to organizational data reengineering initiatives. 
 The fundamental objective of TDQM is to extend to data quality, the principles of Total Quality Management (TQM) [Oakland 1989].
In operations management, TQM has shifted the focus of reengineering activities from efficiency to effectiveness, by offering methodological guidelines aimed at eliminating discrepancies between the output of operating processes and customers’ requirements. 
Given requirements, reengineering must start from modeling operating processes. 
Consistent with these tenets, TDQM proposes a language for the description of information production (IP) processes, called IP-MAP [Shankaranarayan et al. 2000]. IP-MAP has been variously extended, 
towards UML and also to support organizational design. IP-MAP is the only language for information process modeling and represents a de facto standard. 
Practical experiences with TDQM are reported, for example, in Kovac and Weickert [2002].

- Detailed comments. TDQM’s goal is to support the entire end-to-end quality improvement process, from requirements analysis to implementation. 
As shown in Figure 6(a) TDQM Cycle consists of four phases that implement a continuous quality improvement process: definition, measurement, analysis, and improvement.
The roles responsible for the different phases of the quality improvement process are also defined in TDQM. 
Four roles are distinguished: information suppliers, which create or collect data for the IP, information manufacturers, which design, develop, or maintain data and related system infrastructure, information consumers, which use data in their work, and information process managers, which are responsible for managing the entire information production process throughout the information life cycle.
TDQM is comprehensive also from an implementation perspective, as it provides guidelines as to how to apply the methodology. 
In applying TDQM, an organization must: 
(a) clearly understand the IPs; 
(b) establish an IP team consisting of a senior executive as the TDQM champion, an IP engineer who is familiar with the TDQM methodology, and members who are information suppliers, manufacturers, consumers, and IP managers; 
(c) teach IQ assessment and IQ management to all the IP constituen- cies; and 
(d) institutionalize continuous IP improvement.

TDQM relies on the information quality literature for IQ Criteria and IQ improvement techniques. 
In particular, it explicitly refers to Wang and Strong [1996] for the data quality dimensions specification. 
TDQM relates quality issues to corresponding improvement techniques. 
However, in the recent literature no industry-specific technique is referred and no support is offered to specialize general quality improvement techniques.

## Total Information Quality Management(TIQM)

 ![avatar](figures/PhasesTIQM.png)

- General description: The TIQM methodology [English 1999] has been designed to support data warehouse projects. 
The methodology assumes the consolidation of operational data sources into a unique, integrated database, used in all types of aggregations performed to build the data warehouse. 
This consolidation eliminates errors and heterogeneities of source databases. 
TIQM focuses on the management activities that are responsible for the integration of operational data sources, by discussing the strategy that has to be followed by the organization in order to make effective technical choices. 
Cost-benefit analyses are supported from a managerial perspective. The methodology provides a detailed classification of costs and benefits (see Section 3.4).

- Detailed comments. Figure 8 shows the phases of the TIQM methodology. 
From the TIQM’s managerial perspective, there are three main phases: assessment, improvement, and improvement management and monitoring. 
One of the valuable contributions of the methodology is the definition of this last phase, which provides guidelines to manage changes in the organization’s structure according to data quality management requirements. 
Furthermore, the economics approach introduces cost benefit evaluation to justify data quality interventions. 
The goal is not only the achievement of higher data quality level, but to undertake improvement actions only if they are feasible; thus only if benefits are greater than costs.


## Data Quality Assessment(DQA) 

![avatar](figures/PhasesDQA.png)


- General description. The DQA methodology [Pipino et al. 2002] has been designed to provide the general principles guiding the definition of data quality metrics. 
In the literature, data quality metrics are mostly defined ad hoc to solve specific problems and thus, are dependent on the considered scenario. 
The DQA methodology is aimed at identifying the general quality measurement principles common to previous research.

- Detailed comments. The classification of metrics of the DQA methodology is summarized in Figure 12. 
The methodology makes a distinction between subjective and objective quality metrics. 
Subjective metrics measure the perceptions, needs, and experiences of the stakeholders. 
Objective metrics are then classified into task-independent and task-dependent. 
The first assess the quality of data without contextual knowledge of the application, while the second are defined for specific application contexts and include business rules, company and government regulations, and constraints provided by the database administration. 
Both metrics are divided into three classes: simple ratio, min or max value, and weighed average.

## Information Quality Measurement(IQM)

![avatar](figures/PhasesIQM.png)

- General description. The fundamental objective of the IQM methodology [Eppler and Mu ̈nzenmaier 2002] is to provide an information quality framework tailored to Web data. 
In particular, IQM helps the quality-based selection and personalization of the tools that support Webmasters in creating, managing, and maintaining Web sites.

- Detailed comments. The IQM methodology provides guidelines to ensure that software tools evaluate all the fundamental information quality dimensions. 
The methodology provides two sets of guidelines: the information quality framework defining quality criteria, and the action plan explaining how to perform quality measurements.
The main phases of IQM methodology are reported in Figure 13. The first phase de- fines the measurement plan. 
The information quality framework is defined as a list of relevant information quality criteria identified by interviewing the information stake- holders. 
The framework is the input for an information quality audit that associates the information quality criteria with the methods and tools that will be used in the measurement process. 
Some criteria require multiple measurement methods. The IQM methodology coordinates the application of multiple measurement methods.

## Comprehensive methodology for Data Quality management(CDQ).

 ![avatar](figures/PhasesCDQ.png)
 
- General description. The CDQ methodology [Batini and Scannapieco 2006; Batini et al. 2008] is conceived to be at the same time complete, flexible, and simple to apply. 
Completeness is achieved by considering existing techniques and tools and integrating them in a framework that can work in both intra- and inter-organizational contexts, and can be applied to all types of data, structured, semistructured and unstructured. 
The methodology is flexible since it supports the user in the selection of the most suitable techniques and tools within each phase and in any context. 
Finally, CDQ is simple since it is organized in phases and each phase is characterized by a specific goal and set of techniques to apply.

The CDQ methodology is innovative since it provides support to select the optimal quality improvement process that maximizes benefits within given budget limits. 
Second, it emphasizes the initial requirements elicitation phase. In fact, the other methodologies implicitly assume that contextual knowledge has been previously gathered and modelled. 
The focus is on how to reach total data quality without providing indications as to how to use contextual knowledge. 
A goal of CDQ is instead to obtain a quantitative assessment of the extent to which business processes are affected by bad information.

- Detailed comments. Three main phases characterize the methodology: state reconstruction, assessment, and choice of the optimal improvement process (see Figure 20). 
In the first phase of the methodology, the relationships among organizational units, processes, services, and data are reconstructed. 
These relationships are modelled by using matrixes that describe which organizational units use data and their roles in the different business processes. 
Furthermore, in this phase, processes are described along with their contribution in the production of goods/services and the legal and organizational rules that discipline workflows. 
The second phase sets new target quality levels that are needed to improve process qualities, and evaluates corresponding costs and benefits. 
This phase locates the critical variables affected by poor quality. Since improvement activities are complex and costly, it is advisable to focus on the parts of the databases and data flows that raise major problems. 
Finally, the third phase consists of five steps and is aimed at the identification of the optimal improvement process: the sequence of activities that has the highest cost/effectiveness ratio. 
New target quality levels are set by considering costs and benefits. Different improvement activities can be performed to reach new quality targets. 
The methodology recommends the identifica- tion of all the data-driven and process-driven improvement techniques for the different databases affected by poor quality. 
A set of mutually consistent improvement tech- niques constitutes an improvement process. 
Finally, the most suitable improvement process is selected by performing a cost-benefit analysis.

# Evaluation

![avatar](figures/4ClassificationOfMethodologies.png)

— complete methodologies, which provide support to both the assessment and improvement phases, and address both technical and economic issues;
— audit methodologies, which focus on the assessment phase and provide limited sup-
port to the improvement phase;
— operational methodologies, which focus on the technical issues of both the assessment and improvement phases, but do not address economic issues.
— economic methodologies, which focus on the evaluation of costs.


# Conclusions


## Challenges
可以參考The Challenges of Data Quality and Data Quality Assessment in the Big Data Era