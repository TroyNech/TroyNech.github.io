---
title: Apriori Implementation
---   

**[Code](https://github.com/TroyNech/apriori)**

This is an assignment I did for my data mining course last term. It finds the association rules of a dataset using the Apriori algorithm.

With the provided dataset, association rules of size 3 are as follows:

1. {DAI55911, GRO85051} -> {FRO40251} (1.00000)
2. {DAI62779, DAI88079} -> {FRO40251} (1.00000)
3. {ELE17451, GRO85051} -> {FRO40251} (1.00000)
4. {ELE26917, GRO85051} -> {FRO40251} (1.00000)
5. {ELE92920, DAI23334} -> {DAI62779} (1.00000)

The high-level pseudo code is as follows:

* Create Apriori object
* Find the list of frequent items by reading each transaction in the file (try to add items to hashmap (Itemset class overrides equals and hashCode) as key with value 1 – if already exists in hashmap, increment value)
* Continue finding larger frequent itemsets until tgtItemsetLen is hit or there were no frequent itemsets in the last iteration
  * Find the candidate set
    * If the candidate itemset length is 1, candidate set is all possible pairs of frequent items
    * Else the candidate set is the set of itemsets created when 2 frequent itemsets that are the same except for the last item are combined
  * Read each transaction in the file, incrementing the count of those candidate itemsets that appear in the transaction
  * Move infrequent itemsets into an infrequentItemset hashmap
* Compute the association rules where antecedent length is tgtItemsetLen - 1 and consequent length is 1. Create all possible combinations of frequentItemset of length tgtItemsetLen. Get the required support values by looking through the saved frequent and infrequent itemsets of smaller lengths
* Sort the rules first in descending order of confidence, then by ascending order of itemsets (Rule class overrides compareTo)
* Print out rules in format “{antecedent} -> {consequent} (confidence)”
