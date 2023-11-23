# ML-Competition-CUET-ETE-Day-2023
Data Pre-processing:
At first, we explore the dataset to get about the idea of text orientation and 'NaN' value. We remove 'NaN' valued column from the training set. We visualize text length to get mean text length. We process data by removing stop words punctuation and white space. We also normalize text and make lowercase all the English text. We remove 'href' from the dataset. "%" is converted to ' শতাংশ'. The removes all optional occurrences of ZWNJ or ZWJ from Bangla text. One more thing we did was convert the emoji to text.

Modeling and parameter setting:
We split the train set 8.2 ratio for the training set and validation set. We fine-tune 'banglabert' model for in this downstream task. We choose 320 as the max length of the text to get tokenization of the summary. We also enable truncations and padding while tokenizing. We only keep labels, 'input_ids' and 'attention_mask' for training and validating bert model. For test 'input_ids' and 'attention_mask' are kept.

The parameter settings for inference are learning rate =2e-5, warmup ratio' =0.1, weight decay =0.01, 'epoch' = 5, batch size = 8, optimizer = adafactor and 0.3 dropout rate.
