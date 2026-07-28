# Kittisak Satitkulrat — IT Internship Portfolio

เว็บไซต์พอร์ตโฟลิโอส่วนตัวสำหรับใช้สมัครฝึกงาน/สหกิจศึกษาสาย IT (Cloud, DevOps, Web Development)
ของ **กิตติศักดิ์ สถิตย์กุลรัตน์** นักศึกษาชั้นปีที่ 4 คณะเทคโนโลยีสารสนเทศและนวัตกรรม มหาวิทยาลัยกรุงเทพ

## ✨ Features

- ดีไซน์โทนอบอุ่น สบายๆ (warm & cozy) พื้นครีม สีเน้นส้มอิฐ (terracotta) การ์ดโค้งมนเงานุ่มๆ
- Responsive รองรับมือถือ/แท็บเล็ต/เดสก์ท็อป
- Sections ครบ: About, Education, Skills, Projects, UI/UX Design, Activities, Certificates, Contact
- Scrollspy navbar (ไฮไลต์เมนูตามตำแหน่งที่เลื่อนอยู่)
- Scroll-reveal animation แบบเรียบๆ ไม่หวือหวา
- ระบบ fallback รูปภาพ — จุดไหนยังไม่มีไฟล์รูปจริงจะโชว์ไอคอนสำรองแทนอัตโนมัติ ไม่ขึ้นเป็นรูปแตก
- ไม่มี dependency ฝั่ง build — เป็น HTML/CSS/JS ล้วน เปิดใช้งานได้ทันที

## 📁 โครงสร้างไฟล์

```
kittisak-portfolio/
├── index.html          หน้าเว็บหลัก (ทุก section)
├── css/
│   └── style.css       สไตล์ทั้งหมด (ธีม, layout, responsive, animation)
├── js/
│   └── script.js       ปฏิสัมพันธ์ (navbar, scrollspy, reveal, typed text)
├── assets/             โฟลเดอร์สำหรับรูปภาพ/ไฟล์ประกอบ (ว่าง รอใส่รูปจริง)
└── README.md
```

## 🚀 วิธีใช้งาน / เปิดเว็บไซต์

**วิธีที่ง่ายที่สุด:** ดับเบิลคลิกไฟล์ `index.html` เพื่อเปิดในเบราว์เซอร์ได้ทันที

**หรือรันผ่าน local server (แนะนำเวลาพัฒนาเพิ่ม):**

```powershell
# วิธีที่ 1: ใช้สคริปต์ PowerShell ที่แถมมาให้ (ไม่ต้องติดตั้งอะไรเพิ่ม)
powershell -ExecutionPolicy Bypass -File .\serve.ps1 -Port 8080
# แล้วเปิดเบราว์เซอร์ไปที่ http://localhost:8080

# วิธีที่ 2: ใช้ Python (ถ้าเครื่องมี Python ติดตั้งอยู่)
python -m http.server 5500
# แล้วเปิดเบราว์เซอร์ไปที่ http://localhost:5500
```

หรือใช้ส่วนขยาย **Live Server** ใน VS Code แล้วคลิก "Go Live"

## 🖼️ การใส่รูปภาพจริง (สำคัญ — ยังไม่ได้ใส่)

หน้าเว็บถูกเตรียม `<img>` ไว้ให้ครบทุกจุดแล้ว (Projects, UI/UX Design, Activities, Certificates)
แต่ **ยังไม่มีไฟล์รูปจริงอยู่ในโฟลเดอร์ `assets/`** เพราะรูปที่ส่งมาทางแชทไม่สามารถบันทึกเป็นไฟล์ในเครื่องให้อัตโนมัติได้
(ไม่มีชื่อไฟล์ต้นฉบับติดมาด้วย) ระหว่างนี้แต่ละจุดจะโชว์เป็นไอคอนสำรอง (fallback) แทนโดยอัตโนมัติ ไม่ขึ้นเป็นรูปแตก

**วิธีใส่รูปจริง:** นำไฟล์รูปที่มีไปเซฟใน `assets/` โดยตั้งชื่อไฟล์และนามสกุลให้ตรงกับตารางด้านล่างเป๊ะๆ
แค่นั้นรูปจะขึ้นแทนไอคอนทันทีโดยไม่ต้องแก้โค้ดเพิ่ม:

