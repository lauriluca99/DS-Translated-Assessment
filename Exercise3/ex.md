Questions:

How would you design a data pipeline for a Machine Translation system? (e.g. necessary steps, main challenges, etc.)

What would you do to collect new and good quality data from the web? Assume you want to use them to train a neural model for Machine Translation.

Suppose that low quality translations created by the system are post-edited by professional translators. How would you use this process to monitor the quality of the Machine Translation system?

Answers:

1- Designing a data pipeline for a Machine Translation system involves several steps. Certainly is very important to collect a large corpus of bilingual texts and clean/preprocess these data, usually this involves tokenization, sentence segmentation, removing special characters, and normalizing the text. After that is necessary to split the data into training, validation, and test sets. The training set should be the largest portion to ensure effective model training. Now we can train a Machine Translation model using a suitable algorithm. Lastly you will have to evaluate the system through different metrics and evaluate its effectiveness and efficiency.

2- I would search major websites where translated content is available using filters and quality checks to remove irrelevant or noisy data.After that to conduct a manual review of a sample of the collected data to ensure quality. This can involve professional translators checking the accuracy of translations.

3- The new translations could enrich the train set of the system and it could be useful to retrain the network, furthermore different metrics could be adopted for the evaluation of the system.

