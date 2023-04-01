# Chat2Chart: Generating Visualization Code with LLMs   
Chat2Chart provides a set of three datasets for benchmarking LLMs, two adapted from existing benchmarks ([NLV](https://github.com/nlvcorpus/nlvcorpus.github.io) and [nvBench](https://sites.google.com/view/nvbench/)) and one entirely new named Common Visualization Programming Tasks (CVPT). Each datasets contains a set of (Natual Language Utterance, Vega-Lite Code) pair.

CVPT covers a wide range of visualization techniques, spanning 105 unique examples from the [Vega-Lite gallery](https://vega.github.io/vega-lite/examples/) with varying complexity from basic charts to composite ones. 

![image](https://user-images.githubusercontent.com/14938532/229285040-55edf713-743d-4433-9825-608851b5992b.png)


## Access to Datasets  
/datasets includes three folder for each dataset with a consistent structure:
- corpus.csv stores the NL utterance, ground-truth visualization, and dataset used for each visualization
- datasets.json indexes the dataset used for each visualization
- gptResult.json stores the prompt and response of benchmarking LLMs, including the baseline (GPT-3 Davinci-3), fewshot learning, fine-tuning, and the DataBot method.
- finetune: data used for fine-tuning GPT-3

In our experiment, we hold out the first 5 examples for few-shot learning and the next 400 for fine-tuning. The remaining data is used for testing.

## Demo
[demo.ipynv](https://github.com/Chat2Chart/Chat2Chart/blob/main/demo.ipynb) provides a walk-through to read the data, view the visualization, fine-tune models, and compare results.
