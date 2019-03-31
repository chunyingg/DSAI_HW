# DSAI_HW1

## forecasting.ipynb 固定鏈結
https://nbviewer.jupyter.org/gist/chunyingg/5cbac6c691ab7cf69487feb79b8dd4a8/forecasting.ipynb


## 資料集
主要使用 '高峰值2019.csv' 作為訓練集<br>
內容包含2019年1/1~3/30的電力高峰值資料

## 預測模型
LSTM(Long Short-Term Memory)<br>
長短期記憶網路<br>
因其適合用來處理時間序列的數據，故選擇之<br>
將訓練好的模型儲存為my_model.h5以確定每次結果會固定

## 預測方法
1.將資料正規化<br>
2.利用前30天的 '尖峰負載(MW)' 作為X_train <br>
3.而未來7天的 '尖峰負載(MW)' 作為Y_train <br>
4.將資料打散，目的為使之不要按照日期排序影響訓練<br>
5.先預測3/31,4/1的電力高峰值 <br>
6.最後使用4/2前30天的資料讓模型預測最後得到預測結果
