# The rules of survival
## Mini-project

For this project you are asked to implement the *PRISM* algorithm to extract the classification rules with the highest accuracy and coverage from the hospital patients [dataset](https://drive.google.com/file/d/1uVd09ekR1ArLrA8qN-Xtu4l-FFbmetVy/view?usp=sharing) described in this [demo notebook](rules_motivation.ipynb).

Your algorithm should extract the rules ranked by accuracy (from highest to lowest), and the ties are broken in favor of a rule with a higher coverage. If both accuracy and coverage are the same - the condition is selected arbitrarily.

Your algorithm should have two additional optinal parameters: 
* the _accuracy_ threshold - the number from 0 to 1 which specifies which rules are considered valid. If after refining the rules and still within the coverage threshold you reach the best accuracy which is below the threshold, you can stop generating rules. 
* the _coverage_ threshold - the absolute number of records covered by the rule. If a more precise rule covers less records than this threshold, the algorithm should stop refining this rule. If the accuracy of this rule is high enough, it is added to the solution. Otherwise this rle is abandoned.

The output of the algorithm should be a decision list, where all the rules are presented ranked as above. For each Rule include the rule itself, its accuracy, and its coverage.

Please keep your code clean, modular, and add explanations for each step.

Finally, apply the algorithm to the Titanic and COVID-19 datasets.  

In your report (a separate markdown Section), summarize which rules did you learn from this dataset, and discuss your discoveries.