| ตำแหน่งในเว็บ | ชื่อไฟล์ที่ต้องใช้ | รูปที่ควรใส่ |
|---|---|---|
| หน้าแรก (Hero) → รูปโปรไฟล์ | `assets/profile-photo.jpg` | รูปโปรไฟล์/รูปถ่ายของกิตติศักดิ์ |
| Projects → E-Sports (การ์ดซ้าย) | `assets/project-esports-screenshot.png` | สกรีนช็อตหน้าเว็บระบบ E-Sports 2025 (หน้า ลงทะเบียน/ดูทีม/Admin) |
| Projects → WALLET-TRACK | `assets/project-wallet-track-screenshot.png` | สกรีนช็อตหน้าเว็บ WALLET-TRACK (Expense Tracker) |
| Projects → BEEFOOD | `assets/project-beefood-screenshot.png` | สกรีนช็อตหน้าเว็บสั่งอาหารออนไลน์ BEEFOOD |
| UI/UX Design → E-Commerce | `assets/design-ecommerce-clothing.jpg` | ภาพ mockup แอปร้านขายเสื้อผ้าธีมชมพู |
| UI/UX Design → Campus Smart Parking | `assets/design-campus-parking.jpg` | ภาพ flow Figma "Campus One" (จอมือถือหลายจอต่อกัน) |
| UI/UX Design → Daily UI 10 Days | `assets/design-daily-ui-challenge.jpg` | ภาพรวม 10 การ์ด Day 1–10 |
| Activities → รูปที่ 1 | `assets/activity-jobfair-booth.jpg` | รูปกลุ่มคนคุยกันที่บูธงาน Mini Job Fair (มีตัวมาสคอตอยู่ด้านหลัง) |
| Activities → รูปที่ 2 | `assets/activity-career-expo.jpg` | รูปถือนามบัตรยืนหน้าบูธ (ป้าย "able") |
| Activities → รูปที่ 3 | `assets/activity-ai-day.jpg` | รูปยืนหน้าป้าย "IT EMPOWERING DAY 2026" |
| Certificates → รูปที่ 1 | `assets/cert-cybersecurity-foundation.png` | ใบ Cybersecurity Foundation Course (NCSA/THNCA) |
| Certificates → รูปที่ 2 | `assets/cert-thailand-cyber-top-talent.jpg` | ใบ Thailand Cyber Top Talent 2023 (NCSA/Huawei) |
| Certificates → รูปที่ 3 | `assets/cert-sololearn-html.jpg` | ใบ Sololearn HTML Course |
| Certificates → รูปที่ 4 | `assets/cert-great-learning-html-tags.png` | ใบ Great Learning Academy — HTML Attributes and Tags |
| Certificates → รูปที่ 5 | `assets/cert-borntodev-devlab3.png` | ใบ borntoDev DevLab 3 |
| Certificates → รูปที่ 6 | `assets/cert-hackerrank-css.png` | ใบ HackerRank CSS Certificate |

> นามสกุลไฟล์ต้องตรงกับที่ระบุไว้ข้างบนเป๊ะๆ (ส่วนใหญ่เป็น `.jpg` ยกเว้น certificate 4 ใบข้างต้นที่เป็น `.png`)
> ถ้าไฟล์จริงของคุณเป็นนามสกุลอื่น ให้แก้ใน `index.html` ตรงจุดนั้นให้ตรงกับไฟล์จริงด้วย
> (ค้นหาคำว่า `src="assets/` ใน `index.html` เพื่อหาตำแหน่งได้ง่ายๆ)

**เกี่ยวกับสัดส่วนรูปภาพ:** กรอบรูปทั่วไป (Projects, UI/UX Design, Activities, Certificates) ใช้ `object-fit: contain`
แปลว่ารูปจะถูกย่อ/ขยายให้พอดีกรอบโดย **เห็นภาพเต็มเสมอ ไม่ถูกครอบตัด** (ถ้าสัดส่วนรูปไม่ตรงกับกรอบพอดี จะมีพื้นที่ว่างสีครีม
ด้านข้าง/บน-ล่างเล็กน้อย ซึ่งเป็นเรื่องปกติ) ยกเว้น **รูปโปรไฟล์ที่หน้าแรก** ซึ่งเป็นกรอบวงกลม ใช้ `object-fit: cover`
เพื่อครอบตัดรูปให้เต็มวงกลมสวยงาม (แนะนำใช้รูปหน้าตรง/รูปสี่เหลี่ยมจัตุรัสเพื่อให้ครอบตัดสวยที่สุด)

**ส่วน Certificates:** เพิ่มเอฟเฟกต์ **เอาเมาส์ชี้ที่รูปแล้วภาพจะขยายใหญ่ขึ้น** (hover to zoom) เพื่อให้เห็นรายละเอียดในใบ certificate ได้ชัดเจนขึ้นโดยไม่ต้องคลิกเปิดไฟล์แยก

## 🔗 แก้ไขข้อมูลติดต่อ / ลิงก์ผลงาน

จุดที่ควรอัปเดตเพิ่มเติมเมื่อมีลิงก์จริง (ปัจจุบันเป็น `#` placeholder):

- ส่วน **UI/UX Design Portfolio** → ใส่ลิงก์ Figma จริงแทน `href="#"` ในแต่ละการ์ด (E-Commerce, Smart Parking, Daily UI)
- ส่วน **Hero Socials** → ใส่ลิงก์ LINE จริงแทน `href="#"` (ปัจจุบันแสดงแค่ไอคอน)
- ตรวจสอบอีเมล/เบอร์โทร/ลิงก์ GitHub ในส่วน `#contact` ให้ตรงกับข้อมูลล่าสุดเสมอ

## 🎨 ปรับแต่งธีมสี

สีหลักกำหนดไว้ที่ตัวแปร CSS ด้านบนของไฟล์ `css/style.css` (ใน `:root`) แก้ค่าที่นี่ที่เดียว
สีทั้งเว็บจะเปลี่ยนตาม (ปัจจุบันเป็นธีมโทนอบอุ่น/สบายๆ):

```css
--bg: #faf5ed;      /* พื้นหลังครีม */
--accent: #d97757;  /* ส้มอิฐ (terracotta) - สีเน้นหลัก ปุ่ม/ลิงก์/ไอคอน */
--sage: #8a9a72;     /* เขียวมอส - ไอคอนหมวด Web Dev / activity ที่ 2 */
--dusty-blue: #6e8fa6; /* ฟ้าหม่น - ไอคอนหมวด Security / activity ที่ 3 */
--mustard: #cf9a3e;  /* เหลืองมัสตาร์ด - GPA chip / cert icon */
--plum: #a97c9e;     /* ม่วงอ่อน - ไอคอนหมวด Soft Skills */
```

## 📞 ข้อมูลติดต่อในเว็บไซต์

- Email: kittisak.sati@bumail.net
- Phone: 099-495-2227
- LINE ID: ohm5187
- GitHub: [github.com/ohmzaa5187](https://github.com/ohmzaa5187)

---

Built with HTML5, CSS3 และ JavaScript (Vanilla) — ไม่ต้องติดตั้ง dependency ใดๆ
