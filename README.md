# Natural Language Inteference(NLI) for detecting contradiction

## Notebook Introduction
Link to dataset : [Contradictory, My Dear Watson)](https://www.kaggle.com/competitions/contradictory-my-dear-watson/code)

Mainly this competition focusing one usage of TPU for training NLI model, but in this notebook GPU will be used instead.
model used is [mDeBERTa](https://huggingface.co/MoritzLaurer/mDeBERTa-v3-base-xnli-multilingual-nli-2mil7)

This notebook focusing on how to achieve good accuracy in detecting three categories : entailment, contradiction and neutral.
the dataset contain 4176 entailment labels, 3880 contradiction labels, and 4064 labels.

the number of epoch is 5 and learning rate 1-e4.

## Evaluation

While the accuracy reached 80.9% , the gap between training and validation loss are too wide. This mean the model overfitting with its training dataset. The cause of overfitting might be the learning rate should be lower, the data is not big enough for model to learn. So we can say model perform best at first epoch with accuracy of 75.1%
or something that we not discovered yet.

## Future research

Adding more data into dataset and applying peft to lower cost of computation.

Thanks for reading !
