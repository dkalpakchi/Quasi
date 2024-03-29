# Quasi

This is the official repository for the article ["Quasi: a synthetic Question-Answering dataset in Swedish using GPT-3 and zero-shot learning"](https://openreview.net/pdf?id=lGFed4WfQWg) accepted to NoDaLiDa 2023.

The structure of the repository is as follows:
- `raw` folder contains the initial textual data from SFI national tests (`sfi.jsonl`) and all non-filtered MCQs generated by GPT-3 to these texts (`generated.jsonl`)
- `annotated` folder contains our annotations to the MCQs in `generated.jsonl`, along with the MCQs themselves in the file `all.json`. For convenience the file is split into two parts:
  - `quasi.json` with the actual Quasi dataset with MCQs judged to be of sufficient quality (`quasi_formatted.json` is a pretty printed readable version of the dataset)
  - `poor_quality.json` - the remainder of MCQs with problems (`poor_quality_formatted.json` is a pretty printed readable version)
- `synthesize.py` contains the source code used to generate MCQs with GPT-3.
