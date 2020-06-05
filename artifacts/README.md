---
description: Dataset versioning and model management
---

# Artifacts

Artifacts is the latest product in the Weights & Biases toolkit, focusing on dataset versioning, pipeline tracking, and model management. Users reached out after trying solutions like DVC and Pachyderm, asking for a way to neatly integrate with W&B. We're iteratively building this new product with feedback from our users. Reach out in the [W&B Forum](http://bit.ly/wandb-forum) with questions or suggestions.

W&B Artifacts track and version the **data objects** used across your ML pipeline. Use Artifacts to keep track of all the dataset versions, models, and evaluation results used and generated in machine learning projects. You can think of a single W&B artifact as an **immutable folder of data**. An artifact’s contents are carefully checksummed and verified, to ensure reproducibility.  
  
Artifacts are general and flexible: you can store data directly in them, or store **references** to data in other systems. Using our Artifacts API, you can log artifacts as outputs of W&B runs, or use artifacts as input to runs.

![](../.gitbook/assets/artifact1%20%281%29.png)

Since a run can use another run’s output artifact as input, artifacts and runs together form a directed graph. You don’t need to define pipelines ahead of time. Just use and log artifacts, and we’ll stitch everything together.

![](../.gitbook/assets/artifact2.png)
