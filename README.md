# Seminar Template
LaTeX-Template for seminar papers

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
# Related Work

In this section, 3~5 data quality assessment methods are introduced in brief:
## Total Data Quality Management(TDQM)
 ![avatar](figures/PhasesTDQM.png)

Total Information Quality Management(TIQM), 

The TIQM methodology [English 1999] has been designed to support data warehouse projects. 
The methodology assumes the consolidation of operational data sources into a unique, integrated database, used in all types of aggre- gations performed to build the data warehouse. 
This consolidation eliminates errors and heterogeneities of source databases. 
TIQM focuses on the management activities that are responsible for the integration of operational data sources, by discussing the strategy that has to be followed by the organization in order to make effective technical choices. 
Cost-benefit analyses are supported from a managerial perspective. The methodology provides a detailed classification of costs and benefits (see Section 3.4).

 ![avatar](figures/PhasesTIQM.png)

Data Quality Assessment(DQA), 
Information Quality Measurement(IQM), 
Comprehensive methodology for Data Quality management(CDQ).


# Conclusions


## Challenges
可以參考The Challenges of Data Quality and Data Quality Assessment in the Big Data Era