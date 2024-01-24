# ViT-Model
## Vision Transformer and Contrastive Representation Learning

In this model, first, we are implemting [Vision Transformer](https://arxiv.org/pdf/2010.11929v2.pdf) (ViT) for image recognition. Then, we are utilizing the implemented ViT to train a model using [Contrastive Representation Learning](https://arxiv.org/pdf/1503.03832.pdf), i.e. Triplet Loss.
## Part 1 : Data Augmemtation

For the dataset, we will use the FashionMNIST dataset. For implmentation, you are explore the usage of different [data augmentation](https://pytorch.org/vision/master/auto_examples/transforms/plot_transforms_illustrations.html) techniques.
## Part 2 : Vision Transformer

A `check_vit.py` test script is provided to inspect the correctness of your implementations. Make sure not to modify any code in the provided test script.

Additionally, the code to train a classifier is provided below. If your ViT implementation is correct, a trained model should reach 88% accuracy and above with no issue.

## Part 3 : Contrastive Representation Learning

In this part, you are to use [PyTorch-Metric-Learning](https://github.com/KevinMusgrave/pytorch-metric-learning) to implement triplet loss and learn an embedding representation model with ViT. Quick tutorials and notebooks are available in the repo.

However, only a subset of data from the FashionMNIST training set (around 1/12) will be used to train the model. The code to subsample the full train dataset is provided in `sample_balanced_subset`. You must not modfiy the code in that block.

To pass this part, you are to reach **60%** and above in Precision@1 metric scoring on the full FashionMNIST test dataset with your trained embedding model. The final model must be submitted along with your notebook with logging outputs. The test function is provided in `evaluate_at_end_epoch`.

Furthermore, you are required to employ one of the learning rate schedulers, like [MultiStepLR](https://pytorch.org/docs/stable/generated/torch.optim.lr_scheduler.MultiStepLR.html#torch.optim.lr_scheduler.MultiStepLR), [Consine Annealing LR](https://pytorch.org/docs/stable/generated/torch.optim.lr_scheduler.CosineAnnealingLR.html#torch.optim.lr_scheduler.CosineAnnealingLR). Or you can implement your own learning rate adjusting strategy, as a function to training iteration or epoch, using [LambdaLR](https://pytorch.org/docs/stable/generated/torch.optim.lr_scheduler.LambdaLR.html#torch.optim.lr_scheduler.LambdaLR).

## Part 4 : Application

In the below examples, we perform inference with the trained embedding model using K-nearest neighbors.

Now, we perform the K-nearest neighbors, by comparing our sample against the embeddings in the bank.

The trained embedding model can also be used to train a new classifier.

The intuition behind **Transfer Learning**, and a referring tutorial can be seen [here](https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html).

A sample function to test with the classification head is provided, as `test_classification_model`.
