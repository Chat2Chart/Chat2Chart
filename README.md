# Chat2Chart: Generating Visualization Code with LLMs   
Chat2Chart provides a set of three datasets for benchmarking LLMs, two adapted from existing benchmarks ([NLV](https://github.com/nlvcorpus/nlvcorpus.github.io) and [nvBench](https://sites.google.com/view/nvbench/)) and one entirely new named Common Visualization Programming Tasks (CVPT). Each datasets contains a set of (Natual Language Utterance, Vega-Lite Code) pair.

CVPT covers a wide range of visualization techniques, spanning 105 unique examples from the [Vega-Lite gallery](https://vega.github.io/vega-lite/examples/) with varying complexity from basic charts to composite ones. 

## Access to Datasets  
/datasets includes three folder for each dataset with a consistent structure:
- corpus.csv stores the NL utterance, ground-truth visualization, and dataset used for each visualization
- datasets.json indexes the dataset used for each visualization
- gptResult.json stores the prompt and response of benchmarking LLMs, including the baseline (GPT-3 Davinci-3), fewshot learning, fine-tuning, and the DataBot method.
- finetune: data used for fine-tuning GPT-3

## Demo
Demo.ipynv provides a walk-through to read the data, view the visualization, fine-tune models, and compare results.