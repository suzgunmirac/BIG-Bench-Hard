# BIG-Bench Hard
![BBH-Results](https://github.com/suzgunmirac/BIG-Bench-Hard/blob/main/figures/bbh-results.png)

## Abstract
[BIG-Bench](https://github.com/google/BIG-bench) [(Srivastava et al., 2022)](https://arxiv.org/abs/2206.04615) is a diverse evaluation suite that focuses on tasks believed to be beyond the capabilities of current language models. Language models have already made good progress on this benchmark, with the best model in the BIG-Bench paper outperforming average reported human-rater results on 65% of the BIG-Bench tasks via few-shot prompting. But on what tasks do language models fall short of average human-rater performance, and are those tasks actually unsolvable by current language models?

[In this work](https://arxiv.org/abs/2210.09261), we focus on a suite of 23 challenging BIG-Bench tasks which we call **BIG-Bench Hard (BBH)**. These are the task for which prior language model evaluations did not outperform the average human-rater. We find that applying chain-of-thought (CoT) prompting to BBH tasks enables PaLM to surpass the average humanrater performance on 10 of the 23 tasks, and Codex (code-davinci-002) to surpass the average human-rater performance on 17 of the 23 tasks. Since many tasks in BBH require multi-step reasoning, few-shot prompting without CoT, as done in the BIG-Bench evaluations (Srivastava et al., 2022), substantially underestimates the best performance and capabilities of language models, which is better captured via CoT prompting. As further analysis, we explore the interaction between CoT and model scale on BBH, finding that CoT enables emergent task performance on several BBH tasks with otherwise flat scaling curves.

## BBH Data
All the task files are under the directory `/bbh`.

## CoT Prompts
All the chain-of-thought (CoT) prompt files are under the directory `/cot-prompts`

![BBH-CoT-Prompts](https://github.com/suzgunmirac/BIG-Bench-Hard/blob/main/figures/bbh-setup.png)

## Codex Results
The outputs from the Codex (code-davinci-002) model are under the directory `/code-davinci-002-outputs`.

![BBH-Codex-Outputs](https://github.com/suzgunmirac/BIG-Bench-Hard/blob/main/figures/bbh-model-outputs.png)

## Citation
If your research makes use of our data or results, please consider citing our paper as well as the BIG-Bench paper.

**BIG Bench** ([_Beyond the Imitation Game: Quantifying and Extrapolating the Capabilities of Language Models_ (Srivastava et al., 2022)](https://arxiv.org/abs/2206.04615))
```
@article{srivastava2022beyond,
  title={Beyond the Imitation Game: Quantifying and extrapolating the capabilities of language models},
  author={Srivastava, Aarohi and Rastogi, Abhinav and Rao, Abhishek and Shoeb, Abu Awal Md and Abid, Abubakar and Fisch, Adam and Brown, Adam R and Santoro, Adam and Gupta, Aditya and Garriga-Alonso, Adri{\`a} and others},
  journal={arXiv preprint arXiv:2206.04615},
  year={2022}
}
```

**BIG-Bench Hard** ([_Challenging BIG-Bench Tasks and Whether Chain-of-Thought Can Solve Them_ (Suzgun et al., 2022)](https://arxiv.org/abs/2210.09261))
```
@article{suzgun2022challenging,
  title={Challenging BIG-Bench Tasks and Whether Chain-of-Thought Can Solve Them},
  author={Suzgun, Mirac and Scales, Nathan and Sch{\"a}rli, Nathanael and Gehrmann, Sebastian and Tay, Yi and Chung, Hyung Won and Chowdhery, Aakanksha and Le, Quoc V and Chi, Ed H and Zhou, Denny and and Wei, Jason},
  journal={arXiv preprint arXiv:2210.09261},
  year={2022}
}
```