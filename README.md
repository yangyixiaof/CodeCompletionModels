# 博士论文第四章中REP与Pointer-Mixture比较实验数据
REP模型与Pointer-Mixture中的Attention-Pointer的具体比较数据请查阅IJSEKE论文（此论文已经被IJSEKE接收，将在2020年1月底至2月初发表），获取地址为
https://drive.google.com/open?id=1BpaHDzRX2qrNdzYinDQmy4xUhOmQshd7

在小数据集上，Attention-Pointer可以取得比REP略微好一点的效果，但在大数据集上，REP模型的预测精度比Attention-Pointer预测精度略微好一点（预测轮数相同，且往后连续两轮预测精度均没有提升），REP模型的时间开销比Attention-Pointer低8%-25%。我们还发现，将Attention机制实现在REP模型中，决策器算法采用REP的决策算法，Attention机制会降低实验效果。

# 博士论文所有模型下载链接

## 第二章PCC模型实现地址  
[PCC完整实现（附数据集、数据预处理代码、视频和教程）](https://github.com/yangyixiaof/CodeCompletionPlugin)  
  
## 第三章HLM和SLM模型实现下载地址  
[初始TLM实现（附数据集、数据预处理代码和教程）](https://www.dropbox.com/s/8typta3a81htclr/TLM.zip)  
[完整HLM-SLM实现](https://www.dropbox.com/s/sr9zztiwmzicslx/HLM-SLM-REP.zip)  
  
## 第四章REP模型实现下载地址  
[初始REP实现（附数据集、数据预处理代码和教程）](https://www.dropbox.com/s/28p8j44zdc78ob4/REP.zip)  
[改进REP实现（附Pointer-Mixture实现以及对比）](https://www.dropbox.com/s/sr9zztiwmzicslx/HLM-SLM-REP.zip)  
  
## 预处理程序下载地址  
[独立的数据预处理模块](https://www.dropbox.com/s/iafkui5dv9jet2f/JavaCodePreProcess.zip)  
[独立的汇总数据集（不完整，很快会完善）](https://www.dropbox.com/s/wlriqymllx985k8/CodeCorpus.zip)  



