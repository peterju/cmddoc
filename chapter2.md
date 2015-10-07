# 第二章 命令列特性


## 切換目錄：CD
change directory的縮寫，注意絕對路徑與相對路徑的差別，鍵入cd /?可得到更多的說明
```
d: && cd /d c:\windows\system32
```
```
cd "\winnt\profiles\username\programs\start menu"
```

## 變數設定
Windows作業系統環境的變數都是全域變數，我們可以透過下面的指令觀察有哪些環境變數。
```
set
```

設定變數時，一樣使用 set 指令，取用變數時，則需在變數前後加上%
```
set myname=Peter
echo %myname%
```
* 取消環境變數 => set var=
* 變數的運算 => set /a var+=3
* 輸入時的字串提示 => set /p var=Please input your age:

其他的進階用法，請輸入 set /? 來獲得。

因為全域變數會交互影響，因此要模擬區域變數或指令執行之後不影響目前環境，我們會呼叫一個新的 cmd 來執行一次性指令之後返回。

* 建立新的shell執行指令後返回 => cmd /c 命令

請在命令提示字元視窗下練習輸入下面的指令
```
prompt Level1$g
cmd
prompt Level2$g
cmd
prompt Level3$g
exit
exit
```
* 更改提示字元用法 => prompt /?


## 顯示
* 停止回應 => echo off
* 空一行 => echo.
* 顯示var變數內容 => echo %var%
* 顯示當前目錄 => echo %cd%
* 顯示日期 => echo %date%
* 顯示時間 => echo %time%
* 顯示擷取字串 => echo %date:~0,4%%date:~5,2%%date:~8,2%

## 跳行
* goto 標籤 (須定義標籤，標籤前要有冒號)
* goto :eof (無須定義標籤，直接結束程式之意)

## 呼叫
* 從批次檔中呼叫其他程式 => call xxx
* 呼叫副程式 => call :標籤 參數
* 擴充支援 => call /? (http://inpega.blogspot.tw/2012/07/cd-dp0.html)

## 傳回值
* if errorlevel 1
* if %errorlevel%==1
* 命令1失敗才執行命令2 => 命令1 || 命令2

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