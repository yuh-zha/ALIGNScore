# AlignScore
This is the repository for AlignScore, a metric for automatic factual consistency evaluation of text pairs. The metric is introduced in 

[AlignScore: Evaluating Factual Consistency with a Unified Alignment Function](https://arxiv.org/abs/2305.16739)

Yuheng Zha, Yichi Yang, Ruichen Li and Zhiting Hu

ACL 2023

What is factual consistency and its evaluation?
* **Facutual Consistency:** For a given text pair (**a**, **b**), they are considered factual consistent if 1) all the information in **b** is also present in **a**; 2) **b** does not contradict **a**.
* **Evaluation:**  Show the degree of factual consistency between the context (text **a**) and the claim (text **b**).

Where is factual consistency evaluation applicable?
* **Summarization**: document and summary
* **Paraphrase**: sentence A and sentence B
* **Dialog**: context and response
* ...

# Leaderboard
We list the performance of AlignScore as well as other metrics here. 

| Rank | Metrics          | SummaC* | TRUE** | Other-Spearman | Average | Paper | Code |
| ---- | :--------------- | :-----: | :----: | :------------: | :-----: | :---: | :--: |
| 1    | AlignScore-large |  88.6   |  83.8  |      49.3      |  73.9   |   -   |   -  |
| 2    | AlignScore-base  |  87.4   |  82.5  |      44.9      |  71.6   |   -   |   -  |
| 3    | QAFactEval       |  83.8   |  79.4  |      42.4      |  68.5   | [:page\_facing\_up:](https://arxiv.org/abs/2112.08542) | [:octocat:](https://github.com/salesforce/QAFactEval) |
| 4    | UniEval          |  84.6   |  78.0  |      41.5      |  68.0   | [:page\_facing\_up:](https://arxiv.org/abs/2210.07197) | [:octocat:](https://github.com/maszhongming/UniEval) |
| 5    | SummaC-CONV      |  81.0   |  78.7  |      34.2      |  64.6   | [:page\_facing\_up:](https://arxiv.org/abs/2111.09525) | [:octocat:](https://github.com/tingofurro/summac) |
| 6    | BARTScore        |  80.9   |  73.4  |      34.8      |  63.0   | [:page\_facing\_up:](https://arxiv.org/abs/2106.11520) | [:octocat:](https://github.com/neulab/BARTScore) |
| 7    | CTC              |  81.2   |  72.4  |      35.3      |  63.0   | [:page\_facing\_up:](https://arxiv.org/abs/2109.06379) | [:octocat:](https://github.com/tanyuqian/ctc-gen-eval) |
| 8    | SummaC-ZS        |  79.0   |  78.2  |      30.4      |  62.5   | [:page\_facing\_up:](https://arxiv.org/abs/2111.09525) | [:octocat:](https://github.com/tingofurro/summac) |
| 9    | ROUGE-2          |  78.1   |  72.4  |      27.9      |  59.5   | [:page\_facing\_up:](https://aclanthology.org/W04-1013/) | [:octocat:](https://github.com/pltrdy/rouge) |
| 10   | ROUGE-1          |  77.4   |  72.0  |      28.6      |  59.3   | [:page\_facing\_up:](https://aclanthology.org/W04-1013/) | [:octocat:](https://github.com/pltrdy/rouge) |
| 11   | ROUGE-L          |  77.3   |  71.8  |      28.3      |  59.1   | [:page\_facing\_up:](https://aclanthology.org/W04-1013/) | [:octocat:](https://github.com/pltrdy/rouge) |
| 12   | QuestEval        |  72.5   |  71.4  |      25.0      |  56.3   | [:page\_facing\_up:](https://arxiv.org/abs/2103.12693) | [:octocat:](https://github.com/ThomasScialom/QuestEval) |
| 13   | BLEU             |  76.3   |  67.3  |      24.6      |  56.1   | [:page\_facing\_up:](https://aclanthology.org/P02-1040/) | [:octocat:](https://www.nltk.org/_modules/nltk/translate/bleu_score.html) |
| 14   | DAE              |  66.8   |  65.7  |      35.1      |  55.8   | [:page\_facing\_up:](https://aclanthology.org/2020.findings-emnlp.322/) | [:octocat:](https://github.com/tagoyal/dae-factuality) |
| 15   | BLEURT           |  69.2   |  71.9  |      24.9      |  55.4   | [:page\_facing\_up:](https://arxiv.org/abs/2004.04696) | [:octocat:](https://github.com/google-research/bleurt) |
| 16   | BERTScore        |  72.1   |  68.6  |      21.9      |  54.2   | [:page\_facing\_up:](https://arxiv.org/abs/1904.09675) | [:octocat:](https://github.com/Tiiiger/bert_score) |
| 17   | SimCSE           |  67.4   |  70.3  |      23.8      |  53.8   | [:page\_facing\_up:](https://arxiv.org/abs/2104.08821) | [:octocat:](https://github.com/princeton-nlp/SimCSE) |
| 18   | FactCC           |  68.8   |  62.7  |      21.2      |  50.9   | [:page\_facing\_up:](https://arxiv.org/abs/1910.12840) | [:octocat:](https://github.com/salesforce/factCC) |
| 19   | BLANC            |  65.1   |  64.0  |      14.4      |  47.8   | [:page\_facing\_up:](https://arxiv.org/abs/2002.09836) | [:octocat:](https://github.com/PrimerAI/blanc) |
| 20   | NER-Overlap      |  60.4   |  59.3  |      18.9      |  46.2   | [:page\_facing\_up:](https://arxiv.org/abs/2111.09525) | [:octocat:](https://github.com/tingofurro/summac) |
| 21   | MNLI             |  47.9   |  60.4  |      3.1       |  37.2   | [:page\_facing\_up:](https://arxiv.org/abs/1704.05426) | [:octocat:](https://github.com/nyu-mll/multiNLI) |
| 22   | FEQA             |  48.3   |  52.2  |      -1.9      |  32.9   | [:page\_facing\_up:](https://arxiv.org/abs/2005.03754) | [:octocat:](https://github.com/esdurmus/feqa) |

\*  SummaC: [\[Paper\]](https://arxiv.org/abs/2111.09525) \| [\[Github\]](https://github.com/tingofurro/summac)

** TRUE: [\[Paper\]](https://arxiv.org/abs/2204.04991) \| [\[Github\]](https://github.com/google-research/true)


# Installation

Our models are trained and evaluated using PyTorch 1.12.1. We recommend using this version to reproduce the results.

1. Please first install the right version of PyTorch before installing `alignscore`.
2. You can install `alignscore` by cloning this repository and `pip install .`.
3. After installing `alignscore`, please use `python -m spacy download en_core_web_sm` to install the required spaCy model (we use `spaCy` for sentenization).

# Evaluating Factual Consistency
To evaluate the factual consistency of the `claim` w.r.t. the `context`, simply use the score method of `AlignScore`.
```python
from alignscore import AlignScore

scorer = AlignScore(model='roberta-base', batch_size=32, device='cuda:0', ckpt_path='/path/to/checkpoint', evaluation_mode='nli_sp')
score = scorer.score(contexts=['hello world'], claims=['hello world'])
```
`model`: the backbone model of the metric. Now, we only provide the metric trained on RoBERTa

`batch_size`: the batch size of the inference

`device`: which device to run the metric

`ckpt_path`: the path to the checkpoint

`evaluation_mode`: choose from `'nli_sp', 'nli', 'bin_sp', 'bin'`. `nli` and `bin` refer to the 3-way and binary classficiation head, respectively. `sp` indicates if the chunk-sentence splitting method is used. `nli_sp` is the default setting of AlignScore


# Checkpoints
We provide two versions of the AlignScore checkpoints: `AlignScore-base` and `AlignScore-large`. The `-base` model is based on RoBERTa-base and has 125M parameters. The `-large` model is based on RoBERTa-large and has 355M parameters. 

**AlignScore-base**: 
https://huggingface.co/yzha/AlignScore/resolve/main/AlignScore-base.ckpt

**AlignScore-large**:
https://huggingface.co/yzha/AlignScore/resolve/main/AlignScore-large.ckpt

# Training  
You can use the above checkpoints directly for factual consistency evaluation. However, if you wish to train an alignment model from scratch / on your own data, use `train.py`.
```python
python train.py --seed 2022 --batch-size 32 \
--num-epoch 3 --devices 0 1 2 3 \
--model-name roberta-large -- ckpt-save-path ./ckpt/ \
--data-path ./data/training_sets/ \
--max-samples-per-dataset 500000
```

`--seed`: the random seed for initialization

`--batch-size`: the batch size for training

`--num-epoch`: training epochs

`--devices`: which devices to train the metric, a list of GPU ids

`--model-name`: the backbone model name of the metric, default RoBERTa-large

`--ckpt-save-path`: the path to save the checkpoint

`--training-datasets`: the names of the training datasets

`--data-path`: the path to the training datasets

`--max-samples-per-dataset`: the maximum number of samples from a dataset

# Benchmarking
Our benchmark includes the TRUE and SummaC benchmark as well as several popular factual consistency evaluation datasets.

To run the benchmark, a few additional dependencies are required and can be installed with `pip install -r requirements.txt`.
Additionally, some depedencies are not available as packages and need to be downloaded manually (please see `python benchmark.py --help` for instructions).

Note installing `summac` may cause dependency conflicts with `alignscore`. Please reinstall `alignscore` to force the correct dependency versions.

The relevant arguments for evaluating AlignScore are:

`--alignscore`: evaluation the AlignScore metric

`--alignscore-model`: the name of the backbone model (either 'roberta-base' or 'roberta-large')

`--alignscore-ckpt`: the path to the saved checkpoint

`--alignscore-eval-mode`: the evaluation mode, defaults to `nli_sp`

`--device`: which device to run the metric, defaults to `cuda:0`

`--tasks`: which tasks to benchmark, e.g., SummEval, QAGS-CNNDM, ...

For the baselines, please see `python benchmark.py --help` for details.
