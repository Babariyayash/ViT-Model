## Assignment 3: Vision Transformer and Contrastive Representation Learning

In this assignment, first, you are to implement [Vision Transformer](https://arxiv.org/pdf/2010.11929v2.pdf) (ViT) for image recognition. Then, you are utilize the implemented ViT to train a model using [Contrastive Representation Learning](https://arxiv.org/pdf/1503.03832.pdf), i.e. Triplet Loss.

### Submission Guidelines
The assignment codebase is split into two files. `vit_model.py` and `assignment3.ipynb`. In `vit_model.py`, incomplete codes for ViT and embedding model are provided, while in `assignment3.ipynb`, incomplete codes to iterate [FashionMNIST dataset](https://github.com/zalandoresearch/fashion-mnist) and initiate training and testing are provided in blocks. You are to complete the missing codeblock (Marked with comments and #TODO signs) and train the embedding representation model.

In addition to PyTorch, [pytorch-metric-learning](https://github.com/KevinMusgrave/pytorch-metric-learning) is needed to help with the implementation of contrastive representation learning. You are strongly encouraged to go through the [README of the repo](https://github.com/KevinMusgrave/pytorch-metric-learning/blob/master/README.md), which contains the basic usage of the package. You are also strongly encouraged to study the example notebooks provided within the repo, at your own pace.

To submit this assignment for grading, you must submit a compressed zipfile as `Assignment3_{YourCCID}.zip`, with three files inside: `vit_model.py`, `assignment3.ipynb`, and your trained embedding model as `vit_embeds.pt`.

### Collaboration Policy
This must be your own work. Do not share or look at the code of other students (whether they are inside or outside the class). Do not copy the code from the Internet, other than referring [PyTorch's official tutorials](https://pytorch.org/tutorials/), or the examples provided within [pytorch-metric-learning repo](https://github.com/KevinMusgrave/pytorch-metric-learning/tree/master/examples). You can talk to others in the class about solution ideas (but detailed enough that you are verbally sharing, hearing or seeing the code). You must cite whom you talked with in the comments of your programs.
