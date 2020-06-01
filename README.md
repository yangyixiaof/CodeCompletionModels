# Detailed experimental setting and data in Chapter 4 of doctoral dissertation
In Chapter 4, REP model (proposed by me) and Pointer-Mixture (proposed by JianLi) are compared. We use the similar setting as Pointer-Mixture meaning that we ignore grammar tokens when learning token repetition. In this experiment, REP model and Pointer-Mixture only consider variables. When preprocessing data, we mark every variable in the sequence and use REP model or Pointer-Mixture to decide whether the variable should be the already existed one or the one in vocabulary table. 
For grammar tokens (non-variable tokens), we use Hierarchical Language model described in Chapter 3 to further improve the prediction accuracy. This optimization is described at length in Chapter 5 (there may be some confusion in the arrangement of papers). The final accuracy is the weighted average of the two kinds of tokens (variable-tokens and non-variable tokens). 
Please check [paper](https://doi.org/10.1142/S0218194019400229) and [corrigendum paper](https://arxiv.org/abs/2005.04137) for further details. 


# Download links to all models of doctoral dissertation

## Chapter 2 PCC model implementation
[PCC implementation (with dataset, data preprocessing code, video and tutorial)](https://github.com/yangyixiaof/CodeCompletionPlugin)  

## Chapter 3 HLM and SLM model implementation
[HLM-SLM implementation (github address, this project is mixed with REP model, containing tutorial)](https://github.com/GrowingCode/FrameTokenMemAtten)  

## Chapter 4 REP model implementation
[REP implementation (github address, this project is mixed with HLM-SLM model, containing tutorial)](https://github.com/GrowingCode/FrameTokenMemAtten)

## Preprocessor implementation
[Data preprocessing module (translate raw java files to the format which REP or HLM-SLM can directly handle, github address, containing tutorial)](https://github.com/GrowingCode/JavaCodePreProcess.git)  
[Data set (used in dissertation, the separation of data set is remaked so the results may differ from the data presented in paper, github address, containing tutorial)](https://github.com/GrowingCode/CodeCorpus.git)  



