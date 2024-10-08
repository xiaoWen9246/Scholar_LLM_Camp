


# Python实现wordcount

```python


import re

def word_count(text:str) -> dict:
    if text is None:
        return None
    #去除标点符号，只保留字母和空格
    text = re.sub(r'[^\w\s]','',text.lower())
    words = text.split()
    word_freq = {}
    
    for word in words:
        word_freq[word] = word_freq.get(word, 0) + 1
    
    return word_freq

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

print(word_count(text))

{'got': 2, 'this': 1, 'panda': 1, 'plush': 1, 'toy': 1, 'for': 3, 'my': 1, 'daughters': 1, 'birthday': 1, 'who': 1, 'loves': 1, 'it': 5, 'and': 3, 'takes': 1, 'everywhere': 1, 'its': 3, 'soft': 1, 'super': 1, 'cute': 1, 'face': 1, 'has': 1, 'a': 3, 'friendly': 1, 'look': 1, 'bit': 1, 'small': 1, 'what': 1, 'i': 4, 'paid': 1, 'though': 1, 'think': 1, 'there': 1, 'might': 1, 'be': 1, 'other': 1, 'options': 1, 'that': 1, 'are': 1, 'bigger': 1, 'the': 1, 'same': 1, 'price': 1, 'arrived': 1, 'day': 1, 'earlier': 1, 'than': 1, 'expected': 1, 'so': 1, 'to': 2, 'play': 1, 'with': 1, 'myself': 1, 'before': 1, 'gave': 1, 'her': 1}

```

# Vscode连接InternStudio debug笔记
1. 设置断点

![QQ_1727757146341](https://github.com/user-attachments/assets/d3b88ddd-5aef-4f54-adcf-b28c5b9fe48b)

2. 启动debug

![QQ_1727757207746](https://github.com/user-attachments/assets/3d7a7a61-5ee4-4d45-8327-cd519dc37d5f)

3. 查看变量

![QQ_1727757691718](https://github.com/user-attachments/assets/4604a9f0-5a16-4c41-8bbf-1828278074f1)


4. 单步执行代码

![QQ_1727757936627](https://github.com/user-attachments/assets/f4ccc455-4484-4b7b-9e15-b583479dfa28)



