配合我們參加的玉山銀行底下T-Brain平台所舉辦「你說可疑不可疑？－疑似洗錢交易預測」競賽，將過程分為三階段。
1. 競賽過程中public data (在比賽進行時，使用public data測是我們的模型預測能力)
2. 競賽過程中private data (在比賽尾聲，主辦方使用private data做為比賽評分依據)
3. 競賽結束後public data (在比賽結束後，我們有public data的解答，因此可以自己計算分數，繼續精進我們的模型)

使用方式:
下方說明各檔案內容，任一程式(.ipynb)皆可直接執行。


資料夾-data:本次競賽所公布的資料庫，內容如下。
training data與public data關於特徵的資料
public_train_x_cdtx0001_full_hashed.csv
public_train_x_ccba_full_hashed.csv
public_train_x_dp_full_hashed.csv
public_train_x_custinfo_full_hashed.csv
public_train_x_remit1_full_hashed.csv
private data關於特徵的資料
private_x_cdtx0001_full_hashed.csv
private_x_ccba_full_hashed.csv
private_x_remit1_full_hashed.csv
private_x_dp_full_hashed.csv
private_x_custinfo_full_hashed.csv

training data的洗錢警示(alert_key)
train_x_alert_date.csv
public data的洗錢警示(alert_key)
public_x_alert_date.csv
private data的洗錢警示(alert_key)
private_x_alert_date.csv

training data的解答(洗錢label)
train_y_answer.csv
public data的解答 (洗錢label)
24_ESun_public_y_answer.csv

T-brain平台上傳格式範例
sample.csv

程式碼會對應三階段。
1. 競賽過程中public data:這裡使用的是第一版feature
extract_featuresV1.ipynb :可產生public data的第一版feature，存檔於result/featuresV1.csv。
Model_FeatureV1.ipynb :內容包含Random Forest/XGB/SVM model，可各別使用也可以使用voting classifier，預設為voter(XGB+SVM)。
Model_DNN_FeatureV1.ipynb:內容包含DNN model，作圖結果，存檔於result/DNN_acc.png、result/DNN_loss.png、result/DNN_score.png。

2. 競賽過程中private data:這裡使用的是第一版feature
extract_featuresV1_Private.ipynb :可產生private data的第一版feature，存檔於result/featuresV1_Private.csv。
Model_FeatureV1_Private.ipynb :內容包含Random Forest/XGB/SVM model，可各別使用也可以使用voting classifier，預設為voter(XGB+SVM)。

3. 競賽結束後public data:這裡使用的是第二版feature
extract_featuresV2.ipnb :可產生public data的第二版feature，存檔於result/featuresV2.csv。
Model_FeatureV2.ipynb:內容包含Random Forest/XGB/SVM model，可各別使用也可以使用voting classifier。
utils.py: 內容為Model_FeatureV2.ipynb所需之函式。

資料夾-result:儲存過程中產生的結果。
1. 競賽過程中public data:
public_combined_data.csv: 由extract_featuresV1.ipynb產出，也由extract_featuresV1.ipynb所用，是第一版Feature的中間產物。
featuresV1.csv: 由extract_featuresV1.ipynb產出，是第一版Feature的最終結果，由Model_FeatureV1.ipynb、Model_DNN_FeatureV1.ipynb所用。
DNN_acc.png: 由Model_DNN_FeatureV1.ipynb所產出，紀錄DNN accuracy。
DNN_loss.png: 由Model_DNN_FeatureV1.ipynb所產出，紀錄DNN loss。
DNN_score.png: 由Model_DNN_FeatureV1.ipynb所產出，紀錄DNN score。
Public_Prob_FeatureV1.csv: 由Model_FeatureV1.ipynb所產出，用於繳交T-brain平台的資料。

2. 競賽過程中private data:
private_combined_data.csv: 由extract_featuresV1_Private.ipynb產出，也由extract_featuresV1_Private.ipynb所用，是第一版Private Feature的中間產物。
featuresV1_Private.csv: 由extract_featuresV1_Private.ipynb產出，是第一版private Feature的最終結果，由Model_FeatureV1_Private.ipynb所用。
Private_Prob_FeatureV1.csv: 由Model_FeatureV1_Private.ipynb所產出，用於繳交T-brain平台的資料。

3. 競賽結束後public data:
alert_key_info.csv: 由extract_featuresV2.ipynb產出，也由extract_featuresV2.ipynb所用，是第二版Feature的中間產物。
top_featsV2: 由Model_FeaturesV2.ipynb產出。
featuresV2.csv: 由extract_featuresV2.ipynb產出，是第二版Feature的最終結果，由Model_FeatureV2.ipynb所用。