### Challenge 13: Detecting Fraudulent Contracts

**Level:** Easy to Medium  
  
**Description:** You work in the contracts department of a software company and are asked to detect fraudulent (or wrong) contracts based on their contract value. Given the PDF versions of the contracts, you need to extract their contract value (and, optionally, any other fields you find useful) and detect outliers among them. You can either use simpler outlier detection techniques, such as those based on statistics or visualization, or more advanced ones based on machine learning.  
  
**Author**:  [Lada Rudnitckaia](https://hub.knime.com/lada)  
  
**Dataset:** [Contract data in the KNIME Community Hub](https://hub.knime.com/alinebessa/spaces/Just%20KNIME%20It!%20Season%203%20-%20Datasets/Challenge%2013%20-%20Dataset~PY1cXhvh92p6MY-E/)  
  
**Solution Summary:** After ingesting and processing the contracts in PDF format, and isolating their contract values, we identify outliers via  [IQR (interquartile range)](https://en.wikipedia.org/wiki/Interquartile_range), and box plot and histogram visualizations. Through these techniques, two contracts seem to be fraudulent based on their unusually large values.  
  
**Solution Details:** We start our solution by parsing the PDF contracts with the PDF Parser node. Next, the Document Data Extractor node extracts text from each PDF. In parallel, we use sequences of Cell Splitter nodes to isolate contractual information, including their values. We then use the Column Appender node to add these new columns with extracted information to the initial contract table, and apply the Table Manipulator node to filter out and rename columns. At this point of the workflow, we only keep information on contract IDs and their corresponding values. This simplified table is then sent to a component named Outliers Detection, which uses a combination of nodes Numeric Outliers, Tile View, Box Plot, and Histogram nodes) to extract numeric outliers in different ways -- visually and statistically.

**[See our Solution in KNIME Community Hub](https://hub.knime.com/-/spaces/-/~Cbeyjwpy165eqvPq/current-state/?pk_vid=d6448d9ae537c0821725191057168798)**
<br>
> Written with [StackEdit](https://stackedit.io/).
