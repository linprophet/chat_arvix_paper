# chat_arvix_paper
基于OpenAI ChatGPT，快速生成一篇文章的中文总结

## feature
1. 基于字体识别的章节分割，确保每个section被独立总结
2. 基于语义sentence的分块chunk，避免了chunk导致的信息损失或重复
3. logger记录，每次会存储openai的调用返回值，避免出现

## quick start
1. 修改主入口的paper_list： 目前支持直接给定 arxiv paper id 自动下载，或给定本地的路径
2. 指定模型
3. ` python pdf_paper_reader_arxiv.py `
```
if __name__ == '__main__':
    paper_list = ["2307.04349", "2307.03109"] #also support use "../data/paper/2307.04349.pdf
    model = "gpt-3.5-turbo-16k-0613"  # ["gpt-3.5-turbo-16k-0613", "gpt-4"]
    generate_summary(paper_list, model)
```

## TODO
1. 打磨summary prompt
