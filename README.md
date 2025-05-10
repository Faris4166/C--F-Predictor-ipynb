<img src = "https://raw.githubusercontent.com/Faris4166/Simple-Checklist-Application-in-Python/refs/heads/main/BG.jpg">

# C-F-Predictor-ipynb
หลักการทำงานของโปรเจกต์นี้คือ การแปลงอุณหภูมิจากเซลเซียส (Celsius) เป็นฟาเรนไฮต์ (Fahrenheit) โดยใช้ Machine Learning (Linear Regression) เพื่อสร้างโมเดลในการทำนายความสัมพันธ์ของข้อมูล ซึ่งอธิบายได้เป็นขั้นตอนดังนี้

## 🔧 หลักการทำงาน:

📥1. โหลดข้อมูล (Import Data) นำเข้าข้อมูลจากไฟล์ celsius.csv ซึ่งมี 2 คอลัมน์:
* celsius: อุณหภูมิในองศาเซลเซียส
* fahrenheit: อุณหภูมิในองศาฟาเรนไฮต์

    ```python
    datos = pd.read_csv("celsius.csv")
    ```

🔍2. สำรวจข้อมูล (Exploratory Data Analysis - EDA)
ใช้คำสั่ง `.info()` และ `.head()` เพื่อดูประเภทข้อมูลและตัวอย่างข้อมูล 5 แถวแรก
📊3. การวิเคราะห์ภาพ (Data Visualization)
ใช้ `seaborn` สร้างกราฟ scatterplot เพื่อดูความสัมพันธ์ระหว่างเซลเซียสและฟาเรนไฮต์
ถ้าความสัมพันธ์เป็นเส้นตรง นั่นคือสัญญาณว่า Linear Regression เหมาะสม
🏗️4. สร้างโมเดล (Model Creation)
ใช้ `LinearRegression` จาก `scikit-learn` เพื่อฝึกโมเดลด้วยข้อมูล

    ```python
    X = datos["celsius"]y = datos["fahrenheit"]
    ```
    แยก features และ labels

🧠5. สร้างโมเดล Machine Learning (Linear Regression)
   ```python
      from sklearn.linear_model import LinearRegressionmodel = LinearRegression()model.fit(X.values.reshape(-1, 1), y)
   ```
🔮6. ทำนายและแสดงผลลัพธ์
* ทำนายค่าฟาเรนไฮต์จากเซลเซียส
* วาดกราฟเปรียบเทียบค่าจริงและค่าที่โมเดลทำนาย
---

<div align="center">
  <img src = "https://media.tenor.com/pbJ9b99yp2UAAAAM/lick-anime.gif">
</div>
<div align="center">
    📚 แหล่งข้อมูลอ้างอิง: <a href="https://www.domestika.org/en/courses/5239-introduction-to-ai-with-python">Introduction to AI with Python (Domestika)</a> - คอร์สออนไลน์เบื้องต้นเกี่ยวกับการประยุกต์ใช้ AI ด้วยภาษา Python ซึ่งเป็นแหล่งความรู้พื้นฐานที่สำคัญสำหรับโปรเจกต์นี้ครับ
</div>
<div align="center">
  📚 Data Source Reference: <a href="https://www.domestika.org/en/courses/5239-introduction-to-ai-with-python">Introduction to AI with Python (Domestika)</a> - An introductory online course about applying AI with Python, which provided essential foundational knowledge for this project.
</div>
  
