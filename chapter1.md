# 批次檔介紹
批次檔的編寫都是純文字檔，盡量使用ANSI的編碼方式，建議使用 [NotePad++](https://notepad-plus-plus.org/) 之類的有語法提示的純文字編輯器編寫

## 副檔名
* bat
* cmd

## 註解方式
* rem
* :

## 切換目錄
* d: && cd /d c:\windows\system32
* cd "\winnt\profiles\username\programs\start menu"

## 變數設定
* 觀察環境變數 => set
* 設定環境變數 => set var=value
* 取消環境變數 => set var=
* 變數的運算 => set /a var+=3
* 輸入時的字串提示 => set /p var=Please input your age:
* 建立新的shell執行指令後返回 => cmd /c 命令

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