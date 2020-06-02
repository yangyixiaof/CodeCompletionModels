# Download links to all models of my doctoral dissertation

## Chapter 2 PCC model implementation
[PCC implementation (with dataset, data preprocessing code, video and tutorial)](https://github.com/yangyixiaof/CodeCompletionPlugin)  

## Chapter 3 HLM and SLM model implementation
[HLM-SLM implementation (github address, this project is mixed with REP model, containing tutorial)](https://github.com/GrowingCode/FrameTokenMemAtten)  

## Chapter 4 REP model implementation
[REP implementation (github address, this project is mixed with HLM-SLM model, containing tutorial)](https://github.com/GrowingCode/FrameTokenMemAtten)

### Detailed experimental setting and data for comparsion of REP and Pointer-Mixture in Chapter 4 of doctoral dissertation
　　In Chapter 4, REP model (proposed by me) and Pointer-Mixture (proposed by JianLi) are compared. We use the similar setting as Pointer-Mixture meaning that we ignore grammar tokens when learning token repetition. In this experiment, REP model and Pointer-Mixture only consider variables. When preprocessing data, we mark every variable in the sequence and use REP model or Pointer-Mixture to decide whether the variable should be the already existed one or the one in vocabulary table. 
<br>
　　For grammar tokens (non-variable tokens), we use Hierarchical Language Model described in Chapter 3 to further improve the prediction accuracy. This optimization is described at length in Chapter 5 (there may be some confusion in the arrangement of paper content). The final accuracy is the weighted average of the two kinds of tokens (variable-tokens and non-variable tokens). 
<br>
　　Please check [paper](https://doi.org/10.1142/S0218194019400229) and [corrigendum paper](https://arxiv.org/abs/2005.04137) for further details. 

### Explanation for "we learn the repetition patterns of all kinds of tokens." in dissertation: 
　　First of all, for different kinds of tokens, we apply independent REP model to learn token repetition. For example, for grammar tokens, we use one REP model to learn token repetition, for variables, we use another isolated REP model to learn token repetition. 
<br>
* grammar tokens
    * For grammar tokens, we also try to apply REP to learn the token repetition, however, we found that grammar tokens have no regularity of token repetition. When a large number of grammar tokens are not repeated while only a small number of grammar tokens are repeated, this leads to the situation that the model will think all nearly all grammar tokens in test set are not repeated. Thus this is equivalent to directly use traditional language model to predict token. Here we use Hierarchical Language Model as traditional language model.　
<br>
* literals
    * For string literals or char literals or number literals, in test set, most of such tokens are marked UNK. If we think predicting UNK correctly is good, then applying REP will improve the model performance. Otherwise, it will degenerate into a similar situation as grammar tokens due to the reason that few string literals or char literals or number literals are repeated in training set or test set. 

## Data preprocessor implementation
[Data preprocessing module (aim for translating raw java files to the tensor format which REP or HLM-SLM can directly handle, github address, containing tutorial)](https://github.com/GrowingCode/JavaCodePreProcess.git)  
[Data set (note that the separation (train, test, valid) of data set is remaked so the results may differ from the data presented in the dissertation or the already published paper, github address, containing tutorial)](https://github.com/GrowingCode/CodeCorpus.git)  



