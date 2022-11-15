# wmv_to_mp4
::【指令說明】 
:: ffmpeg 啟用 FFmpeg（即「ffmpeg.exe」） 
:: -i   = 輸入檔案，後面接你要轉的檔案  
:: -c:v = 指定影片編碼器  
:: -c:a = 指定音訊編碼器  
:: -c:s = 指定字幕編碼器  
:: libx265 = h265編碼器的名稱  
:: aac     = AAC編碼器的名稱  
:: copy    = 不做轉檔直接複製   
:: c = codec(編碼器)  
:: v = video  
:: a = audio  
:: s = subtilte(字幕)  

::【FFmpeg基本格式】 
:: ffmpeg -i [輸入影片] -c:v [影片編碼器] [影片參數] -c:a [音訊編碼器] [音訊參數]  [輸出檔案]  
:: ffmpeg -i input.MOV -c:v libx264 -c:a aac output.mp4  

:: -r   設定fps  
:: -crf 是 x264 的參數  
:: -ar  設置音頻採樣頻率  
:: -q:a 設置音頻質量  

:: %~nx1 - 只將 %1 擴展到文件名和擴展名  
:: %~n1  - 僅將 %1 擴充到一個文件名  
:: ffmpeg -i %~nx1 -c:v libx264 -crf 23 -c:a aac -q:a 100 %~n1.mp4  
