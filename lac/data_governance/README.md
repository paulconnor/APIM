Summary:

This project was designed to provide a data governance framework for sharing potentially sensitive data stored in siloed databases with external partners. Due to the nature of the data and associated PII attributes, there needed to be a model that mapped physical database fields to logical groupings. Individual fields might not represent a data privacy issue, but when combined with other fields the sensitivy level can quickly escalate. The data privacy categories needed to be applied at this logical grouping of fields and extracted from an in-house reporting tool. Then consumers of data collections would be granted access based on their own security classification and that of the data sets in question.

The key elements to the data privacy model were:

- Classification – that defines the Collection, phyical Data Elements and the Classification Level for a number of logical data collections.
- Source Data – provides records from different sources and associated attributes.
- Mapping – defines the relationship between the Classification logical data elements and the physical attributes from the Source DBs.

This is required and important as the Classification is on a Logical data level and the Source Data is on a Physical level (typically from databases).

Process steps:

1) Read the Source Data records
2) For each Source Data record get the logical mapping
3) Obtain the Classification level for the logical data item
4) Produce various reports for different consumers based on their security clearance

In addition, it was required to be able to get report meta data for auditing to show who was consuming what types of classified data. 

For example:
- what Classifications a report contains.
- list of the Data sources and Destination
- any other useful/relevant metadata
