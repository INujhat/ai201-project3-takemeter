# TakeMeter Project Planning

## Community

For this project, I chose the Reddit community **r/movies**. This community contains thousands of discussions where users share reactions, reviews, and detailed analyses of movies. The variety of writing styles makes it a good dataset for a text classification task.

---

## Label Taxonomy

### Analysis

Posts that explain opinions using evidence, reasoning, or technical discussion about filmmaking.

Examples:

* "The cinematography uses long tracking shots to create suspense."
* "The screenplay carefully develops each character before the climax."

---

### Review

Posts that express a personal opinion while giving a brief explanation.

Examples:

* "I really enjoyed this movie because the acting was fantastic."
* "I didn't like the ending because it felt rushed."

---

### Reaction

Posts that mainly express an emotional response with little or no explanation.

Examples:

* "This movie was amazing!"
* "Worst movie ever."

---

## Hard Edge Cases

Some posts contain both opinions and technical reasoning.

Example:

"This movie is terrible because the pacing and editing completely ruined the experience."

This could be classified as either Review or Analysis.

Decision Rule:

If the post mainly expresses a personal opinion, it will be labeled **Review**.

If the post focuses on technical reasoning or evidence, it will be labeled **Analysis**.

---

## Data Collection Plan

I will collect approximately 200 public posts and comments from r/movies.

Target distribution:

* Analysis: 65 examples
* Review: 70 examples
* Reaction: 65 examples

If one label becomes underrepresented, I will collect additional examples for that category until the dataset is reasonably balanced.

---

## Evaluation Metrics

I will evaluate my model using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

Accuracy measures overall correctness, while Precision, Recall, and F1 Score provide better insight into how well each label is predicted.

---

## Definition of Success

I would consider the classifier successful if it achieves approximately 80% accuracy with balanced F1 scores across all three labels. The fine-tuned model should outperform the zero-shot baseline.

---

## AI Tool Plan

### Label Stress Testing

I will use ChatGPT to generate difficult examples that sit between my labels to verify that my definitions are clear.

### Annotation Assistance

I may use ChatGPT to suggest labels for examples, but every label will be reviewed manually before being added to the dataset.

### Failure Analysis

After evaluation, I will use ChatGPT to identify patterns among incorrect predictions and verify those findings before writing my analysis.

