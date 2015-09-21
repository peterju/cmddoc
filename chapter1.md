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
* echo off
* echo %var%
* echo %cd%
* echo %date%
* echo %time%
* echo %date:~0,4%%date:~5,2%%date:~8,2%

## 跳行
* goto 標籤 (須定義標籤，標籤前要有冒號)
* goto :eof (無須定義標籤，直接結束程式之意)

## 呼叫
* 從批次檔中呼叫其他程式 => call xxx
* 呼叫副程式 => call :標籤 參數