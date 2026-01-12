# 臺北市私立薇閣高級中學114學年度第1學期工程專題
## 班級    辛    	座號 30          	姓名 李冠霆 
### 一、主題：
利用matlab的延伸應用之一的deep learning network來訓練模型，並搭配程式碼能夠做出一個可以分辨食物圖像的系統，也就是在輸入圖片到程式時可以根據我的訓練資料並將其分類再隊的類別。舉例來說，我的食物類別有牛肉麵、炸雞、薯條，再給程式薯條的照片時，我會希望他能夠被歸類在”薯條”的分類，其他類同理。這次會嘗試使用兩個不同的神經網路，並在實驗結束後比對兩個神經網路的差異。 
| <img width="430" height="182" alt="Image" src="https://github.com/user-attachments/assets/dc094a0a-c6af-4f73-9ba8-f1cd097470b5" /> |
| :---|
| AlexNet的架構共八層，第一層到第五層是卷積層(CNN)和池化層，第六層到第八層是全連接層，共有5層卷積和3層全連接層
參考網址https://ithelp.ithome.com.tw/m/articles/10301142 |

| <img width="394" height="223" alt="Image" src="https://github.com/user-attachments/assets/317b952d-8f78-43da-8392-eeb766c6926f" /> |
| :---|
|先以1*1卷積壓縮，再用 1*1 與 3*3 卷積擴展特徵，以降低計算量並維持辨識能力
參考網址https://medium.com/@jasonyen1009/ml-squeezenet-db4af454e50b |

### 二、收集資料：（包含資料篩選、資料預處理、格式轉換）
利用網路上的圖庫搜尋 (https://www.istockphoto.com/hk) 食物的圖片，分類有 $\color{red}{\text{炸雞、牛肉麵、薯條}}$
<img width="541" height="129" alt="Image" src="https://github.com/user-attachments/assets/5972245a-a598-40ac-9bae-69118eb2942f" />
| 將大小調至227*227，並轉換至全彩 | 將檔案名統一並有效排列(名字-001、001..)|
| :--- | :--- |
| <img width="351" height="389" alt="Image" src="https://github.com/user-attachments/assets/249fa025-21dc-4aa5-a117-10b4242ce6c2" /> |<img width="351" height="320" alt="Image" src="https://github.com/user-attachments/assets/6c4d1502-a9b9-44d1-af3f-4919c08b0588" /> |

| 將整理好的檔案輸入到事先準備的train資料夾 | 最後結果整齊，檔案大小也一致|
| :--- | :--- |
| <img width="345" height="380" alt="Image" src="https://github.com/user-attachments/assets/d733aa39-330d-42da-a34b-cfc62cc53ab8" /> |<img width="341" height="392" alt="Image" src="https://github.com/user-attachments/assets/b259a640-f518-49a2-912c-b2d8edbedcb8" /> |

### 三、建立模型挖掘資料：
（使用資料探勘或機器學習方法、訓練資料比率、使用參數…等）(兩個模型參數皆固定)
<img width="301" height="410" alt="Image" src="https://github.com/user-attachments/assets/aa18a640-c61c-4605-b067-59c8a77169cf" />
|<img width="382" height="293" alt="Image" src="https://github.com/user-attachments/assets/abedd930-e815-4ba3-afde-3a32c0684f3a" /> |
| :---|
|*Epoch為訓練次數，不用太高，如果訓練過高，容易導致過擬合，也就是在分析訓練資料外的圖片時準確率降低
 |
 |<img width="473" height="339" alt="Image" src="https://github.com/user-attachments/assets/41a65f25-6b38-40d2-8995-825b7d2024ca" /> |
| :---|
|NumFilters = 類別數 每一個 filter 對應一個類別。上圖是alexnet的結構|

### 四、實驗結果（程式碼（含註解）、實驗結果）
### $\color{red}{\text{*Alexnet:}}$
|<img width="605" height="338" alt="Image" src="https://github.com/user-attachments/assets/a5587454-f123-406d-b163-4c9d0aa8f23e" /> |
| :---|
|*配合上述的訓練參數，得到了100%的訓練率but訓練率100%並不代表一定準確，有可是因為類別差異明顯或是圖片數量過少而使訓練率看起來很高，如果要確認訓練效果需搭配準確率來確認是否有好的辨識能力，尤其是對訓練資料外的圖片。|

|<img width="603" height="172" alt="Image" src="https://github.com/user-attachments/assets/f429c57d-04be-4c3c-9567-e9cacf78e4ba" /> |
| :---|
|*這段程式碼的功能是利用訓練完成的深度學習模型進行影像分類。它讀取圖片，並將影像縮放到模型所需的像素。圖片會被輸入到訓練好的神經網路中，取得模型預測的類別以及各分類的機率。之後程式會顯示這張圖片，透過這段程式碼，可以方便地測試模型在單張圖片上的分類結果並視覺化呈現。|
