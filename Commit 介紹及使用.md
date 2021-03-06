# Commit介紹及使用
 >__使用分支可以幫助開發者，以不影響到主支線的前提下來撰寫程式，當分支工作完畢後再將分支合併入主支線內__

將暫存區的檔案提交到儲存庫儲存<br>
```git commit ```<br><br>
說明這次的 commit 做了什麼事，引號裡面的註解中英文皆可<br>
```git commit -m "修改記錄" ```<br>

操作如下
![commit-m](image/commit-m.PNG "Title")
>從回饋裡的訊息可以看到這些提交相關資訊
* 提交到哪個分支（main）
* 提交的 SHA-1 校驗碼（462ceb1）
* 有多少檔案被更動
* 統計此提交有多少列被新增和被移除

``` git commit ```的一些常用變化
|git|do|
|:-----|:-----|
|```git commit -a** ```|如果變更都只是修改檔案內容的話，可省略 ```git add``` 的步驟，直接提交變更|
|```git commit --amend** ```|將變更合併到上次提交中|
|```git commit -s** ```|再提交訊息最後面加上一個 signoff by，某些開源的社群複審時會加上 signoff，例如 Linux Kernel|
|```git commit --allow-empty** ```|在 git log 上留訊息|

