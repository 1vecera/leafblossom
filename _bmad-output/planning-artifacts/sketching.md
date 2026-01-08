What core problem are you trying to solve with decision tree visualization?
- currently, there is no easy way to properly visualize decision trees that is customizable, easy to use, interactive. At core, large trees get very quickly unreadable and confusing. The visulization packages for python are eithere to simplistic or bloated, yet not customizable.

Who experiences this problem most acutely?
- data scientists trying to understand the behavior of their decision tree based models like plain decision tress, xgboost or random forest models.
- data scientist trying to explain limits of predictability for a given problem by using decision tree surrogate model. 

What would success look like for the people you're helping?
- seemlessly integrate with existing decision tree libraries like scikit-learn, xgboost, random forest, etc.
- easy to navigate interactive visualization of the decision tree that quickly shows how the model behaves, how it decides and instances are categorized and what could be potential issues that the model learns

What excites you most about this solution?
- It would make data science pretty
- I wouldn't have to argue with the business people about the limits of predictability of the model.

The story behind the solution: I am a data scientist working on a model and the business keeps pressing me about findings some supreme drivers of churn that would drive to a model that has 80% precision for some small subset of the users. Yet, such cut of the prediction space is simply not possible! 

I've tried to visualize this by replacing the xgboost model with 700 decision trees with a simple one tree surrogate model, but quickly found it's almost impossible to customize the visualization and the default solutions: dtreeviz and sklearn.tree.plot are not enough. dtreeviz generates this crazy out of the world visualization that are unreadable for large trees and sklearn.tree.plot is not customizable at all, ugly, etc.

I'd like to change that!


----

How do people currently solve this problem?
You mentioned dtreeviz and sklearn.tree.plot - are there other workarounds data scientists use?

- not visualizing at all but looking at textual output
- there is also now a new newcomer called supertree which seems promissing and we probably create something relevant


Do people export to external tools, build custom web viz, or just give up on visualization?
- give up and use SHAP
Are there any non-Python tools that people resort to?
- none - Graphviz in case, but that is rare
What's MOST frustrating about current solutions?
- We can't customize what values are shown on each node
For dtreeviz: Is it the "crazy out of this world" visual style that's the issue, or is it also performance with large trees?
- it's not performance
For sklearn.tree.plot: Is it just the lack of customization, or are there other pain points?
- it's also not visually pleasing
You mentioned "large trees get very quickly unreadable" - what's the threshold? At what depth/size does it become unusable?
- depth 6 or 7
What happens if this problem goes unsolved?
Do data scientists just skip visualization entirely?
- yes very often.
Does this lead to poor model explainability and business mistrust?
- it leads to often missunderstanding of how the model works.
Are teams making decisions based on misunderstood models?
- yes very often - because of the missunderstanding of the model 
Who feels this pain most INTENSELY?
Is it more senior data scientists who need to explain to stakeholders?
Or junior data scientists trying to debug their models?
- not important
Are there specific industries (finance, healthcare) where this is more critical?
- not relevant 



What does supertree do well that we should learn from?


Supertree is interactive, allows for folding specific nodes, setting depths to visualize more or less of the tree.
Showing the path to the leaf
Depth change
Color change
Fullscreen in Jupyter
Links sample visualization

SHAP doesn't show you the limtis of predictability - e.g. showing that if we split the feature space we can't get to a specific precision needed.

What about interactivity - zoom, collapse branches, search nodes?

Needed

Unfair advantage - 

Will look extremely beautiful 
Will allow specifying the metrics display at each node
Will be very compact



**If we could solve this perfectly, what would that look like?**

Let me push on the specifics:

**Beauty & Design:**

-   What's your visual inspiration? Clean/minimalist? Data-rich/dense? Modern UI?

Very clean and minimalist, modern UI 
Clean information density 

-   Color schemes - predefined themes or full custom?

- something famous that works well for data visualization and doesn't scream

-   Typography - serif/sans? Data-ink ratio goals?

Lora

**Compactness Strategy:**

-   How do we handle large trees? Smart algorithms? Smart defaults?

By default not showing all the depth, but first 4 layers, nodes that are not expanded should be folded.

-   Collapsible branches as the main approach?

Information about quality of the split 

-   What about "focus mode" - zoom into one path?

yes - should be able to display single path and fold everything else

**Node Customization:**

-   What are the MOST important metrics to show? (sample count, gini, entropy, class distribution, prediction probability?)

if binary, percentage of postive cases, if multiclass, percentage of cases for each class. Clearly show on each path link variable and threshold

-   Should users build their own node templates? Or choose from presets?

-   Any ML library-specific features (XGBoost stats, sklearn specifics)?

Support outputs from XGBoost, sklearn

Is it the aesthetic standard (beautiful where others are ugly)? yes
The customization depth (control node metrics where others are rigid)? yes
The compactness algorithms (smart folding where others are overwhelming)? no

Is the data science community ready for better tools? yes, it the current visualization tools feels very outdate