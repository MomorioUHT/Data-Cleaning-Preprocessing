# Data-Cleaning-Preprocessing
* Example Data: ```loan.csv```

### Features

| Feature | คำแปล / ความหมาย | คำอธิบายเพิ่มเติม |
|---------|-----------------|-----------------|
| **Loan_ID** | รหัสเงินกู้ | หมายเลขอ้างอิงเฉพาะของแต่ละรายการเงินกู้ ใช้เพื่อระบุตัวตนไม่ให้ซ้ำกัน |
| **Gender** | เพศของผู้กู้ | ระบุว่า “ชาย” หรือ “หญิง” |
| **Married** | สถานะการสมรส | บอกว่าผู้กู้ “แต่งงานแล้ว” หรือ “โสด” |
| **Dependents** | จำนวนสมาชิกในครอบครัวที่อยู่ในความดูแล | เช่น บุตร หรือผู้สูงอายุที่ต้องดูแล ระบุเป็นจำนวนคน |
| **Education** | ระดับการศึกษา | ระบุระดับวุฒิการศึกษาของผู้กู้ เช่น “Graduate” (จบปริญญา) หรือ “Not Graduate” (ยังไม่จบปริญญา) |
| **Self_Employed** | สถานะการทำงานอิสระ | บอกว่าผู้กู้เป็น “พนักงานประจำ” หรือ “ประกอบอาชีพอิสระ” |
| **ApplicantIncome** | รายได้ต่อเดือนของผู้กู้หลัก | รายได้เฉลี่ยต่อเดือนของผู้ยื่นกู้ (บาท หรือหน่วยเงินอื่น ๆ) |
| **CoapplicantIncome** | รายได้ต่อเดือนของผู้ร่วมกู้ | รายได้ของผู้ร่วมกู้ (เช่น คู่สมรส หรือญาติ) |
| **LoanAmount** | จำนวนเงินที่ขอกู้ | ระบุจำนวนเงินกู้ที่ผู้ยื่นขอ |
| **Loan_Amount_Term** | ระยะเวลาผ่อนชำระเงินกู้ (เป็นวัน) | เช่น 360 วัน หรือ 480 วัน หมายถึงระยะเวลาทั้งหมดที่ต้องชำระคืน |
| **Credit_History** | ประวัติการชำระหนี้ | ใช้ดูว่าผู้กู้เคยมีการชำระเงินกู้ตรงเวลาหรือไม่ (1 = มีประวัติชำระดี, 0 = ไม่มีประวัติหรือชำระไม่ดี) |
| **Property_Area** | พื้นที่ที่ตั้งทรัพย์สิน | เช่น “Urban” (ในเมือง), “Rural” (ชนบท), หรือ “Semiurban” (กึ่งเมือง) |
| **Loan_Status** | สถานะของเงินกู้ | แสดงผลการอนุมัติ เช่น “Y” = อนุมัติ, “N” = ไม่อนุมัติ |


### Data Cleaning Technique used
* Handling Missing Values
    * continuous features: SimpleImpulter Mean
    * categorial features: SimpleImpulter Most-frequent (Mode)
* Handling Outliers
    * using interquartile range (IQR) to cap out maximum and minimum values
* Scaling
    * using StandardScaler with
        * ApplicantIncome
        * CoapplicantIncome
        * LoadAmount
* One-Hot Encoding categorical features to make data ready for future ML Projects!