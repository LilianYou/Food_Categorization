# Food_categorization
This is information collection for a challenge in the [2020 WaiDATATHON](https://www.womeninai.co/waidatathon) .

I used the [recipe ingredients dataset](https://www.kaggle.com/kaggle/recipe-ingredients-dataset) from Kaggle.com. The goal for the project is to discover the probability of the co-occurrence of ingredients in a recipe. I used python jupyter notebooks to run [apriori algorithms](https://medium.com/@kaumadiechamalka100/apriori-algorithm-f7fb30793274) on [Amazon Web Services](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc). Overall, the unsupervised learning algorithm I developed here will be further matched with our nutrients dataset to tailorize healthier food recommendation with more popular recipes.

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

Here are a few data visualizations from the project:

![EDA](https://raw.githubusercontent.com/LilianYou/Food_Categorization/images/fig1.png)

The loaded dataset consists of 428,275 single item descriptions. I first did a data exploration by listing the occurring frequency of ingredients from all recipes. 

![EDA2](https://raw.githubusercontent.com/LilianYou/Food_Categorization/images/fig2.png)

Here is another direct visualization of the food frequency. As you can see here, common food like oil, garlic, pepper, onion, butter, appear most frequently in food recipes.

![parallel visualize plot](https://raw.githubusercontent.com/LilianYou/Food_Categorization/images/fig3.png)
Based on the EDA figure, I did an association rule mining. As you can see, here is a parallel visualize plot displaying the connection between each pair of ingredients from the recipe datasets. High frequency ingredients has higher possibility to connect with all other ingredients, especially other high frequency ingredients.

![parallel visualize plot](https://raw.githubusercontent.com/LilianYou/Food_Categorization/images/Fig4.png)
If you zoom in the plot, you can tell that, for example, garlic has the highest frequency co-occur with oil, and then onion, pepper, cilantro, soy sauce, and butter.

![parallel visualize plot](https://raw.githubusercontent.com/LilianYou/Food_Categorization/images/Fig5.png)
I also did a network graph of the relationship of all ingredients in the recipe dataset. We found a concentric layout of the graph, meaning ingredients within the same frequency categorization have corresponding level of possibility connecting with each other.

![parallel visualize plot](https://raw.githubusercontent.com/LilianYou/Food_Categorization/images/Fig6.png)
When we take a look at the association rules strength distribution, we can see that the likelihood of two ingredients co-occur in a recipe increases with the popularity of ingredients and then correlation maintains even when controlling for the independent popularity of one of the ingredients in a pair.

