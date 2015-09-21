# 批次檔介紹

## 副檔名
* bat
* cmd

## 註解方式
* rem
* :

## 切換目錄
cd /d
cd "\winnt\profiles\username\programs\start menu"

## 變數設定
* set var=value
* set
* cmd /c

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

## 轉向
* 命令 > 檔案名稱
* 命令 >> 檔案名稱
* 命令 2>>檔案名稱
* 命令 2>&1
* 命令 < 檔案名稱
 
## 特殊裝置
nul => ping 168.95.192.1 > nul
con => copy con newfile.txt

## 管線
* 命令1 | 命令2
 