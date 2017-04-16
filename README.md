這是什麼？
========
給定一個作者針對特定一類文學寫成的中文作品，本作試圖透過機器學習的方法建立一個文風辨識器，自動辨認一個作品是否屬於該作者的該類文學作品。

什麼是文風？
========
文風目前仍難以精確定義，在本作中，我們利用慣用詞彙作為文風的代表特徵，因此這裡的文風更接近所謂的「用詞習慣」。

怎麼安裝？
========
直接將本作全部下載或 clone 下來即可。

怎麼使用？
========
1. 將文本準備好後，先以 cut_into_dic.py 將文本分詞並存為 dic 檔。

        python3 cut_into_dic.py [文本檔案位置] [輸出的 dic 檔的位置]

2. 生成完所有 dic 檔後，修改 filepaths.py 的內容。

3. 生成關鍵詞文件，檔名可以自取。本作中使用了 grep_topwords.py 工具，修改內部的 dic_list 變數，將想要抽取關鍵字的文本加入變數內，再直接執行即可，結果直接印在標準輸出界面上。

        python3 grep_topwords.py

4. 修改 run_test.py，更改初始 open 時目標檔案路徑到已經生成的關鍵詞文件，並指定 to_train (訓練用文本) 與 to_test (測試文本)
的內容，原則上只要內容和 filepaths.py 定義的一致即可。

5. 執行 run_test.py，目前結果會直接印在標準輸出界面上。

        python3 run_test.py

技術細節
========
想獲得詳盡的說明，或者了解這個作品的更多延伸功能，請閱讀下篇內容。
https://drive.google.com/open?id=0B3AB2cDxZCwhQ3lDWHlCNUpxWlNyMldqRUJpUXdKcWVsX3Bv
