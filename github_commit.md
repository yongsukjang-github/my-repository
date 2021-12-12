visual studio code에서 github commit 하기

1. initialize repository 클릭  
2. commit할 파일 '+' 클릭  
3. 상단 'v' 클릭  
4. 메모 입력 > enter  

```terminal
git remote add origin —http~
git pull
git add .
git commit -m “comment”
git push
```

- 특정 파일 commit

```terminal
git status
git add 파일명
git commit -m '메세지명'
```

```terminal  
git remote -v
```