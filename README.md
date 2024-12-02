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
 ```Source Code index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carousel Fullscreen</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
  body {
    font-family: Arial, sans-serif;
    background-color: #f8f9fa;
    margin: 0;
    padding: 0;
  }

  .carousel-inner img {
    width: 100%; /* ครอบคลุมความกว้างหน้าจอ */
    height: calc(100vh - 56px); /* ปรับขนาดให้พอดีความสูงของหน้าจอ */
    object-fit: contain; /* ทำให้รูปภาพทั้งหมดแสดงผลแบบไม่ถูกตัด */
  }

  .carousel-caption {
    bottom: 15%; /* ขยับตำแหน่งขึ้นเล็กน้อย */
  }

  .carousel-caption h5 {
    font-size: 3rem; /* ขนาดหัวข้อใหญ่ */
    font-weight: bold;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.8);
    color: #fff; /* ตัวอักษรสีขาว */
  }

  .carousel-caption p {
    font-size: 1.2rem;
    color: #f0f0f0;
    text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.8);
  }

  @media (max-width: 768px) {
    .carousel-caption h5 {
      font-size: 2rem;
    }
    .carousel-caption p {
      font-size: 1rem;
    }
  }
</style>
  </head>
  <body>
    <div id="carouselExampleCaptions" class="carousel slide">
      <div class="carousel-indicators">
        <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
        <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
        <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
      </div>
      <div class="carousel-inner">
        <!-- Slide 1 -->
        <div class="carousel-item active">
          <img src="ใส่รูปภาพที่ 1" class="d-block w-100" alt="Slide 1">
          <div class="carousel-caption d-none d-md-block">
            <h5>Slide 1</h5>
            <p>ใส่คำอธิบายรูปภาพที่ 1</p>
          </div>
        </div>
        <!-- Slide 2 -->
        <div class="carousel-item">
          <img src="ใส่รูปภาพที่ 2" class="d-block w-100" alt="Slide 2">
          <div class="carousel-caption d-none d-md-block">
            <h5>Slide 2</h5>
            <p>ใส่คำอธิบายรูปภาพที่ 2</p>
          </div>
        </div>
        <!-- Slide 3 -->
        <div class="carousel-item">
          <img src="ใส่รูปภาพที่ 3" alt="Slide 3">
          <div class="carousel-caption d-none d-md-block">
            <h5>Slide 3</h5>
            <p>ใส่คำอธิบายรูปภาพที่ 3</p>
          </div>
        </div>
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js"></script>
  </body>
</html>
 ```
## 8. ทดลองรันสคริปต์อีกครั้ง
- หลังจากการปรับปรุงโค้ดแล้ว ให้นักเรียนทดลองรันสคริปต์อีกครั้งเพื่อดูการเปลี่ยนแปลงของผลลัพธ์ที่ได้ และตรวจสอบว่าการตกแต่งที่ทำไปนั้นแสดงผลตามที่ต้องการหรือไม่

