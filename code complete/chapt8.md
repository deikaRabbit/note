檢查所有輸入到程式的值不論是從外部或是子程式而來，都無法信任必須自己檢查有沒有合法或是安全性的問題
assert 用在開發階段可以幫助我們快速找到問題，可以從 production code 移除避免降低效能
error handling 是用來處理預期會發生問題的情況，assert 則是檢查絕不該發生的問題，一但觸發了 assert 就表示 code 有問題必須要修正
error handler
* 返回中立值：return 0 or '' or nullptr
* 換下一個正確的資料：資料流的處理，等待下一個
* return 與前次相同的
* 換成最接近的合法值
* log message
* return error code：讓呼叫的人處理
* call error handler function：集中處理，但是會有高耦合的問題，會有安全性的問題
* show error message：
* 局部處理：由設計實作的工程師決定該怎麼處理，但是有可能會讓 show error message 散佈在整個系統中
* shutdown：

健全性 or 正確性
健全性：無論如何都要讓功能可以持續運作下去
正確性：回傳正確的資料才是重要的，不回傳也比傳錯好
不同性質的軟體會有不同的傾向