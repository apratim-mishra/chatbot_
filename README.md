# chatbot_
Chatbot with DialoGPT


Much of the code is taken from GPT 2 or https://github.com/huggingface/transformers/tree/main/examples/pytorch/language-modeling

This is a chatbot trained on House MD (a tv show) on a single character with data from kaggle: https://www.kaggle.com/datasets/bcruise/house-md-episodes

We make a chatbot using DialoGPT: https://www.microsoft.com/en-us/research/project/large-scale-pretraining-for-response-generation/

Transformers from the Huggingface Library are used for finetuning the model


DialoGPT is a transformer based decoder transform models for dialogue generation. They made changes to the original GPT-2 model with multiple pruning methods in training. Authors use top - k decoding strategy along with MMI (mutual information maximization) for ranking responses. 

While this has been replaced with GODEL (https://www.microsoft.com/en-us/research/project/godel/#:~:text=In%20contrast%20with%20its%20predecessor%20DialoGPT%2C%20GODEL%20leverages,a%20database%20or%20document%29%20to%20produce%20good%20responses.0) which presents better results, the multitask loss for handling language specificities is important to understand in the original DialoGPT paper.

In terms of applications, it is relatively easy to be leveraged for specific dialogue generation tasks. Here, we have used the transcripts from HOUSE MD for finetuning, but we can use transcripts from any movie or any other television to tune on a characters' dialogue.

We see clear improvements in dialogue generation in the second case, when the trained is used
