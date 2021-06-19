# Welcome to GitHub Desktop!

This is your README. READMEs are where you can communicate what your project is and how to use it.

Write your name on line 6, save it, and then head back to GitHub Desktop.

class FreqStack:

    def __init__(self):
        self.ls=[]
        self.freq={}

    def push(self, val: int) -> None:
        self.ls.append(val)
        if val in self.freq:
            self.freq[val]+=1
        else:
            self.freq[val]=0
            self.freq[val]+=1
             
    def pop(self) -> int:
        c=max(self.freq.values())
        for i in range(len(self.ls)-1,-1,-1):
            if(self.freq[self.ls[i]]==c):
                self.freq[self.ls[i]]-=1
                return self.ls.pop(i)
                
        