# Machine Learning Project: CO2 Time Series Forecasting

Dự án Machine Learning sử dụng phương pháp Direct Multi-step Forecasting để dự báo nồng độ CO2 trong tương lai dựa trên dữ liệu chuỗi thời gian.

## 📋 Mô tả dự án

Dự án này triển khai mô hình dự báo chuỗi thời gian để dự đoán nồng độ CO2 trong khí quyển. Sử dụng phương pháp Direct Multi-step Forecasting với Linear Regression để dự báo nhiều bước thời gian trong tương lai.

## 🛠️ Công nghệ sử dụng

- **Python 3.x**
- **Pandas** - Xử lý và phân tích dữ liệu
- **Matplotlib** - Visualization
- **Scikit-learn** - Machine Learning algorithms
  - Linear Regression
  - Random Forest Regressor
  - Metrics: MAE, MSE, R²

## 📁 Cấu trúc dự án

```
Machine_learning_Project_Co2_Timseries-forecasting/
├── README.md
├── direct_ts.py          # Main implementation file
├── co2.csv              # Dataset CO2
└── requirements.txt     # Dependencies (nếu có)
```

## 📊 Dataset

Dự án sử dụng dataset CO2 với các cột:
- `time`: Thời gian
- `co2`: Nồng độ CO2

## 🔧 Cài đặt

1. Clone repository:
```bash
git clone https://github.com/QuyDatSadBoy/Machine_learning_Project_Co2_Timseries-forecasting.git
cd Machine_learning_Project_Co2_Timseries-forecasting
```

2. Cài đặt dependencies:
```bash
pip install pandas matplotlib scikit-learn
```

## 🚀 Sử dụng

Chạy script chính:
```bash
python direct_ts.py
```

## 🔍 Phương pháp

### Direct Multi-step Forecasting
- **Window Size**: 5 (sử dụng 5 giá trị quá khứ để dự báo)
- **Target Size**: 3 (dự báo 3 bước thời gian trong tương lai)
- **Train/Test Split**: 80/20

### Feature Engineering
Hàm `create_ts_data()` tạo features từ chuỗi thời gian:
- Tạo lag features: `co2_1`, `co2_2`, `co2_3`, `co2_4`
- Tạo target variables: `target_1`, `target_2`, `target_3`

### Model Training
- Sử dụng Linear Regression cho mỗi target
- Training riêng biệt cho từng bước dự báo

## 📈 Evaluation Metrics

Dự án đánh giá mô hình bằng các metrics:
- **R² Score**: Hệ số xác định
- **MSE**: Mean Squared Error
- **MAE**: Mean Absolute Error

## 🔮 Kết quả

Kết quả được in ra console bao gồm:
- R2 scores cho 3 targets
- MSE values cho 3 targets  
- MAE values cho 3 targets

## 🤝 Đóng góp

1. Fork dự án
2. Tạo feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request


## 👨‍💻 Tác giả

**QuyDatSadBoy** - [GitHub Profile](https://github.com/QuyDatSadBoy)

## 🔗 Links

- [Repository](https://github.com/QuyDatSadBoy/Machine_learning_Project_Co2_Timseries-forecasting)
- [Issues](https://github.com/QuyDatSadBoy/Machine_learning_Project_Co2_Timseries-forecasting/issues)

## 📚 Tài liệu tham khảo

- [Scikit-learn Time Series](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.linear_model)
- [Pandas Time Series](https://pandas.pydata.org/docs/user_guide/timeseries.html)
- [Multi-step Forecasting Strategies](https://machinelearningmastery.com/multi-step-time-series-forecasting/)

---

*Dự án được tạo cho mục đích học tập và nghiên cứu về Time Series Forecasting*
