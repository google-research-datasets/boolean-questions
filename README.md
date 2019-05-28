# BoolQ Dataset

BoolQ is a question answering dataset for yes/no questions containing 15942 examples.
These questions are *naturally occurring* ---they are generated in unprompted and unconstrained settings.

Each example is a triplet of (question, passage, answer), with the title of the page as optional additional context.
The text-pair classification setup is similar to existing natural language inference tasks.

By sampling questions from a distribution of information-seeking queries (rather than prompting annotators for text pairs), we observe significantly more challenging examples compared to existing NLI datasets.

More details are available in [our paper](https://arxiv.org/abs/1905.10044), which can be cited as follows.


```
@inproceedings{clark2019boolq,
  title =     {BoolQ: Exploring the Surprising Difficulty of Natural Yes/No Questions},
  author =    {Clark, Christopher and Lee, Kenton and Chang, Ming-Wei, and Kwiatkowski, Tom and Collins, Michael, and Toutanova, Kristina},
  booktitle = {NAACL},
  year =      {2019},
}
```

## Dataset Description

The BoolQ dataset release consists of three `.jsonl` files, where each line is a JSON dictionary with the following format:

```
{
  "question": "is france the same timezone as the uk",
  "passage": "At the Liberation of France in the summer of 1944, Metropolitan France kept GMT+2 as it was the time then used by the Allies (British Double Summer Time). In the winter of 1944--1945, Metropolitan France switched to GMT+1, same as in the United Kingdom, and switched again to GMT+2 in April 1945 like its British ally. In September 1945, Metropolitan France returned to GMT+1 (pre-war summer time), which the British had already done in July 1945. Metropolitan France was officially scheduled to return to GMT+0 on November 18, 1945 (the British returned to GMT+0 in on October 7, 1945), but the French government canceled the decision on November 5, 1945, and GMT+1 has since then remained the official time of Metropolitan France."
  "answer": false,
  "title": "Time in France",
}
```

The files are:

* **train.jsonl**: 9427 labeled training examples
* **dev.jsonl**: 3270 labeled development examples
* **test.jsonl**: 3245 unlabeled test examples

The test data with hidden labels will be released at a later date, along with a leaderboard submission system.

## Dataset Links
* [Training set](https://storage.cloud.google.com/boolq/train.jsonl)
* [Development set](https://storage.cloud.google.com/boolq/dev.jsonl)

## Leaderboard Submission
Coming soon!

## License
BoolQ is released under the [Creative Commons Share-Alike 3.0](https://creativecommons.org/licenses/by-sa/3.0/) license.
