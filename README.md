# Colorectal-cancer

巨量科學中心統計團隊計畫專案 (節錄部分資訊，完整報告於markdown or pdf)

## introduction

在過去的研究當中，如:Irvin et al.(2019)使用chest radiographs影像資料來區分病人的肺癌種類與有無，而Khalifa et al.(2020)運用特定的基因表達量來區分病人是屬於肺癌中的何種種類，
但尚未有研究嘗試過同時考慮RNA與影像兩者資訊來進行分析，因此該次分析的目的是同時考慮RNA資料與影像資料進入模型，建立一個模型來配適資料，藉以預測病人是否會有大腸直腸癌的復發。

## approach

1. 針對影像資料，Hastie et al.(2011)所介紹的方法，使用病患的大腸直腸癌復發與否與復發時間，來進行重要的特徵變數選擇
![image](https://user-images.githubusercontent.com/99631406/153803104-c234614c-2806-4d9c-a0d0-0f4dcecb46eb.png)

2. RNA當中有些基因的counts數極度稀少，為了避免有過多與大腸直腸癌復發無關的基因變數進入模型，影響後續分析，因此想先運用DESeq2的套件來幫助我們先篩選掉部分非顯著差異表達的基因
![image](https://user-images.githubusercontent.com/99631406/153803060-047b33dd-e8b2-402e-9d50-3275b4958535.png)

3. 做完前處理後，運用機器學習模型 CATCH model

 ![image](https://user-images.githubusercontent.com/99631406/153803144-eb2928e6-8d75-476d-8536-5efc608f83b7.png)


## result
![image](https://user-images.githubusercontent.com/99631406/153803221-83177c42-35f5-47f2-9b27-b1e717f83d7d.png)

