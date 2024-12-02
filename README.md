# ขั้นตอนการทำใบงาน: การสร้างเว็บไซต์ด้วย Carousel ใน Google Apps Script

## 1. เปิดเว็บไซต์ Bootstrap - Carousel
- เริ่มต้นด้วยการเข้าเว็บไซต์ [Bootstrap - Carousel](https://getbootstrap.com/docs/5.3/components/carousel/#how-it-works) และศึกษาเกี่ยวกับ Carousel ที่มีอยู่ในเว็บไซต์นี้

## 2. เลือกการแสดงผล Carousel ที่สนใจ
- เลือกตัวอย่างการแสดงผล Carousel ที่คุณสนใจจากเว็บไซต์ Bootstrap และศึกษาวิธีการใช้งาน โดยอาจเลือกแสดงรูปภาพ ข้อความ หรือเนื้อหาต่างๆ

## 3. เปิด Google Sheets และตั้งชื่อไฟล์
- สร้าง Google Sheets ใหม่ โดยตั้งชื่อและตั้งค่าการอนุญาตต่างๆ เพื่อให้สามารถเข้าถึงได้
![Screenshot 2024-12-02 110357](https://github.com/user-attachments/assets/8c782a88-6210-4685-b166-2ecb5f10acde)

- เปิดใช้ Google Apps Script ผ่านเมนู **ส่วนขยาย > Apps Script**
![Screenshot 2024-12-02 105627](https://github.com/user-attachments/assets/09f2d760-416b-4a1e-bd08-33eff7e44a0d)

## 4. สร้างไฟล์ `Code.gs`
- ใน Google Apps Script ให้สร้างไฟล์ `Code.gs` และเพิ่มโค้ดฟังก์ชัน `doGet(e)` ดังนี้:
    ```javascript
    function doGet(e) {
      return HtmlService.createHtmlOutputFromFile('index');
    }
    ```
- หากมีไฟล์ `Code.gs` อยู่แล้ว ให้นำโค้ดนี้ไปใส่เพื่อเรียกใช้งานไฟล์ HTML ที่จะสร้างในขั้นตอนถัดไป

## 5. สร้างไฟล์ `index.html`
- สร้างไฟล์ใหม่ใน Google Apps Script โดยเลือก **File > New > HTML** ตั้งชื่อว่า `index.html`
![Screenshot 2024-12-02 110937](https://github.com/user-attachments/assets/220edd97-15d3-416b-a33d-c09f76adaf02)
![Screenshot 2024-12-02 111024](https://github.com/user-attachments/assets/f7e38601-dd6d-4396-8290-4703e57b3ccc)
- นำ **source code** สำหรับ Carousel ที่เลือกจากเว็บไซต์ Bootstrap มาวางในไฟล์ `index.html`

## 6. ทดลองรันสคริปต์
- หลังจากที่ได้ตั้งค่าโค้ดทั้งหมดแล้ว ให้ทดลองรันสคริปต์เพื่อดูผลลัพธ์ว่าเกิดอะไรขึ้นบ้าง

## 7. ปรับปรุงและตกแต่งโค้ดใน `index.html`
- ให้นักเรียนปรับแต่งและตกแต่งโค้ดในไฟล์ `index.html` ให้สวยงามตามความคิดสร้างสรรค์ เช่น การเพิ่มรูปภาพ ข้อความ หรือการเปลี่ยนแปลงสีสัน และองค์ประกอบต่างๆ เพื่อให้เหมาะสมกับความต้องการของตนเอง

## 8. ทดลองรันสคริปต์อีกครั้ง
- หลังจากการปรับปรุงโค้ดแล้ว ให้นักเรียนทดลองรันสคริปต์อีกครั้งเพื่อดูการเปลี่ยนแปลงของผลลัพธ์ที่ได้ และตรวจสอบว่าการตกแต่งที่ทำไปนั้นแสดงผลตามที่ต้องการหรือไม่
