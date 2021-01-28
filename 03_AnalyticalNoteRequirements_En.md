# Analytical Note Requirements

## Synopsis

Analytical note (AN) is the primary working and reporting document for the R&D, Prototype and MVP phases of any artificial intelligence-aided digital project (AIDP). It describes the context of the problem, presents the business and mathematical statements of the problem. It also contains analysis of the source data, discussion of suggested solution and recommendations on the results of the accomplished work. AN is used for a general assessment of approach to the solution and obtained results without an in-depth study of the practical implementation of the algorithms and actual scrutiny of the written code.

AN is chiefly used as grounds for the managerial decisions regarding transition from one project phase to another (e.g., from Prototype to MVP), as well as for simplifying the planning and decision-making communications within a project team at different stages. The document is also used for a retrospective analysis of project delivery, general characterization of an integrated multi-module digital product, as well as for introduction of the problem context to the new team members (including when a product is handed over to the service support). Therefore, the target audience of any AN includes project managers, product owners, technology experts, and new specialists engaged in the development process.

It should be said that AN is drafted and filled up in the course of all the project phases, ensuring communication and enabling a retrospective analysis of the project's evolution. AN seeks to record each crucial hypothesis and solution iteration, including those that failed to yield expected results. In terms of its implementation, AN should represent a part of project-related Wiki. The Contractor may chose any appropriate Wiki-platform tool (we recommend functionality identical to the proprietary Confluence platform), however it must feature data export into Word and PDF files. In case of Gazpromneft, the Wiki-platform should be corporate Confluence belonging to the Company.

Since AN is gradually filled during several months of the project it is worth somehow marking sections with updates rather than suggesting the team to read the whole text all over again. This could be done by highlighting the new text for fast navigation (the highlights from the previous updates should be removed). The exact timing of AN update should be discussed between the authors, but the most rational is shortly before the regular project meetings. Also it is worth to send notifications to the team about the exact locations of the updated sections, so they won’t have to search through the text manually.

Finally, it should be noted that different sections of AN are filled by various members of the project team. The introduction and business sections are filled by technical analyst of data science (TADS). The data section is written by the data engineer, and the model study – by the data analyst (data scientist). The final validation of the technical part is performed by senior data analyst (senior data scientist), while the overall editing and verification of the text coherence is done by TADS. If some roles are missing within the project team, then data scientist writes the relevant text instead (for the introduction and business parts it is assumed that only the most basic information should be provided).

This document suggests requirements for a step by step completion of different sections of AN in accordance with the approved template. The template covers the minimum essential information related to the project. However, the authors of the analytical note are free to include any additional sections that may contribute to a streamlined presentation. The location and titles of the suggested sections are dictated by the overall logic of the narrative, but they can be modified depending on the nature of a specific problem. If the sections are rearranged, the authors must ensure consistency and coherence of the text to allow for a seamless understanding of the material by the reader.


## 1. Problem statement

### 1.1 Problem overview

General context of the problem. Description of the standard technological and business processes (for example, "NDT probes are used to monitor а pipe wear; they include 12-16 instrument modules that diagnose magnetic behavior of the pipe"). Approximate volume: 1-2 pages.

### 1.2 Business problem statement

Description of the current situation at GPN Group in respect to this problem, supported with specific figures and realistic estimates. A detailed description of the "bottleneck" and results that can be achieved if the bottleneck is eliminated. Presentation of business metrics and expected outcome in explicit form (e.g., reduced risk, reduced time, lower labor input, etc.). Approximate volume: 1-2 pages.

### 1.3 General statement of the mathematical problem

#### 1.3.1 Hypothesis

Presumed approach to solving the problem with the help of AI algorithms. Justification of using AI algorithms, rather than utilizing other approaches. Presumption of the most suitable algorithms and mathematical metrics. General assumptions for solving the problem. The exact list of mathematical problems solved in the project (e.g., solving the classification problem, optimization problem, etc.). Approximate volume: 1-2 pages.

#### 1.3.2 Technical statement of the problem

General mathematical statement. For example, “Let: X is a set of object descriptions (core photos) and Y is a set of classes (sandstone, siltstone, mudstone etc.). It is required to find an unknown dependence of mapping X→Y based on the training dataset Xm={(x1, y1), …, (xm, ym)} and given the assumptions Z.” Approximate volume: 1 page.

#### 1.3.3 Digital product acceptance criteria and general model precision requirements

Description of the accuracy requirements for the mathematical core (provided by the Customer), as well as general acceptance requirements for the project stage deliverables discussed in the current version of AN (analytical note is filled up gradually throughout several AIDP phases). Specification of the general criteria for the overall project success.

## 2. Source data analysis results

### 2.1 Data format description

Listing of key parameters used to solve the problem. Description of the data sources (location of the data warehouse, description of its structure, data export and updating processes) and dataset merging process. Description of how data was converted into widespread "readable" formats (especially for data recorded by the specialized sensors).

### 2.2 Data integrity and quality analysis

Identification of data quality and representativity. Building bar charts of key relevant parameters (including by class/cluster) that can offer a visual understanding of the values scattering extent and also demonstrate the general trends (e.g., for core images analysis – listing of every combination of rocks found in the images). Analysis of the data principal statistical characteristics (minimum and maximum values, dispersion, mathematical expectation, etc.). Building correlation matrices for all values (in case of large scope of values, this information should be provided in an attachment or as a separate file).

