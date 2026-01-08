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
