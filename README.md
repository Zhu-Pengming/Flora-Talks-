## 爬虫
  1. 确定问题的格式： 视频评论可能有不同的格式，例如以用户名开头，后跟冒号和问题。检查评论的结构以确定问题的开始。

  2. 使用正则表达式或字符串处理函数提取问题： 使用适当的正则表达式或字符串处理函数，从评论中提取问题。确保捕获完整的问题文本。

  3. 确定回答的格式： 确定回答是如何被格式化的，可能以回复用户名开头，后跟冒号和回答。检查评论的结构以确定回答的开始。

  4. 使用正则表达式或字符串处理函数提取回答： 使用适当的正则表达式或字符串处理函数，从评论中提取回答。确保捕获完整的回答文本。

  5. 整理数据成表格： 将问题和相应的回答整理成一个表格。每一行代表一个问题，列包括问题和多个回答，可以使用表格形式或保存为CSV文件。

  6. 标记Up主回答： 如果Up主有回答，可以通过用户名进行标记或添加额外的列来指示是否是Up主的回答。




  训练集为爬虫 ，来源：哔哩哔哩,小红书，微博，
  关键词：盆栽种植

  确保在微调中使用的数据集具有代表性，并涵盖了模型在实际应用中可能面临的各种情况。这有助于提高模型的泛化能力

  评论过滤（Filtering）：
  
  使用情感分析： 利用情感分析工具对评论进行过滤，保留积极或中性的评论。这有助于排除掉负面或不相关的评论。
  定义过滤条件： 设定过滤条件，例如只保留表达兴趣、正面情感或提出问题的评论。这有助于筛选出对你的 chat bot 目标有帮助的内容。
  问题总结（gpt总结）  生成回答（gpt + 作者的回答）
  去除噪声： 删除评论中的广告、链接、重复的内容等噪声，确保模型训练数据的纯净性。

  清理和处理你收集到的数据
  
  使用你收集到的盆栽相关对话数据对模型进行微调。这个过程可以使用监督学习方法，确保模型能够生成与盆栽有关的有意义回答。
  
  设计提示：设计与盆栽相关的提示，以引导用户的提问。这些提示应该涵盖不同方面，如植物养护、疾病诊断、肥料使用等。
  
  集成到 Chat Bot：
  将微调后的模型集成到你的 chat bot 中。确保与用户的交互流畅，模型能够理解并生成符合期望的回答。


  Prefix-Tuning：
      适用场景： 适用于自然语言生成任务(NLG)，如文本生成。
      优势： 通过在输入中添加任务相关的前缀向量，可以在下游任务中进行微调，而无需更新整个模型的参数。
      建议： 如果应用主要涉及到生成性任务，比如为用户提供文本建议或回复，Prefix-Tuning可能是一个不错的选择。
  


数据集：不仅仅是哔哩哔哩，网站，(Image-Text)
搭模型：gpt2, seq2seq
训练：colab
app
