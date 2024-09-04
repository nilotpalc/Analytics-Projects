### Challenge 5: Offensive Language and the LGBTQIA+ Community

****Level:**** Medium
****Description:**** As a member of a think tank, your task is to craft a report on LGBTQIA+ representation in political discourse. Given a EU dataset gathering responses from LGBTQIA+ individuals across all member states, you decide to start your work by investigating the answers to the following question:  _"In your opinion, how widespread is offensive language about lesbian, gay, bisexual, and/or transgender people by politicians in the country where you live?”.  
  
_Use a map to present the results effectively.

****Author**:** [Michele Bassa](https://hub.knime.com/michele_bassa)
****Datasets:**** [LGBTQIA+ Survey Data in the KNIME Community Hub](https://hub.knime.com/alinebessa/spaces/Just%20KNIME%20It!%20Season%203%20-%20Datasets/Challenge%205%20-%20Dataset~5454ntBTXopo7O3V/)<br>
****Solution Summary:**** To tackle this challenge, we reduce the scope of the data to question  _"In your opinion, how widespread is offensive language about lesbian, gay, bisexual and/or transgender people by politicians in the country where you live?"_. We then filter the answers and only keep the most common ones:  _"rare"_ and  _"widespread"_. This facilitates the understanding of trends and patterns across countries. We compute the percentages of answer  _"widespread"_  for every country and also compute their map coordinates. Finally, we join the geospatial information and the computed percentages and plot them in a map.****Solution Details:**** After reading the survey dataset with the CSV Reader node, we prepare the data by reducing it to question  _"In your opinion, how widespread is offensive language about lesbian, gay, bisexual and/or transgender people by politicians in the country where you live?"_, and to its two most common answers,  _"rare"_ and  _"widespread"_. We also group the data by country, keeping the totals for both answers. We loop over this data (Group Loop Start and Loop End nodes) to compute the percentages of answer  _"widespread"_  for every country, using the Math Formula node (we compute the denominator for these percentages with the Moving Aggregator node). Next, we run another loop (Table Row to Variable Loop Start and Loop End nodes) to find the map coordinates of each country with the OSM Boundary Map node. We join the previously calculated percentages to the data with the map coordinates (Joiner node), use the Projection node to improve formatting for visualization, filter irrelevant data with the Row Filter node, and then finally plot the computed information with the Geospatial View node.

[See our Solution in KNIME Community Hub](https://hub.knime.com/knime/spaces/Just%20KNIME%20It!/Challenge%205%20-%20Offensive%20Language%20and%20the%20LGBTQIA+%20Community~kqNKL3L8bXvdfurV/current-state?pk_vid=d6448d9ae537c0821725424102168798)


> Written with [StackEdit](https://stackedit.io/).
