任务一：完成wordcount函数
```python
text = """
Got this panda plush toy for my daughter's birthday,
who loves it and takes it everywhere. It's soft and
super cute, and its face has a friendly look. It's
a bit small for what I paid though. I think there
might be other options that are bigger for the
same price. It arrived a day earlier than expected,
so I got to play with it myself before I gave it
to her.
"""

def wordcount(text):
    # 去除标点符号并将字符串转换为小写  
    cleaned_string = text.replace(',', '').replace('.', '').replace('\n', '').replace('?', '').lower()  
      
    # 分割字符串获取单词列表  
    words = cleaned_string.split()  
      
    # 统计每个单词出现的次数  
    word_count = {}  
    for word in words:  
        if word in word_count:  
            word_count[word] += 1  
        else:  
            word_count[word] = 1
    
    return word_count


if __name__ == "__main__":
    print(wordcount(text))
```

任务二：Debug流程
![image](https://github.com/llkn-2/InternLM-camp/blob/main/assets/Debug.png)
