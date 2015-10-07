# 第二章 命令列特性

## 切換目錄：CD
change directory的縮寫，注意絕對路徑與相對路徑的差別，鍵入cd /?可得到更多的說明
```
d: && cd /d c:\windows\system32
```
```
cd "\winnt\profiles\username\programs\start menu"
```

## 轉向
* 命令 > 檔案名稱
* 命令 >> 檔案名稱
* 命令 2>>檔案名稱
* 命令 2>&1
* 命令 < 檔案名稱 => sort < grade.txt
 
## 特殊裝置
nul => ping 168.95.192.1 > nul
con => copy con newfile.txt

## 管線
* 命令1 | 命令2

## 網路資源
* 參考網址 http://steve-jansen.github.io/guides/windows-batch-scripting/index.html