�t�X�ڭ̰ѥ[���ɤs�Ȧ橳�UT-Brain���x���|��u�A���i�ä��i�áH�кæ��~������w���v�v�ɡA�N�L�{�����T���q�C
1. �v�ɹL�{��public data (�b���ɶi��ɡA�ϥ�public data���O�ڭ̪��ҫ��w����O)
2. �v�ɹL�{��private data (�b���ɧ��n�A�D���ϥ�private data�������ɵ����̾�)
3. �v�ɵ�����public data (�b���ɵ�����A�ڭ̦�public data���ѵ��A�]���i�H�ۤv�p����ơA�~���i�ڭ̪��ҫ�)

�ϥΤ覡:
�U�軡���U�ɮפ��e�A���@�{��(.ipynb)�ҥi��������C


��Ƨ�-data:�����v�ɩҤ�������Ʈw�A���e�p�U�C
training data�Ppublic data����S�x�����
public_train_x_cdtx0001_full_hashed.csv
public_train_x_ccba_full_hashed.csv
public_train_x_dp_full_hashed.csv
public_train_x_custinfo_full_hashed.csv
public_train_x_remit1_full_hashed.csv
private data����S�x�����
private_x_cdtx0001_full_hashed.csv
private_x_ccba_full_hashed.csv
private_x_remit1_full_hashed.csv
private_x_dp_full_hashed.csv
private_x_custinfo_full_hashed.csv

training data���~��ĵ��(alert_key)
train_x_alert_date.csv
public data���~��ĵ��(alert_key)
public_x_alert_date.csv
private data���~��ĵ��(alert_key)
private_x_alert_date.csv

training data���ѵ�(�~��label)
train_y_answer.csv
public data���ѵ� (�~��label)
24_ESun_public_y_answer.csv

T-brain���x�W�Ǯ榡�d��
sample.csv

�{���X�|�����T���q�C
1. �v�ɹL�{��public data:�o�̨ϥΪ��O�Ĥ@��feature
extract_featuresV1.ipynb :�i����public data���Ĥ@��feature�A�s�ɩ�result/featuresV1.csv�C
Model_FeatureV1.ipynb :���e�]�tRandom Forest/XGB/SVM model�A�i�U�O�ϥΤ]�i�H�ϥ�voting classifier�A�w�]��voter(XGB+SVM)�C
Model_DNN_FeatureV1.ipynb:���e�]�tDNN model�A�@�ϵ��G�A�s�ɩ�result/DNN_acc.png�Bresult/DNN_loss.png�Bresult/DNN_score.png�C

2. �v�ɹL�{��private data:�o�̨ϥΪ��O�Ĥ@��feature
extract_featuresV1_Private.ipynb :�i����private data���Ĥ@��feature�A�s�ɩ�result/featuresV1_Private.csv�C
Model_FeatureV1_Private.ipynb :���e�]�tRandom Forest/XGB/SVM model�A�i�U�O�ϥΤ]�i�H�ϥ�voting classifier�A�w�]��voter(XGB+SVM)�C

3. �v�ɵ�����public data:�o�̨ϥΪ��O�ĤG��feature
extract_featuresV2.ipnb :�i����public data���ĤG��feature�A�s�ɩ�result/featuresV2.csv�C
Model_FeatureV2.ipynb:���e�]�tRandom Forest/XGB/SVM model�A�i�U�O�ϥΤ]�i�H�ϥ�voting classifier�C
utils.py: ���e��Model_FeatureV2.ipynb�һݤ��禡�C

��Ƨ�-result:�x�s�L�{�����ͪ����G�C
1. �v�ɹL�{��public data:
public_combined_data.csv: ��extract_featuresV1.ipynb���X�A�]��extract_featuresV1.ipynb�ҥΡA�O�Ĥ@��Feature�����������C
featuresV1.csv: ��extract_featuresV1.ipynb���X�A�O�Ĥ@��Feature���̲׵��G�A��Model_FeatureV1.ipynb�BModel_DNN_FeatureV1.ipynb�ҥΡC
DNN_acc.png: ��Model_DNN_FeatureV1.ipynb�Ҳ��X�A����DNN accuracy�C
DNN_loss.png: ��Model_DNN_FeatureV1.ipynb�Ҳ��X�A����DNN loss�C
DNN_score.png: ��Model_DNN_FeatureV1.ipynb�Ҳ��X�A����DNN score�C
Public_Prob_FeatureV1.csv: ��Model_FeatureV1.ipynb�Ҳ��X�A�Ω�ú��T-brain���x����ơC

2. �v�ɹL�{��private data:
private_combined_data.csv: ��extract_featuresV1_Private.ipynb���X�A�]��extract_featuresV1_Private.ipynb�ҥΡA�O�Ĥ@��Private Feature�����������C
featuresV1_Private.csv: ��extract_featuresV1_Private.ipynb���X�A�O�Ĥ@��private Feature���̲׵��G�A��Model_FeatureV1_Private.ipynb�ҥΡC
Private_Prob_FeatureV1.csv: ��Model_FeatureV1_Private.ipynb�Ҳ��X�A�Ω�ú��T-brain���x����ơC

3. �v�ɵ�����public data:
alert_key_info.csv: ��extract_featuresV2.ipynb���X�A�]��extract_featuresV2.ipynb�ҥΡA�O�ĤG��Feature�����������C
top_featsV2: ��Model_FeaturesV2.ipynb���X�C
featuresV2.csv: ��extract_featuresV2.ipynb���X�A�O�ĤG��Feature���̲׵��G�A��Model_FeatureV2.ipynb�ҥΡC