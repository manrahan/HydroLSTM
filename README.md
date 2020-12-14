# HydroLSTM
Deep Learning (LSTM/GRU) Models with Data for Streamflow Forecasting

## Data
This repo aims to share the models in the paper "A rainfall‐runoff model with LSTM‐based sequence‐to‐sequence learning" and "Distributed long-term hourly streamflow predictions using deep learning–A case study for State of Iowa.". We simply shared one sample data of the catchment of USGS 05389000 Yellow River near Ion, IA in 521_data.csv.  
It is the original data with missing values and no pretreatment such as moving average. The precipitation is in the unit of mm. It is obtained from StaveIV and calculated by zonal statistics operation. The ET is the empirical values for Iowa in the unit of mm/month. The discharge data is from the USGS. and in the unit of m3/s.  
The whole dataset in the paper "Distributed long-term hourly streamflow predictions using deep learning–A case study for State of Iowa" will be shared later.  

## Task
To predict the hourly discharge as good as we can. So, both models are beyond the traditional rainfall-runoff models since we used the current discharge for data assimilation.  

## Models
### Model 1: Encoder-Decoder LSTM (LSTM-seq2seq).
This model have shown strong predictability on the 24 hours predictions as presented in the paper:  
Xiang, Z., Yan, J., & Demir, I. (2020). A rainfall‐runoff model with LSTM‐based sequence‐to‐sequence learning. Water resources research, 56(1), e2019WR025326.  

### Model 2: Neural Runoff Model (NRM).
To solve the bottle-neck problem of the state vector in model 1, we proposed the second model for the prediction of the future 120 hours. The model is presented in the paper:  
Xiang, Z., & Demir, I. (2020). Distributed long-term hourly streamflow predictions using deep learning–A case study for State of Iowa. Environmental Modelling & Software, 104761.
