# Food_categorization
This is information collection for a challenge in the [2020 WaiDATATHON](https://www.womeninai.co/waidatathon).
.
Data are from public sources. The goal is to select dishes for people based on nutritient needs, so that people can get good advice on what food to eat.

Concepts:

Association Mining searches for frequent items in the data-set. In frequent mining usually the interesting associations and correlations between item sets in transactional and relational databases are found. In short, Frequent Mining shows which items appear together in a transaction or relation.

Need of Association Mining:
Frequent mining is generation of association rules from a Transactional Dataset. If there are 2 items X and Y purchased frequently then its good to put them together in stores or provide some discount offer on one item on purchase of other item. This can really increase the sales. 

Important Definations :
Support : It is one of the measure of interestingness. This tells about usefulness and certainty of rules. 5% Support means total 5% of transactions in database follow the rule.
Support(A -> B) = Support_count(A ∪ B)
Confidence: A confidence of 60% means that 60% of the customers who purchased a milk and bread also bought butter.
Confidence(A -> B) = Support_count(A ∪ B) / Support_count(A)
If a rule satisfies both minimum support and minimum confidence, it is a strong rule.

Support_count(X) : Number of transactions in which X appears. If X is A union B then it is the number of transactions in which A and B both are present.

Maximal Itemset: An itemset is maximal frequent if none of its supersets are frequent.
Closed Itemset:An itemset is closed if none of its immediate supersets have same support count same as Itemset.
K- Itemset:Itemset which contains K items is a K-itemset. So it can be said that an itemset is frequent if the corresponding support count is greater than minimum support count.

Data description:
Data come from Recipe1M+ http://pic2recipe.csail.mit.edu/
