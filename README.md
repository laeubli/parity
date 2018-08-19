# Has Neural Machine Translation Achieved Human Parity? A Case for Document-level Evaluation

This repository contains the data we collected to assess the impact of document-level context on human perception of machine translation quality.

We briefly outline the contents of each file below. Please see our [paper](https://openreview.net/forum?id=Hygfmc5U-7) for more detailed information:

```
@inproceedings{laeubli2018parity,
  author = "L{\"a}ubli, Samuel and Sennrich, Rico and Volk, Martin",
  title = "Has Neural Machine Translation Achieved Human Parity? A Case for Document-level Evaluation",
  booktitle = "Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing (EMNLP)",
  year = "2018",
  address = "Brussels, Belgium",
  publisher = "Association for Computational Linguistics",
  url = "https://openreview.net/pdf?id=Hygfmc5U-7"
}
```

### `participants.csv`

Meta information on all participants – professional translators recruited from [ProZ](https://www.proz.com). They produced the ratings available in `ratings.csv`.

### `documents.csv`

55 full articles randomly sampled from the [WMT 2017 English–Chinese test set](http://www.statmt.org/wmt17/translation-task.html), only considering the 123 native Chinese articles. We only used Chinese sources from WMT; human (Reference-HT; the `human` column) and machine translations (Combo-6; the `mt` column) were obtained from [data released by Microsoft](http://aka.ms/Translator-HumanParityData).

Documents E-1 to E-55 and I-1 to I-55 are the same articles with a different random subset (5 articles) converted to control items (spam).

### `sentences.csv`

2 x 120 sentences randomly sampled from the [WMT 2017 English–Chinese test set](http://www.statmt.org/wmt17/translation-task.html), only considering the 123 native Chinese articles. We only used Chinese sources from WMT; human (Reference-HT; the `human` column) and machine translations (Combo-6; the `mt` column) were obtained from [data released by Microsoft](http://aka.ms/Translator-HumanParityData).

Sentences U-1 to U-120 overlap with the full documents in `documents.csv`. 16 random sentences were converted to control items (spam) in each set.

### `ratings.csv`

Ratings produced by participants (see `participants.csv`). In our paper, we excluded ratings for sentences U-1 to U-120 from analysis because of overlap with full documents (see above).

### `ratings.with-spam.csv`

The same as `ratings.csv`, including control items (spam).