### 2.3 Outliers and anomalies analysis

Description of outliers/corrupt data/missing data. Graphs of their distribution by class/cluster. 

### 2.4 Final dataset description

Justification of any information removal from the dataset. Description of the data recovery or filtering (scripts). Description of the final dataset format and parameters.

### 2.5 Expert evaluation

Listing of data seen as crucial by the expert and justification of this opinion (e.g., physical patterns or parameters approved in the operating manual). Existing data analysis methodology (if any) that the expert uses on a regular basis, indicating the metrics and results expected after the data processing. This Section may, to some extent, duplicate the Data description document.

## 3. Problem solution description

### 3.1 General

#### 3.1.1 Solution logic

Description of the general solution logic (e.g., in a block diagram format). Primarily this is required when several sub-problems are solved in parallel within a single initiative.

#### 3.1.2 Metrics

General description and justification of mathematical metrics employed for testing purposes. Specification of the metrics hierarchy, i.e. how metrics of individual models are transformed into general quality metrics for the entire digital product. The metrics basic descriptions should be given in the end of the current document (Section 6.1). If such description is provided, Section 3.1.2 should contain the proper links to it. Also if there are no sub-problems within a given initiative, the current Section is omitted and the metrics are described in Section 3.2.1.1.

### 3.2 Solving sub-problem 1

If there are no separate sub-tasks, the section is renamed as Problem solution. In this case, hereinafter in the template the term sub-problem should be understood just as a problem.

#### 3.2.1 Problem solution strategy

Description of the general logic of solving sub-problem 1.

##### 3.2.1.1 Mathematical sub-problem statement and metrics selection

Mathematical definition of the sub-problem 1. Boundary conditions. Description and justification of the selected metrics for the given sub-problem. The metrics basic descriptions should be given in the end of the current document (Section 6.1). If such description is provided, Section 3.2.1.1 should contain the proper links to it.

##### 3.2.1.2 Data preparation

Description of the training, validation and testing sets selection. If required, description of the data balancing process in case of the nonuniform initial data representation (e.g., there are 100 wells with measurements during 10 months, and 10 wells with measurements during 100 months). Description of any other data transformations conducted within this sub-problem.

##### 3.2.1.3 Mathematical models description

Listing of all mathematical models used within this sub-problem and justification of their choice supported by the references on the research papers, previous projects and best practices (this Section could be seen as a small literature review). The models basic descriptions should be given in the end of the current document (Section 6.1). If such description is provided, Section 3.2.1.3 should contain the proper links to it.

##### 3.2.1.4 Mathematical models study

Description of all numerical experiments with the models form Section 3.2.1.3. The experiments conditions, model hyperparameters and settings should be provided along with the achieved metrics values. Each experiment should link to a particular Jupiter Notebook or similar computing environment, where the study was conducted, to provide an opportunity for independent verification of the obtained results. The results themselves should be provided in the form of plots and tables.
 
Description of additional criteria for choosing the best model apart from meeting the defined metrics (required, when several models demonstrate similar results). Selection of the best model based on the metrics and any additional criteria. 

Please note that this is the most important Section of the report. It must provide exhaustive information about the tested models supported by the benchmarking graphs and charts. If necessary, this Section may contain additional sub-sections for a more structured representation of information.

##### 3.2.1.5 Conclusions for sub-problem 1

Results of the best model on the test dataset. The study of the model applicability boundaries. General conclusions on the quality of the best model.


### 3.3 Solving sub-problem 2

The content of this Section is identical to that of 3.2 (in presence of sub-problem 2).

## 4. Model applications

A brief description of the further model applications (in which digital services will it work, where the final digital solution will be deployed, what are the expected application scenarios, etc.). If the graphic prototype is ready, provide its screenshots or other clarifying infographics. Approximate volume: 1 page.

Please note that detailed functional and technical requirements to the digital product are provided in a separate Requirements Specification for MVP refinement stage of AIDP, and not in AN.

## 5. Conclusion

### 5.1 Takeaways

Summary of the completed work. Explicit recommendations to move on to the next project phase, start a new R&D initiative with a related subject, or a statement that the further work on the project is counter-productive with the justification of this opinion. Approximate volume: 1-2 pages.

### 5.2 Recommendations

#### 5.2.1 Recommendations on the data

Particular recommendations on improving completeness and quality of the data (e.g., accumulating a larger dataset, retrofitting the measuring systems with extra sensors, changing the date recording intervals, etc.). Approximate volume: 1-2 pages.

#### 5.2.2 Problem solution recommendations

Particular recommendations on the application of AI algorithms (e.g., suggestion to use a different type of algorithms or a different logic of solution accuracy assessment). Listing of new problems, which could arise during the initiative realization. Approximate volume: 1-2 pages.

## 6. Attachments

### 6.1 Glossary

Reference section, which contains the abbreviation list and the description of basic concepts. The latter includes the general information on the studied algorithms and implemented metrics. This Section may contain multiple external links.

### 6.2 Takeaways

Any materials that were not included in the body of analytical note (to keep it concise) but should not be removed from it (e.g., additional graphs and charts).

### 6.3 Project retrospection 

The brief description of previous stages of the project or major solution steps, which could have some retrospective value.
