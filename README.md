# NER-Bert-BiLSTM-CRF：修正了原代码中stack时张量维度不一致问题
其实没有什么特别大的改动，唯一的改动就是data_loader.py中的__getitem__，所以就不做什么特别详细的说明了


## 目录结构
```
--checkpoint：模型和配置保存位置
----sample
--------xx.json
--------xx.bin
--model_hub：预训练模型
----chinese-bert-wwm-ext:
--------vocab.txt
--------pytorch_model.bin
--------config.json
--data：存放数据
----sample
--------ner_data：处理之后的数据
------------labels.txt：标签
------------train.txt：训练数据
------------dev.txt：测试数据
--config.py：配置
--model.py：模型
--process.py：处理ori数据得到ner数据
--predict.py：加载训练好的模型进行预测
--main.py：训练和测试
```

如果现在正在进行的上传没出意外的话，应该会把代码打包，里面会有bert模型的权重，如果出了意外，就只能重新找一个中文模型了

再把原repo🐎一下：[点这里](https://github.com/taishan1994/BERT-BILSTM-CRF)

如果有数据格式上的问题，记得再找一下自己的repo，应该也会传上来的
