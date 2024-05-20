1、在data下新建数据集文件夹，在该文件夹下新建mid_data、raw_data。raw_data下放置数据集文件。

2、在raw_data下新建process.py，主要处理数据为mid_data下的文件，具体可参考上述实例数据集。

3、在preprocess.py定义数据集名和文本最大长度，运行后得到final_data下的文件。

4、程序主入口main.py。

数据集的名称：cner
数据集的地址：data/cner/
总共的字的类别数目：num_tags
是否使用gpu：如果是指定gpu_ids="0"（默认使用第0块），否则指定gpu_ids="-1"
文本的最大长度：max_seq_len，需要和我们在preprocess.py里面指定的保持一致
使用use_bilstm和use_crf分别指定是否使用bilstm和crf模块

需要在hugging face下载chinese-bert-wwm-ext模型，主要是需要vocab.txt、config.json、pytorch_model.bin，放在和该项目同级的model_hub下面。然后我们就可以处理数据为bert所需要的格式了，具体内容在preprocess.py里面