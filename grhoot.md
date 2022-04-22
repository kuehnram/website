# GRhOOT Ontology

GRhOOT, the **G**erman **Rh**et**O**rical **O**n**T**ology, is a domain ontology of currently 110 rhetorical figures in the German language.

Here are the links to the ontology, the github repository, and a LODE documentation:
* [Ontology in OWL format](https://ramonakuehn.de/grhoot.owl)
* [Github Repository](https://github.com/kuehnram/GRhOOT-Ontology) 
* [LODE Documentation](https://ramonakuehn.de/grhoot_documentation.htm)
* Paper: Kühn, R., Mitrović, J., & Granitzer, M. (2022): GRhOOT: Ontology of Rhetorical Figures in German. In Proceedings of The 13th Language Resources and Evaluation Conference, Marseille, France, June. European Language Resources Association. (to appear)

## Goal
We developed a modular ontology of rhetorical figures.
The formal representation shall facilitate their detection, thus improving sentiment analysis, argument mining, detecting hate speech/fake news, and many other tasks where non-literal language is important.
The ontology can be a support for human annotators to create annotated datasets with rhetorical figures.

![Contribution](/img/websitecontribution.PNG)

## Methodology
Rhetorical figures can have a strong effect on the readers/listeners, but are often neglected in NLP. With our ontology, we want to tackle this problem and support the automatic detection and annotation of rhetorical figures. Our contributions are:

* Comparing each figure from the [RetFig](https://link.springer.com/chapter/10.1007/978-3-642-40585-3_49) ontology if it exists in German.
* Together with German linguist and reference books, we evaluated if the properties are the same.
* Ontology modeled in Protégé for 110 rhetorical figures with names in English, Serbian, and example sentences.
* We modeled 36 additional figures.
* Completeness and Consistency Check: Competency questions answered by DL and SPARQL queries to ensure that the ontology works as expected.
    



## Applications
A decision tree based on the ontology can help to find the name for a figure:
For example: 

*I like Pizza! You like Pizza!*

    Pizza:
    (Repetition = yes) ∧ (SameForm = Word) ∧ (isInPosition = End) → Epiphora

    like:
    (Repetition = yes) ∧ (SameForm = Word) ∧ (isInPosition = notSpecified) 
    → Epanalepsis/Gradatio/Anticlimax

We designed a decision tree for figures of repetition in GRhOOT:
<!-- ![DecisionTree](/img/decisiontree.pdf)-->


We are also planning to implement a web app that guides users interactively. User can choose text samples from the pool. An active learning approach helps at the annotation process, generating annotated data for machine learning models. Stay tuned for updates!

