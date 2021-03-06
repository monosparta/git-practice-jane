# GitFlow 介紹
>當同一個專案一起開發的人數越來越多，如果沒有訂好規矩，每個人的 Commit 習慣可能都不同，所以便有人提出一套流程讓大家可以遵守

 __根據 Git Flow 的建議，主要的分支有 ```master```、```develop```、```hotfix```、```release``` 以及 ```feature``` 這五種分支__

 * ### Master分支
 用來放穩定、隨時可上線的版本。這個分支的來源只能從別的分支合併過來，開發者不會直接 Commit 到這個分支。因為是穩定版本，所以通常也會在這個分支上的 Commit 上打上版本號標籤。
  * ### Develop分支
 所有開發的基礎分支，當要新增功能的時候，所有的 Feature 分支都是從這個分支切出去的。而 Feature 分支的功能完成後，也都會合併回來這個分支。
  * ### Hotfix分支
 當線上產品發生緊急問題的時候，會從 Master 分支開一個 Hotfix 分支出來進行修復，Hotfix 分支修復完成之後，會合併回 Master 分支，同時也會合併一份到 Develop 分支。
* ### Release分支
當 Develop 分支夠成熟了，就可以把 Develop 分支合併到 Release 分支，在這邊進行算是上線前的最後測試。測試完成後，Release 分支將會同時合併到 Master 以及 Develop 這兩個分支上。Master 分支是上線版本，而合併回 Develop 分支的目的，是因為可能在 Release 分支上還會測到並修正一些問題，所以需要跟 Develop 分支同步，免得之後的版本又再度出現同樣的問題。
* ### Feature分支
開始新增功能的時候使用 Feature 分支， Feature 分支都是從 Develop 分支來的，完成之後會再併回 Develop 分支。

